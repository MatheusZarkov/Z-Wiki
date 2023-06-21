---
{"dg-publish":true,"permalink":"/zettelkasten/3000-ai/stable-diffusion/tutorials/como-fazer-meu-proprio-modelo-de-inpainting/","created":"","updated":""}
---

Making your own inpainting model is very simple:

-   Go to Checkpoint Merger
-   Select "`Add Difference`"
-   Set "`Multiplier`" to `1.0`
-   Set "A" to the official inpaint model (SD-v1.5-Inpainting) [https://huggingface.co/runwayml/stable-diffusion-inpainting/tree/main](https://huggingface.co/runwayml/stable-diffusion-inpainting/tree/main "https://huggingface.co/runwayml/stable-diffusion-inpainting/tree/main")
-   Set "B" to your model
-   Set "C" to the standard base model (SD-v1.5)
-   Set name as whatever you want, probably (your model)\_inpainting
-   Set other values as preferred, ie probably select "Safetensors" and "Save as float16"
-   Hit merge
-   Use your new model in img2img inpainting tab

The way this works is it literally just takes the inpainting model, and copies over your model's unique data to it. Notice that the formula is `A + (B - C)`, which you can interpret as equivalent to `(A - C) + B`. Because 'A' is 1.5-inpaint and 'C' is 1.5, `A - C` is inpainting logic and nothing more. so the formula is `(Inpainting logic) + (Your Model)`. (editado)


![](https://cdn.discordapp.com/attachments/1107819932726612068/1107819932885987400/image.png)