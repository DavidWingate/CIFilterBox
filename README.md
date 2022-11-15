**CIFilterBox is currently unavailable.** The old SwiftUI version is far too crashy, so I'm writing a new AppKit version to improve stability and performance. I expect it to be ready in early 2023. Sorry, but it will be back and it will be better!

# CIFilterBox

*Test the filters in real-time.*

![ReadingBar Icon](https://github.com/DavidWingate/CIFilterBox/raw/main/icon_128x128.png)

See the Core Image Filters working in real-time. Tweak their settings and see instant results. Accomplish in a few clicks what might have taken hours in code.

https://www.davidwingate.dev/cifilterbox

---

If you have ever used CIFilters in your code, you will know they can be difficult and time-consuming to implement. The filters are powerful and versatile, but the documentation can be sparse and opaque. Finding out what a specific filter does and how to control it can take hours of reading, coding, and experimentation.

With CIFilterBox it takes a few clicks.

- Choose from 228 built-in CIFilters
- Easily change the filter settings using simple controls
- See the output image updated in real-time
- Get a code snippet of the current filter and settings

CIFilterBox has a simple and intuitive interface. Quickly find your filter and start playing with the settings. The output image will update in real-time, showing what the filter does and how the settings work. You can use your own input images or choose from the built-in stock photos. Select a background to show the transparent areas of the output, and either crop the image extent or view the full un-cropped output. You can even use the output image as an input to simulate filter chaining.

- Use simple controls for the major input key classes, including: NSNumber; NSAffineTransform; CIColor; CIVector; NSString; NSAttributedString
- Use your own input images or choose from the built-in stock photos
- Arrange the images in a customisable grid
- View information on each input key including Class, Type, and Description
- Receive warnings for common filter problems such as 'image of infinite extent'
- Set a custom output extent for filters with no input image

Once you have the output you need you can copy a code snippet to the clipboard for use in your own code. The output image can be saved as a PNG file, or you can share directly from the app using the standard MacOS sharing service.

- See the output image update in real-time
- Toggle the filter on and off to compare the filtered image with the original
- Crop the image extent, or view the full un-cropped output
- Zoom to fit within the window, or use a scroll view at full resolution
- Select a background to show the transparent areas of the output
- Select from Grid, Black, White, Window (Clear), or Image
- Use your own image, the input image, or one of the built-in stock photos
- View a code snippet of the current filter and settings, and copy it to the clipboard
- Use the output image as the input to simulate filter chaining
- Share the output image via the MacOS sharing service (email, Airdrop etc.)
- Save the output image as a PNG file

I made CIFilterBox for myself after spending too many hours learning what the filters do and how to work them. I hope this app can save you from losing that precious time! CIFilterBox is built entirely in SwiftUI, and takes advantage of some of the new features recently made available to MacOS. This means that there are still some improvements to be made at a system level. Known issues are listed below, but if you spot anything that is missing, broken, or just wrong, I would be grateful if you could let me know—I will do my best to fix it.

Known Issues:

- SwiftUI stores a cache for each filter, which can sometimes result in a large memory footprint. This is most noticeable with CIPersonSegmentation and CISaliencyMapFilter. Use judiciously.
- The grayscale slider in the colour panel always switches back to RGB on edit
- Two filters have been removed because they crash the app for unknown reasons (CIMorphologyRectangleMaximum and CIMorphologyRectangleMinimum)
- Some filters are simply too complex for this type of interface, but are still included for information (CICameraCalibrationLensCorrection, CIBarcodeGenerator, CIMeshGenerator, and CICoreMLModelFilter)
- Some filters are non-functional and undocumented, but are still included for information (CIKMeans, CIPaletteCentroid, and CIPalettize)
