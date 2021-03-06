# Image Smoothing 

Image is just a picture that we see in books,magazines,phones,etc.

Mathematically an image may be defined as _A(x,y) = H(x,y) + B(x,y)_ where, A(x,y)= function of noisy image, H(x,y)= function of image noise , B(x,y)= function of original image.But in theoretical terms, a picture that we look at is a function of image intensity at a particular position in the image i.e.  __f(x,y)__ , where __x__ and __y__ are spatial co-ordinates and the amplitude of _f_ at any pair of co-ordinate (x,y) is called the _intensity_ or _gray level_ of the image at that point.When x,y and the amplitude values of f are all finite , discrete quantities we call the image a digital image.

## Noise in Images

Image noise is random variation of brightness or color information in the images captured. It is degradation in image signal caused by external sources.Images containing multiplicative noise have the characteristic that the brighter the area the noisier it. But mostly it is additive.

## Sources of Image noise

* While image being sent electronically from one place to another.
* Sensor heat while clicking an image.
* With varying ISO Factor which varies with the capacity of camera to absorb light.

## Types of Image noise:


There are different types of image noise.

* __Gaussian Noise__

    Gaussian Noise is a statistical noise having a probability density function equal to normal distribution, also known as Gaussian Distribution. Random Gaussian function is added to Image function to generate this noise. It is also called as electronic noise because it arises in amplifiers or detectors.

* __Salt and Pepper Noise__

    Salt and Pepper noise is added to an image by addition of both random bright (with 255 pixel value) and random dark (with 0 pixel value) all over the image.This model is also known as data drop noise because statistically it drop the original data values.

*  __Poisson Noise__

    The appearance of this noise is seen due to the statistical nature of electromagnetic waves such as x-rays, visible lights and gamma rays. The x-ray and gamma ray sources emitted number of photons per unit time. These rays are injected in patient’s body from its source, in medical x rays and gamma rays imaging systems. These sources are having random fluctuation of photons. Result gathered image has spatial and temporal randomness. This noise is also called as quantum (photon) noise or shot noise.

* __Speckle Noise__

    A fundamental problem in optical and digital holography is the presence of speckle noise in the image reconstruction process. Speckle is a granular noise that inherently exists in an image and degrades its quality. Speckle noise can be generated by multiplying random pixel values with different pixels of an image.

To remove these noises from images there are many methods used. Among them is image-smoothing or image-denoising.

Image blurring(Image-smoothing) is achieved by convolving the image with a low-pass filter kernel. It is useful for removing noise. It actually removes high frequency content (eg: noise, edges) from the image. So edges are blurred a little bit in this operation (there are also blurring techniques which don't blur the edges). OpenCV provides four main types of blurring techniques.

* Averaging
* Gaussian Blurring
* Median Blurring
* Bilateral Filtering

Here we are only going to discuss the below three techniques.


