# log-pic
Encoding and decoding images using prime number pairs, log, addition, and factoring:

The standard image is 1000x1000, wich comprises of 1,000,000 pixels.
To encode such an image, gather togther the first 257,000,000 primes greater than a million.
There are 1,000,000 pixels, and each one has 256 possible values. Thus, the 2 dimentional image is flattened into 1 dimention.
The first 257 primes are reserved for the first pixel, the next 257 for the second, and so on.
Why 257? The first 256 primes will be for the value, and the 257th will be for the pixel position.
