# Problem Set 2 Report

In this assignment, I perform various image processing tasks on an RGB image retrieved from a URL using the updated code. The main tasks include resizing the image to 224x224 pixels, creating grayscale copies using different methods, and convolving the grayscale image with 10 random filters. I also display the filters and the resulting feature maps for each convolution.

## Load and Resize the Image

I begin by loading an RGB image from the given URL and resizing it to 224x224 pixels. The original image is shown below:

![Original Image](https://www.akc.org/wp-content/uploads/2017/11/Nova-Scotia-Duck-Tolling-Retriever-slide1.jpg)

After resizing, the image looks like this:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/c368872f-e3f6-4f76-a847-11d51ce93be3)

The dimensions of the resized image are (224, 224, 3).

## Grayscale Conversion Methods

I explore different methods for converting the resized image to grayscale using the updated code and also discuss their technical and qualitative differences:

### 1. Averaging Method:

**Technical Explanation:** In the averaging method, each pixel in the grayscale image is calculated as the mean of the RGB values of the corresponding pixel in the resized image. Mathematically, grayscale pixel value (G) is computed as `(R + G + B) / 3`, where R, G, and B are the red, green, and blue channel values of the original pixel.

**Qualitative Differences:** This method tends to produce grayscale images with balanced brightness, as it evenly weights all color channels. However, it may not capture subtle color variations.

**Preference for Tasks:** The averaging method is suitable for tasks where preserving the overall brightness and luminance is essential. It can work well for general-purpose grayscale conversions but might not be ideal for tasks that require fine details or color emphasis.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/4fe35fd2-7339-4000-aa10-8e13f238e205)

### 2. Red Channel Method:

**Technical Explanation:** In the red channel method, we extract only the red channel from the resized image and treat it as a grayscale image. The red channel contains information primarily related to red hues.

**Qualitative Differences:** This method emphasizes red tones and can highlight objects with strong red coloration. It discards green and blue information, which might result in the loss of detail in other color channels.

**Preference for Tasks:** The red channel method is useful when you want to accentuate red features or objects in an image. It's often used in applications like vegetation analysis, where green areas are less important, or when emphasizing red objects like stop signs in traffic sign recognition.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/1d1db500-9ea5-4744-b2e7-2c43944476ac)

### 3. Luminance Method:

**Technical Explanation:** The luminance method calculates grayscale values using a weighted sum of the RGB channels based on luminance coefficients. These coefficients are typically `[0.299, 0.587, 0.114]`, reflecting the human eye's sensitivity to different colors. Grayscale pixel value (G) is computed as `0.299 * R + 0.587 * G + 0.114 * B`.

**Qualitative Differences:** The luminance method preserves human-perceived brightness and offers a better representation of color details compared to simple averaging. It's more perceptually accurate.

**Preference for Tasks:** The luminance method is well-suited for tasks where preserving the perceived brightness and color details are crucial, such as image compression, where human visual fidelity is important. It's also used in grayscale versions of color photographs for better aesthetics.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/ace4f974-8928-4044-bab1-ea66ceccc01f)

### 4. Channel Mixing Method:

**Technical Explanation:** In the channel mixing method, we assign different coefficients to the RGB channels, allowing for a customizable grayscale conversion. Each channel's contribution can be adjusted to emphasize certain colors or deemphasize others.

**Qualitative Differences:** This method provides control over the emphasis of specific colors in the grayscale image. By adjusting coefficients, you can create various artistic effects or highlight specific color features.

**Preference for Tasks:** The channel mixing method is versatile and can be tailored for artistic or creative purposes. It's preferred when you want fine control over color emphasis and artistic expression. For example, it can be used in photo editing for creating unique grayscale styles.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/d4726dc9-9ce2-49cd-87fd-8bd8c475dcc6)

## Convolution with Random Filters

I perform convolution on the grayscale image using 10 random filters using the updated code. For each filter, I display the filter itself and the resulting feature map.

### Filter 1

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/ba5f3b0f-f09a-4e0b-9e28-b930d7166e3f)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/8fe8206c-d8a6-4850-9e3c-7051f8703475)

### Filter 2

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/6df62657-75c7-426e-be95-beb9bc666c9e)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/444076bd-c671-4e2b-b234-31563f8e567d)

### Filter 3

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/c4530ed3-9a73-497e-a7f1-6372e219e7cb)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/a8ec5eef-3683-48bf-9ce9-f6ebc731cb2b)

### Filter 4

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/38f02c32-bb02-4a20-91c9-8b85025430af)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/d2587b43-f0e2-4b29-84be-a5a593804c2e)

### Filter 5

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/bb52be0a-7a4d-47c8-8b28-c1d2ac39f73d)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/103c767a-25ce-4612-9611-e3628b96d25c)

### Filter 6

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/c84f37bd-f270-4074-845f-4943c3a35add)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/d409bcb2-883a-4863-826a-25ab8c0363d6)

