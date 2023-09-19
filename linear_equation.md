To plot a linear equation in Python, such as `y = mx + b`, where `m` is the slope and `b` is the y-intercept, you can use Matplotlib to create the plot. Here's a step-by-step example:

```python
import numpy as np
import matplotlib.pyplot as plt

# Define the values of m and b for your linear equation
m = 2  # Slope
b = 3  # Y-intercept

# Generate x values (e.g., from -10 to 10)
x = np.linspace(-10, 10, 100)  # 100 points between -10 and 10

# Calculate y values using the linear equation y = mx + b
y = m * x + b

# Create the plot
plt.plot(x, y, label=f'y = {m}x + {b}', color='blue', linestyle='-')

# Add labels and a legend
plt.xlabel('x')
plt.ylabel('y')
plt.title('Linear Equation Plot')
plt.legend()

# Show the plot
plt.grid(True)
plt.show()
```

Here's what this code does:

1. Import the necessary libraries: NumPy for generating x values and performing calculations, and Matplotlib for plotting.

2. Define the values of `m` (slope) and `b` (y-intercept) for your linear equation.

3. Generate a range of x values using `np.linspace`, which creates 100 evenly spaced points between -10 and 10.

4. Calculate the corresponding y values using the linear equation `y = mx + b`.

5. Create the plot using `plt.plot`, specifying the x and y values. You can customize the appearance of the plot by adjusting properties like color and linestyle.

6. Add labels to the x and y axes, a title to the plot, and a legend that shows the equation.

7. Display the grid using `plt.grid(True)` for better readability (optional).

8. Finally, use `plt.show()` to display the plot.

Running this code will produce a plot of the linear equation `y = 2x + 3`, but you can change the values of `m` and `b` to plot different linear equations.
