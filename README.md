**Completely re-written from the ground up for 2023!**

Built using AppKit instead of SwiftUI, CIFilterBox 2 is much more stable and much MUCH faster!

# CIFilterBox

*Test the filters in real-time.*

![ReadingBar Icon](https://github.com/DavidWingate/CIFilterBox/raw/main/icon_128x128.png)

See the Core Image Filters working in real-time. Tweak the settings and see instant results. Accomplish in a few clicks what would have taken hours in code.

https://www.davidwingate.dev/cifilterbox

---

If you have ever used CIFilters in your code, you will know they can be difficult and time-consuming. The filters are powerful and versatile, but the documentation is sparse and opaque. Finding out what a specific filter does and how to control it can take hours of reading, coding, and experimentation.

With CIFilterBox it takes a few clicks.

- Choose from 228 built-in CIFilters (search by name, OS, or category)
- Easily change the filter settings using simple controls
- See the output image updated in real-time
- Get a code snippet of the current filter and settings

CIFilterBox has a simple and intuitive interface. Quickly find your filter and start playing with the settings. The output image will update in real-time, showing what the filter does and how the settings work. You can use your own input images or choose from the built-in stock photos. Select a background to show the transparent areas of the output, and either crop the image extent or view the filter's full output. You can even use the output image as an input to simulate filter chaining.

- Use simple controls for the major input key classes, including: NSNumber, CIColor, CIVector, NSAffineTransform, and NSString
- Direct input for position, angle, rectangle, and transform, so you can point, click, and drag directly on the image to change the settings
- Use your own input images or choose from the built-in stock photos (curtesy of Gratisography)
- View information on each input key including Class, Type, and Description
- Receive warnings for common filter problems such as 'image of infinite extent'
- Crop the image extent, or view the full un-cropped output
- Set a custom cropping extent for filters with no input image

Once you have the output you need you can copy a code snippet to the clipboard to use in your own code. The output image can be saved as a PNG file, or you can share directly from the app using the standard MacOS sharing service.

- Toggle the filter on and off to compare the filtered image with the original
- Select a background style to best display the transparent areas of different outputs
- Use the output image as the input to simulate filter chaining
- Share the output image via the MacOS sharing service (email, Airdrop etc.)
- Save the output image as a PNG file

I made CIFilterBox for myself after spending too many hours learning what the filters do and how to work them. I hope this app can save you from losing that precious time! Known issues are listed below, but if you spot anything that is missing, broken, or just wrong, I would be grateful if you could let me know—I will do my best to fix it.

Known Issues:

- Core Image stores a cache for each filter, which can sometimes result in a large memory footprint. This is most noticeable with CIPersonSegmentation and CISaliencyMapFilter. Use judiciously.
- The grayscale slider in the colour panel always switches back to RGB on edit, because the interface only uses RGBA values for simplicity
- Some filters have been removed because they crash the app (CIMorphologyRectangleMaximum, CIMorphologyRectangleMinimum, CIPaletteCentroid, CIPalettize, and CIMeshGenerator)
- Some filters are too complex for the current interface, but are still included for information (CICameraCalibrationLensCorrection, CIBarcodeGenerator, CIMeshGenerator, CICoreMLModelFilter, and CIAttributedTextImageGenerator)
- Some filters are non-functional and undocumented, but are still included for information (CIKMeans)
