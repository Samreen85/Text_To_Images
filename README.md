# AI Image Generation & Editing with DALL-E

Generates images from text descriptions and edits existing images using masked inpainting, via OpenAI's DALL-E models.

## Functionality
1. **Text-to-Image** — generates a new image from a text prompt using `dall-e-3`.
2. **Mask Creation** — creates a mask over a region of an existing image (marking the area to be edited).
3. **Masked Image Editing** — edits the masked region of an existing image based on a new text prompt, using `dall-e-2`'s inpainting endpoint.

## Setup

1. Install the OpenAI SDK and Pillow:
   ```
   pip install openai pillow
   ```
2. Set your OpenAI API key (as an environment variable or in the notebook).

## Usage

Run `Generate_Image.ipynb`:
- **Cell 1** — generates an image from a text prompt (e.g., "a white siamese cat") and returns the image URL.
- **Cell 2** — loads `Images/original.png` and creates a mask marking the region to edit.
- **Cell 3** — sends the original image, mask, and an edit prompt to `dall-e-2`'s edit endpoint to regenerate just the masked area.

Sample images (`original.png`, `mask.png`) are included in the `Images/` folder.
