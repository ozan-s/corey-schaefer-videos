# Python SQLite Tutorial: Complete Overview - Creating a Database, Table, and Running Queries
[Video](https://www.youtube.com/watch?v=pd-0G0MigUA)

## Setting up SQLite, creating database and table
    import sqlite3
    conn = sqlite3.connect(':memory:') # In memory db
    conn = sqlite3.connect('employee.db') # Database file
    c = conn.cursor()
    c.execute("""CREATE TABLE employees (
            first text,
            last text,
            pay integer
            )""")
    conn.commit() # Required to save changes
    conn.close()
    
## Insert data into the table
    c.execute("INSERT INTO employees VALUES ('Corey', 'Schaefer', 50000)")
    
## Query data
    c.execute("SELECT * FROM employees WHERE last='Schaefer'")
    c.fetchone() # Get next row in results
    c.fetchmany(5) # Get 5 results
    c.fetchall() # Get all the results
    
## Query data using variables
    c.execute("INSERT INTO employees VALUES (?, ?, ?)", (emp.first, emp.last, emp.pay))
    c.execute("INSERT INTO employees VALUES (:first, :last, :pay)", {'first': emp.first, 'last': emp.last, 'pay': emp.pay})
    c.execute("SELECT * FROM employees WHERE last=?", ('Schaefer',) # Input has to be a tuple!
    
## Use context manager to make changes in the database
    with conn:
        c.execute("INSERT INTO employees VALUES (:first, :last, :pay)", {'first': emp.first, 'last': emp.last, 'pay': emp.pay})
    
    with conn:
        c.execute("""UPDATE employees SET pay = :pay
                    WHERE first = :first AND last = :last""",
                  {'first': emp.first, 'last': emp.last, 'pay': pay})

### This automatically commits the changes and rolls the change back if an exception is raised.
