
Algorithm (Lagrange Interpolation):

            Step 1: Start
            Step 2: Input number of points n, arrays x[n] and y[n], and value of x to be interpolated
            Step 3: Initialize result = 0
            Step 4: For i = 0 to n-1
                - Set term = y[i]
                - For j = 0 to n-1, j ≠ i:
                    term = term * (x - x[j]) / (x[i] - x[j])
                - result = result + term
            Step 5: Output result
            Step 6: Stop
