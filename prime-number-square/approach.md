The document describes an optimized algorithm for finding all prime numbers up to a given number \( n \). Here's a summary of the approach:

1. **Brute Force Method**  
   - Iterate from \( 2 \) to \( n \) and check each number for primality using a prime-checking function (which runs in \( O(\sqrt{n}) \)).
   - Overall time complexity: \( O(n\sqrt{n}) \), which is inefficient for large \( n \).

2. **Optimized Approach: Sieve of Eratosthenes**  
   - Instead of checking primality for each number individually, use an array (`prime[]`) to mark prime numbers efficiently.
   - Steps:
     - Create a boolean array of size \( n+1 \) initialized to `true` (indicating all numbers are initially assumed to be prime).
     - Iterate from \( 2 \) to \( \sqrt{n} \), marking multiples of each prime as `false` (since they are composite).
     - After processing, the remaining `true` values in the array represent prime numbers.

3. **Further Optimizations**  
   - Instead of marking multiples from \( 2 \), start marking from \( p^2 \) (since smaller multiples would have already been marked by smaller primes).
   - Only iterate up to \( \sqrt{n} \) to optimize marking.

4. **Time and Space Complexity**  
   - **Time Complexity:** \( O(n \log \log n) \), derived from mathematical proof related to prime harmonic series.
   - **Space Complexity:** \( O(n) \), since an array of size \( n \) is used.

The algorithm significantly improves efficiency compared to the brute force method, making it suitable for large values of \( n \).