### Filter 7

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/9a9ddb5c-e246-4e7d-8758-d500febbefc9)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/fc8f4964-faf4-4c0b-ad18-fa267a3a02a3)

### Filter 8

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/27fe4ad8-fd3a-4428-8978-98df09b7260a)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/e1d1d2a3-1b4a-4c62-a6c3-074a0cf92fe0)

### Filter 9

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/5389743d-d189-4778-b187-0a3ce327a87a)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/d1427510-a387-4a7f-b6fa-a3a55fab3f23)

### Filter 10

Filter:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/85bd62b7-2991-4d23-9102-7aa8d1018853)

Feature Map:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/0b9abb51-56e2-495c-9c0e-12599070f9b6)

## Custom Convolution Function

I have also implemented a custom convolution function using the updated code. Here's an explanation of the custom convolution function:

**Technical Explanation:**
- The `custom_convolve` function takes two arguments: the input image and a kernel.
- It calculates the dimensions of the output image based on the kernel size and pads the input image to handle edge pixels.
- The convolution operation is performed by iterating over the input image using nested loops.
- At each position, the function computes the element-wise multiplication between the kernel and the corresponding region of the input image.
- The sum of these element-wise products is assigned to the corresponding pixel in the output image.
- Finally, the padded border is removed from the output image to match the original image dimensions.

**Comparison with scipy.signal.convolve2d:**
- I compare the results of the custom convolution with those obtained using the `scipy.signal.convolve2d` function.
- The two results are identical, indicating that the custom convolution function successfully replicates the convolution operation performed by the scipy library.

Custom Convolution Result:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/10d7942e-1728-4058-986d-f2d0e755e43f)

Scipy Convolution Result:

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/7c3d4a88-05cb-4b6b-9f3d-92df28be20fe)

## Additional Filters

In addition to the random filters, I applied several custom filters to the grayscale image using the updated code, each chosen for specific purposes:

### 1. Pencil Sketch Filter

**Why it was Chosen:** The pencil sketch filter is commonly used in image processing to create a sketch-like or artistic effect. It

 can help simplify an image's details, making it look like a hand-drawn pencil sketch.

**Effect on Image:** The pencil sketch filter enhances edges and lines while reducing the influence of fine details and textures. It achieves this by emphasizing high-contrast areas and smoothing low-contrast regions. The result resembles a black-and-white pencil drawing.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/666dcd50-4ef8-4725-a929-1176bca7be08)

### 2. Motion Blur Filter

**Why it was Chosen:** The motion blur filter simulates the effect of motion or blurriness in an image. It can be used for various purposes, including conveying movement or adding a sense of dynamism.

**Effect on Image:** The motion blur filter blurs the image in the direction of motion, creating a streaking effect. In the example, it gives the impression of a moving object, making the image appear as though it was captured while the subject was in motion.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/1590f595-0a73-4a8e-9214-5ad23b452ab5)

### 3. Unsharp Masking Filter

**Why it was Chosen:** The unsharp masking filter is a sharpening technique used to enhance edges and fine details in an image while reducing noise and unwanted artifacts.

**Effect on Image:** The unsharp masking filter enhances the image's sharpness by subtracting a blurred version of the image from the original. This process highlights edges and fine details, resulting in a crisper appearance. It's often used in image enhancement to bring out key features.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/c17db773-2392-4f2c-aa5e-16be756e5300)

### 4. Edge Highlight Filter

**Why it was Chosen:** The edge highlight filter is designed to emphasize the edges or boundaries between objects and regions in an image. It's useful for highlighting object contours and enhancing structure.

**Effect on Image:** The edge highlight filter enhances high-contrast edges in the image, making them more pronounced. It does this by boosting the intensity differences between neighboring pixels along edges. The result is an image with enhanced edge definition, which can be beneficial for object recognition and segmentation.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/77e07798-0193-4c22-9f1f-125251199043)

### 5. Polarized Light Filter

**Why it was Chosen:** The polarized light filter simulates the effects of polarized light on an image. It can be used for various purposes, including creating artistic effects or emphasizing certain textures.

**Effect on Image:** The polarized light filter alters the image's appearance by modifying the intensity and direction of light reflections. It can create patterns and visual effects that mimic the behavior of polarized light in the real world. The result can be artistic and visually striking.

![image](https://github.com/iklopukh2021/MathDataSci/assets/143549784/d2b0da84-0c16-4246-8634-73e1467f1aa5)

## Conclusion

In conclusion, image processing is a versatile field with a wide range of techniques and methods that can be applied to achieve various visual effects and enhance image features. Grayscale conversion methods provide flexibility in preserving brightness and detail, while custom and random filters offer creative and technical options for manipulating images. The choice of method or filter depends on the specific requirements of the task and the desired visual outcome.

This assignment provided valuable hands-on experience in image processing techniques, enabling us to understand the technical nuances and creative possibilities within this field. These skills can be applied to a wide array of applications, including computer vision, image analysis, and artistic image manipulation.
