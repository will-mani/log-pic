# log-pic
Encoding and decoding images using prime number pairs, log, addition, and factoring:

The standard image is 1000x1000, wich comprises of 1,000,000 pixels.
To encode such an image, gather togther the first 257,000,000 primes greater than a million.
There are 1,000,000 pixels, and each one has 256 possible values. Thus, the 2 dimensional image is flattened into 1 dimension.
The first 257 primes are reserved for the first pixel, the next 257 for the second, and so on.
Why 257? The first 256 primes will be for the value, and the 257th will be for the pixel position.
The pixel value prime and the pixel position prime will form a prime pair. Thus, there are 1 million prime pairs for a 1000x1000 image.
Each prime pair tells the value of a pixel at a certain position. The two primes in each pair are multiplied together to form a relatively prime composite.
Now, we want to multiply all the relatively prime composites togther, but the product would be huge, and there would hardly be any compression gains.
To work around this, log might help. Log might be a great help. It could also be a complete failure. 
Anyway, instead of trying to calculate the huge product of relatively prime composites, first find the log of each composite.
Then sum the composite logs together. This might be a round about way of accurately calculating the log of the massive product.
With the sum of logs, to an end comes the encoding.
Next, the decoding. 3 words - bruteforce, bruteforce, bruteforce. 
Remember that huge product of relatively prime composites? We are going to (try to) calculate it!
It's simple - raise the appropriate log base to the power of the log sum, the encoding of the image.
And now the fun part: brute force, brute foce, brute
For each position prime, multiply by each of its 256 value primes. This forms a candidate composite.
The candidate composite that divides (properly, ideally, with a remainder of 0) is the relatively prive composite used in the encoding,
And we have therefore successfully decoded the pixel value at that position. The flattened image can then be turned back into its original 2D form.
And that's that. 
Will this work? I'm pretty sure no. Can this work? It is worth the try.

UPDATE: It does not work because of counting reasons (cannot have one-to-one correspondence with the cardinality of one set (exponent with hundreds of digits (most being after the decimal place)) being much smaller than the cardinality of the other set (huge product representing the image with millions of digits); there's bound to be collisions when going from the original huge number to the relatively small exponent, so ... how do you get a one-to-one mapping from the exponent to the massive product? You don't!) and more simply because exponents do NOT* create a loophole hole for perfectly capturing (thereby effectively compressing) large pattern-deficient numbers. The challenge here is reminiscent of Kolmogorov complexity/randomness. There is a reason why it is hard to compress pattern-deficient/'pattern-low' information. Buzz word for further consideration: entropy.
So in one sense, the idea ended up being a failure, but in another, more accurate sense, it has become a learning opportunity and therefore not a failure. Success, just not how I pictured it (most definitely intended too keep the pun).
