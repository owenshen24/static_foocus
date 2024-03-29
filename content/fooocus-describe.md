Title: Fooocus Describe
Date: 2024-01-06 10:20
Modified: 2024-01-06 10:20
Slug: describe-command
Authors: FooocusFan
Summary: Fooocus Describe

In Midjourney, the `/describe` command analyzes the uploaded image and generates text prompts inspired by it. Since version 2.1.831, Fooocus has added a similar tool.

In order to access it, check the **Input Image** checkbox.

![input image](/images/input_image.png)

Next, switch to **Describe** tab and upload an image either by drag-and-drop or click-to-upload. Now click **Describe this Image into Prompt**.

![Describe this Image into Prompt](/images/describe.png)

The tool works pretty well with anime input, too.

![Describe this anime into Prompt](/images/describe_anime.png)

## Fooocus describe vs Midjourney `/describe`

Just like Midjourney `/describe`, you can get multiple description by clicking **Describe this Image into Prompt** multiple times. However, it only works in **Photograph** mode.

If you're also a developer, you should know that there are [a few differences between Fooocus Describe and other open-source software (which uses CLIP Interrogator)](https://github.com/lllyasviel/Fooocus/discussions/1363):

1. Fooocus Describe is less likely to yield repeated failure cases than CLIP Interrogator, like “in a hat, in a hat, in a hat, in a hat, in a hat, in a hat”.
2. Fooocus Describe will not randomly add artist names and website names into your prompt. (Most CLIP Interrogator implementation will add nearly random artist names and noisy website names)
3. Fooocus Describe is based on [BLIP](https://github.com/salesforce/BLIP) like CLIP Interrogator, but the model choice is based on computation power of most devices.
4. The Anime/Art Describe is based on WD-Tagger-V2 best model. That's why you'll see a different kind of description generated in Photograph and Anime/Art modes.