<!---
  category: GraphicsAndAnimation
  samplefwlink: http://go.microsoft.com/fwlink/p/?LinkId=852875
--->

# Direct2D advanced color image rendering sample

Shows how to use [Direct2D](http://msdn.microsoft.com/library/windows/desktop/dd370990) to load and draw advanced color images.

> **Note:** This sample is part of a large collection of UWP feature samples. 
> If you are unfamiliar with Git and GitHub, you can download the entire collection as a 
> [ZIP file](https://github.com/Microsoft/Windows-universal-samples/archive/master.zip), but be 
> sure to unzip everything to access shared dependencies. For more info on working with the ZIP file, 
> the samples collection, and GitHub, see [Get the UWP samples from GitHub](https://aka.ms/ovu2uq). 
> For more samples, see the [Samples portal](https://aka.ms/winsamples) on the Windows Dev Center. 

Specifically, this sample shows how to:

- Create and configure an advanced color (FP16) DirectX render pipeline.
- Load a JPEG XR containing extended-range floating point data from the disk and decode it with WIC.
- Use Direct2D's effect pipeline to correctly handle an attached ICC profile.
- Implement a custom Direct2D image effect to perform HDR-to-SDR tone mapping, so that HDR images can be rendered in higher quality on SDR displays.
- Use DXGI to retrieve display color capabilities and determine whether tone mapping should be applied.

## Sample project files

The sample's project files fall into the following categories.

### Sample-specific files
The following files form the main educational content of the sample:

- **DirectXPage.xaml/.cpp/.h/:** Implements a XAML-based UI to drive the app. Hosts the DirectX content in a SwapChainPanel.
- **App.xaml/.cpp/.h:** The app's main entry point.
- **D2DAdvancedColorImagesRenderer.cpp/.h:** The core implementation of the Direct2D scene.

### DirectX SDK sample common files
The following files provide common functionality needed by DirectX SDK samples:

- **DeviceResources.cpp/.h:** Manages creation and lifetime of the core Direct3D and Direct2D device-dependent resources. Handles cases such as device lost and window size and orientation changes.
- **DirectXHelper.h:** Common inline helper functions, including ThrowIfFailed which converts HRESULT-based APIs into an exception model.

All DirectX SDK samples and the Visual Studio template DirectX projects contain a version of these files. These common files demonstrate important best practices for DirectX UWP apps, and you are encouraged to use them in your own projects.

### C++ UWP common files
Variants of the following files are found in every UWP app written in C++:

- Package.appxmanifest
- pch.cpp/.h
- D2DAdvancedColorImagesRenderer.vcxproj
- D2DAdvancedColorImagesRenderer.vcxproj.filters
- D2DAdvancedColorImagesRenderer.sln

## Related topics

### Feature areas

[Direct2D](http://msdn.microsoft.com/library/windows/desktop/dd370990): used to render images, primitives, and text.  
[XAML overview](https://msdn.microsoft.com/library/windows/apps/mt185595): technology for building user interfaces in managed and C++ code.  

### Reference

Direct2D APIs:

[Color management effect](https://msdn.microsoft.com/en-us/library/windows/desktop/hh706318)  
[ID2D1DeviceContext2::CreateImageSourceFromWic method](https://msdn.microsoft.com/en-us/library/windows/desktop/dn890793)  

DXGI APIs:

IDXGIOutput6  

Related APIs:

[SwapChainPanel](https://msdn.microsoft.com/library/windows/apps/windows.ui.xaml.controls.swapchainpanel)  

## System requirements

**Client:** Windows 10

**Server:** Windows Server 2016 Technical Preview

**Phone:** Windows 10

## Build the sample

1. If you download the samples ZIP, be sure to unzip the entire archive, not just the folder with the sample you want to build. 
2. Start Microsoft Visual Studio 2017 and select **File** \> **Open** \> **Project/Solution**.
3. Starting in the folder where you unzipped the samples, go to the Samples subfolder, then the subfolder for this specific sample, then the subfolder for your preferred language (C++, C#, or JavaScript). Double-click the Visual Studio 2017 Solution (.sln) file.
4. Press Ctrl+Shift+B, or select **Build** \> **Build Solution**.

## Run the sample

The next steps depend on whether you just want to deploy the sample or you want to both deploy and run it.

### Deploying the sample

- Select Build > Deploy Solution. 

### Deploying and running the sample

- To debug the sample and then run it, press F5 or select Debug >  Start Debugging. To run the sample without debugging, press Ctrl+F5 or selectDebug > Start Without Debugging. 

## Run the sample

The next steps depend on whether you just want to deploy the sample or you want to both deploy and run it.

### Deploying the sample

- Select Build > Deploy Solution. 

### Deploying and running the sample

- To debug the sample and then run it, press F5 or select Debug >  Start Debugging. To run the sample without debugging, press Ctrl+F5 or selectDebug > Start Without Debugging. 