Title: Fooocus forks and variants
Date: 2024-01-05 10:20
Modified: 2024-01-05 10:20
Slug: forks
Authors: FooocusFan
Summary: Introduction to fooocus

Similar to other popular open source AI projects like AUTOMATIC1111, Fooocus has many community-maintained forks. Below is a non-comprehensive list of all the popular ones:

- [fenneishi/Fooocus-Control](https://github.com/fenneishi/Fooocus-Control)
- [runew0lf/RuinedFooocus](https://github.com/runew0lf/RuinedFooocus)  
- [MoonRide303/Fooocus-MRE](https://github.com/MoonRide303/Fooocus-MRE)  
- [metercai/SimpleSDXL](https://github.com/metercai/SimpleSDXL)
- [pppoe/Fooocus-SAM](https://github.com/pppoe/Fooocus-SAM)

Each and every fork has their own set of improvements and new features.

## Fooocus vs Fooocus-Control

Fooocus-Control is now renamed to Fooocus-ControlNet-SDXL.
The software is a fork of Fooocus combined with [ControlNet](https://github.com/lllyasviel/ControlNet), [SDXL](https://github.com/Stability-AI/generative-models) and applied a [IP-Adapter](https://ip-adapter.github.io/) to add advanced features:
- Sketch: Use a sketch as image prompt input and generate images with elements in the sketch included.
- Depth: "Copy" the depth of one image over another.
- Pose: "Copy" the pose from image input and generate variations.
- ReColor: Repaint the color into the imput image.
- MaskInpaint: Create a mask and lets the AI do its thing in that area only.
![Fooocus-ControlNet-SDXL Sketch feature](https://github.com/fenneishi/Fooocus-ControlNet-SDXL/raw/main/asset/sketch/sketch.png)

There are more ControlNet features coming, see more at **[https://github.com/fenneishi/Fooocus-ControlNet-SDXL](https://github.com/fenneishi/Fooocus-ControlNet-SDXL)**

## Fooocus vs RuinedFooocus

RuinedFooocus is another Fooocus fork. Multiple enhancements have been added, mostly improvements on user interface.
### Customization and Personalization
- **Custom Styles and Themes**: Select from custom styles and themes in `settings/styles.csv`.
- **Custom Resolutions**: Add and select custom resolutions.
- **Performance Settings**: Customize samplers, steps, and advanced performance settings.
- **ControlNet and PowerUp**: Advanced image manipulation and custom default settings.
### User Interface Enhancements
- **Dropdown Menus**: Use dropdowns for selecting styles and resolutions.
- **Metadata Management**: Save and view full metadata for images.
- **UI Defaults**: Set and change default UI settings.
- **Readable Display**: Enhanced readability for resolution modes.
### Image Generation Options
- **Multiple Styles Application**: Apply multiple styles to a single prompt.
- **Random Prompt Generation**: Generate random prompts with a dedicated tab.
- **Batch Processing**: Process a list of prompts at once.
- **Image2Image Mode**: Transform existing images into new creations.
- **Inpainting and Evolve Features**: Fill areas and evolve images into variations.
### Workflow and Productivity
- **Drag-and-Drop Functionality**: Drag images to autofill prompts.
- **Prompt Enhancements**: Enhance prompts with loras and style directives.
- **Shortcut Keys**: Quick generation with keyboard shortcuts.
- **Cancel Button**: Terminate image generation when needed.
### Model and Format Support
- **Model Compatibility**: Supports SSD-1B Models and SDXL LCM LORA.
- **Upscaling**: Improve image resolution with upscaling options.
### Automation and Efficiency
- **Automatic Negative Prompts**: Create negative prompts automatically.
- **Automatic Triggerword Downloads**: Fetch Lora triggerwords without manual effort.
- **Generate Forever Mode**: Unlimited image generation.
### Security and Updates
- **Basic Security**: Simple username/password protection.
- **Software Upgrades**: Easy updates for xformers and torch.
### Accessibility and Notifications
- **No Browser Mode**: Use the app without launching a web browser with `--nobrowser` flag.
- **Notification System**: Audio alerts upon generation completion.
- **Metadata Viewer**: Easily inspect image metadata.

**More info: [https://github.com/runew0lf/RuinedFooocus](https://github.com/runew0lf/RuinedFooocus)**

## Fooocus vs Fooocus-MRE

Fooocus-MRE stands for "MoonRide Edition", named after its main developer/maintainer [MoonRide303](https://github.com/MoonRide303). It's got a few more features compared to the original Fooocus:
- **Image-2-Image:** Support for Image-2-Image mode, Upscaling via Image-2-Image (requires more VRAM), generate multiple images using same seed in Image-2-Image mode.
- Control-LoRA model card:  Canny Edge, Revision, Revision are supported.
- Limited support for non-SDXL models (no refiner, Control-LoRAs, Revision, inpainting, outpainting).
- Full metadata display for generated images
- Support for [FreeU](https://chenyangsi.top/FreeU/) (a method to substantially improves diffusion model sample quality at no additional cost).
- Metadata saving (JSON or embedded) and loads prompt information from JSON/image files
- Generate images forever mode
- More compact resolution & style selection
- Audio notification on generation finish
- Hotkey generation added (Ctrl+ENTER)
- Support for loading models from subfolders (ported from RuinedFooocus)
- Authentication supported, useful in `--share` mode.
- Style Iterator (iterates over selected style(s) combined with remaining styles - S1, S1 + S2, S1 + S3, S1 + S4, and so on; for comparing styles pick no initial style, and use same seed for all images).
- Limited support for non-SDXL models

**More info: [https://github.com/MoonRide303/Fooocus-MRE](https://github.com/MoonRide303/Fooocus-MRE)**

## Fooocus vs Fooocus-SAM

SAM stands for Segment-Anything Model, which primarily aims to produce high quality object masks from input prompts such as points or boxes. See the demo image and you'll know how it works:
![](https://github.com/facebookresearch/segment-anything/raw/main/assets/masks2.jpg?raw=true)
Having marked an area as a mask, we can keep or reproduce 
Fooocus-SAM adds [EfficientSAM](https://github.com/yformer/EfficientSAM), which is a compact variant of Segment-Anything Model to Fooocus. It is solely the biggest improvement of this project. Let's see what we can do with it:
![Fooocus-SAM draw the mask](https://raw.githubusercontent.com/pppoe/images-repo/main/blog/fooocus-sam/sam-mask.webp)

![Fooocus-SAM mask identified](https://raw.githubusercontent.com/pppoe/images-repo/main/blog/fooocus-sam/sam-mask-res.webp)
**More information: [https://github.com/pppoe/Fooocus-SAM](https://github.com/pppoe/Fooocus-SAM)**

## Fooocus vs SimpleSDXL

SimpleSDXL is a fork of Fooocus aimed towards Chinese users. Its main features includes:
- Chinese and English prompts supported.
- Chinese UI (texts and buttons)
- Improved image gallery browsing.
- Local model source is supported (to avoid the Chinese GFW)
- Segment-Anything Model supported for masking.

**More information: [https://github.com/metercai/SimpleSDXL](https://github.com/metercai/SimpleSDXL)**