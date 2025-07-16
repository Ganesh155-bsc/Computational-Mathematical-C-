Algorithm (Newton Backward Interpolation):

            Step 1: Start  
            Step 2: Input initial guesses x0 and x1  
            Step 3: Calculate y0 = f(x0), y1 = f(x1)  
            Step 4: If y0 * y1 > 0, then  
              Print "Invalid initial values. Root may not lie between them."  
              Stop  
            Step 5: Repeat while |x1 - x0| > ε (epsilon = 0.0001):  
              - x2 = (x0 + x1) / 2  
              - y2 = f(x2)  
              - If y0 * y2 < 0:  
                x1 = x2  
                y1 = y2  
              - Else:  
                x0 = x2  
                y0 = y2  
            Step 6: Output x2 as the approximate root  
            Step 7: Stop  


Algorithm (Newton Forward Interpolation):

            Step 1: Start
            Step 2: Input number of data points n
            Step 3: Input arrays x[0...n-1] and corresponding y[0...n-1][0] (i.e., f(x) values)
            Step 4: Input the value of x (say, value) to be interpolated
            Step 5: Construct the forward difference table
                       - For i = 1 to n-1
                       - For j = 0 to n-i-1      
                       - y[j][i] = y[j+1][i-1] - y[j][i-1]
            Step 6: Calculate h = x[1] - x[0]
            Step 7: Compute u = (value - x[0]) / h
            Step 8: Initialize sum = y[0][0] and term = 1
            Step 9: For i = 1 to n-1   
                       - term = term * (u - (i - 1))
            sum = sum + (term * y[0][i]) / fact(i)
            Step 10: Output interpolated value sum
            Step 11: Stop
       
Algorithm (Bisection Method):
            
            Step 1: Start  
            Step 2: Input initial guesses x0 and x1  
            Step 3: Calculate y0 = f(x0), y1 = f(x1)  
            Step 4: If y0 * y1 > 0, then  
              Print "Invalid initial values. Root may not lie between them."  
              Stop  
            Step 5: Repeat while |x1 - x0| > ε (epsilon = 0.0001):  
              - x2 = (x0 + x1) / 2  
              - y2 = f(x2)  
              - If y0 * y2 < 0:  
                x1 = x2  
                y1 = y2  
              - Else:  
                x0 = x2  
                y0 = y2  
            Step 6: Output x2 as the approximate root  
            Step 7: Stop  

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

Algorithm (Trapezoidal Rule):

            Step 1: Start  
            Step 2: Input lower limit a, upper limit b, and number of intervals n  
            Step 3: Calculate step size h = (b - a) / n  
            Step 4: Initialize sum = f(a) + f(b)  
            Step 5: For i = 1 to n-1  
                    - Calculate x = a + i * h  
                    - sum = sum + 2 * f(x)  
            Step 6: Compute result = (h / 2) * sum  
            Step 7: Output result  
            Step 8: Stop
