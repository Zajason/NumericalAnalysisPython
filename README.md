# NumericalAnalysisPython

A Hilbert matrix is a matrix of the form Hij = 1/(i + j + 1), where both indices i and j start from 0. For example, the 4 × 4 Hilbert matrix is as follows:

1 1/2 1/3 1/4 1/2 1/3 1/4 1/5 1/3 1/4 1/5 1/6 1/4 1/5 1/6 1/7

Hilbert Matrices: The Hilbert matrices are often used to test algorithms in numerical linear algebra, as they often exhibit "peculiar behavior" ... something you will observe shortly by performing the following steps:

(a) Write code that generates an n×n Hilbert matrix and name it H. Test your code for various values of n to verify that it works correctly. (b) Create a vector with elements equal to 1 using the code b = np.ones((n, 1)) and then solve the system Hx = b using the factorization mentioned in the previous section. (c) Change the value of the first element of b by a very small amount (e.g., add the number 10^-15 to it) and name the resulting vector bnew. Solve the system Hxnew = bnew and then calculate the maximum absolute difference as obtained from the following line of code: np.max(np.abs(x − xnew)). What do you observe? Does the result agree with what you would expect? (d) Create a plot with the values of n on the horizontal axis and the values of the maximum absolute difference on the vertical axis. What conclusions can you draw from this plot regarding the solution of the system Hx = b? (e) You know that the result HH^−1 should be the identity matrix. For different values of n, compute HH^−1 (using np.linalg.inv() to directly calculate the inverse) and then calculate the 2-norm of the difference between the identity matrix (np.identity(n)) and the matrix HH^−1 that you computed. Finally, create a plot with the values of n on the horizontal axis and the values of the 2-norm (as defined earlier) on the vertical axis. What do you observe? What does this mean for the process of inverting Hilbert matrices?

Approximation Problem

The task is to construct a 4th-degree polynomial that best approximates the function:

y=cos⁡(4t)+0.1ε(t)y=cos(4t)+0.1ε(t)

at 50 equally spaced points with tt ranging from 0 to 1. In this problem, we assume that ε(t) is a function that generates normally distributed white noise. In Python, you can import y as:

y = np.cos(4 * t) + 0.1 * np.random.randn(t.shape[0])

First, create the vectors t and y that will contain the data/observations. Then, find the 4th-degree polynomial that best approximates the above function for the given observations, using the method of least squares. Solve the resulting system using both LU factorization (method 1) and QR factorization (method 2). Provide the sum of the squared errors resulting from the above approximation for each method, and provide a plot that contains the data and the curve of the best approximation you arrived at.
