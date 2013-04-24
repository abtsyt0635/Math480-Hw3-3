Math480-Hw3-3
=============

3. Compute a list of all prime numbers up to 10000.

def list_primes(n):
    numbers = set(range(n, 1, -1))
    primes = []
    while numbers:
            p = numbers.pop()
            primes.append(p)
            numbers.difference_update(set(range(p*2, n+1, p)))
    return primes
 
print list_primes(10000)
