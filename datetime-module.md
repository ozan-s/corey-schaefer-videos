# Python Tutorial: Datetime Module - How to work with Dates, Times, Timedeltas, and Timezones
[Video](https://www.youtube.com/watch?v=eirjjyP2qcQ)

## Create a naive date: Do not have timezone information and do not keep track of daylight savings time
    import datetime
    d = datetime.date(2001, 9, 11)
    
## Get today's date
    tday = datetime.date.today()
    tday.year
    tday.day
    tday.weekday() # Monday 0 Sunday 6
    tday.isoweekday() # Monday 1 Sunday 7
    
## timedelta: Gap between two dates
    tdelta = datetime.timedelta(days=0, seconds=0, microseconds=0, milliseconds=0, minutes=0, hours=0, weeks=0)
    tday + tdelta
    
    date2 = date1 + timedelta
    timedelta = date1 - date2
    
    bday = datetime.date(2016, 9, 24)
    till_bday = bday - tday
    till_bday.days
    till_bday.totalseconds()
    
## Create a naive time
    t = datetime.time(9, 30, 45, 100000)
    t.hour
    t.minute
    
## Create a naive date and time    
    dt = datetime.datetime(2016, 7, 24, 12, 30, 45)
    dt.date()
    dt.time()
    dt.year
    
## Useful datetime constructors
    datetime.datetime.today() # Without any timezone information
    datetime.datetime.now() # Can be made timezone aware by passing tz info
    datetime.datetime.utcnow() # Can be made utc timezone aware by passing utc tz info
    
## Import pytz module to work with timezones
    import pytz
    
## Create timezone aware datetime using pytz
    dt = datetime.datetime(2016, 7, 24, 12, 30, 45, tzinfo=pytz.UTC)

### Recommended to always use UTC timezone
    dt_utcnow = datetime.datetime.now(tz=pytz.UTC)
    dt_utcnow2 = datetime.datetime.utcnow().replace(tzinfo=pytz.UTC)

## Convert datetime to another timezone
    dt_mtn = dt_utcnow.astimezone(pytz.timezone('US/Mountain'))
    
## Get a list of all timezones included in pytz
    for tz in pytz.all_timezones:
        print(tz)
        
## Make a naive datetime timezone aware
    dt_mtn = datetime.datetime.now()
    mtn_tz = pytz.timezone('US/Mountain')
    dt_mtn = mtn_tz.localize(dt_mtn)

## Convert one time zone aware datetime to another timezone
    dt_east = dt_mtn.astimezone(pytz.timezone('US/Eastern'))

## Print datetime in ISO format
    dt_mtn.isoformat()
    
## Print datetime in a custom format    
    dt_mtn.strftime('%B %d, %Y')
    
## Convert string to datetime
    dt_str = 'July 24, 2016'
    dt = datetime.datetime.strptime(dt_str, '%B %d, %Y')
    
    # strftime - Datetime to String
    # strptime - String to Datetime
