## Quadratic Equation Roots

Given a quadratic equation in the form ax2 + bx + c. Find its roots.

Note: Return the maximum root followed by the minimum root.

```cpp
vector<int> quadraticRoots(int a, int b, int c) {
        int discriminant = b * b - 4 * a * c;
        if (discriminant < 0) {
            return {-1}; // Imaginary roots
        }
        
        double root1 = (-b + sqrt(discriminant)) / (2.0 * a);
        double root2 = (-b - sqrt(discriminant)) / (2.0 * a);
        
        int r1 = floor(root1);
        int r2 = floor(root2);
        
        vector<int> roots = {r1, r2};
        sort(roots.begin(), roots.end(), greater<int>());
        
        return roots;
       
    }
```
