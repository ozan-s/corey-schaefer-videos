# Matplotlib Tutorial (Part 1): Creating and Customizing Our First Plots
[Video](https://www.youtube.com/watch?v=UO98lJQ3QGI)

## Install matplotlib
    pip install matplotlib
    from matplotlib import pyplot as plt
    
## Create a simple plot
    plt.plot(dev_x, dev_y)
    plt.show()
    
## Add labels to the plot
    plt.title('Chart Title')
    plt.xlabel('X-axis Label')
    plt.ylabel('Y-axis Label')
    
## Plot two lines on the same chart
    plt.plot(ages_x, py_dev_y)
    plt.plot(ages_x, js_dev_y)
    
## Add legend
    plt.legend(['Python', 'JavaScript'])
    
    # Alternative
    plt.plot(ages_x, py_dev_y, label='Python')
    plt.plot(ages_x, js_dev_y, label='JavaScript')
    
## Format line using format strings
    plt.plot(ages_x, py_dev_y, 'k--', label='Python')
    plt.plot(ages_x, js_dev_y, 'b', label='JavaScript')
    
## Format lines using explicit arguments
    plt.plot(ages_x, dev_y, color='k', linestyle='--', marker='.', label='All Devs')
    plt.plot(ages_x, py_dev_y, color='#444444', linestyle='-', marker='o', label='Python')
    
## Make lines thicker
    plt.plot(ages_x, py_dev_y, color='#444444', linestyle='-', marker='o', linewidth=3, label='Python')
    
## Fix padding issues on small screens
    plt.tight_layout()
    
## Add a grid
    plt.grid(True)
    
## See a list of available built-in styles
    print(plt.style.available)
    
## Use one of the available built-in styles
    plt.style.use('fivethirtyeight')
    plt.style.use('ggplot')
    plt.xkcd()
    
## Save the plot as a file
    plt.savefig('plot.png')
