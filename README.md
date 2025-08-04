# log-pic
Encoding and decoding images using prime number pairs, log, addition, and factoring:

The standard image is 1000x1000, wich comprises of 1,000,000 pixels.
To encode such an image, gather togther the first 257,000,000 primes greater than a million.
There are 1,000,000 pixels, and each one has 256 possible values. Thus, the 2 dimentional image is flattened into 1 dimention.
The first 257 primes are reserved for the first pixel, the next 257 for the second, and so on.
Why 257? The first 256 primes will be for the value, and the 257th will be for the pixel position.
The pixel value prime and the pixel position prime will form a prime pair. Thus, there are 1 million prime pairs for a 1000x1000 image.
Each prime pair tells the value of a pixel at a certain position. The two primes in each pair are multiplied together to form a relatively prime composite.
Now, we want to multiply all the relatively prime composites togther, but the product would be huge, and there would hardly be any compression gains.
