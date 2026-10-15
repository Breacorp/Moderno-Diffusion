## Guía de Uso de Moderno Diffusion

### Instalación

Al iniciar la aplicación por primera vez, Moderno Diffusion descargará los datos y modelos base para la generación de imágenes local.

### Actualizaciones

Moderno Diffusion recibe actualizaciones periódicas para añadir funciones y mejorar el rendimiento de inferencia. Tus modelos e historial se mantendrán intactos.

## Generating images

Depending on settings and available computing power it may take a few seconds to a few minutes to generate an image. Image generation may be aborted by pressing the stop button. Use the "save image" link to save the image to a location of your choice.

Clicking on an image opens a separate window displaying the image in full size.

### Text to image
<img width="500" alt="Image of text to image" src="https://user-images.githubusercontent.com/105890749/198898577-1852a780-47b6-4d82-98b7-715b0386e44d.png">

The text to image function is used to create an image based on text input only.

To create an image, simply enter a prompt and press _generate_.

* The **Prompt ideas** button opens a web page where you can browse a gallery for finding useful prompts.
* The **Styles** button provides a palette of often-used terms to add to the prompt.
* The **Options** buttons gives the following options:
  * Num images: The number of images to generate.
  * Image height/width: Sets the dimensions of the image. Note that Stable Diffusion is trained on 512 x 512 (the default setting). Other dimensions may give less good result and take more time.
  * Steps: This corresponds to how many steps are used to build information about the image. Setting to a low number gives faster image generation, and may be useful while exploring different prompts.
  * Batch size: This tells Moderno Diffusion to generate multiple images at a time. New batches of images will be created until "num images" have been created. (Just increasing _num images_ is usually a better option.)
  * Guidance scale: This kind of corresponds to how closely Stable Diffusion should stick to the prompt. Higher value means more strict interpretation.
  * Seed: A number between 0 and 4,294,967,295 that is used as starting point for the image generation. If the same seed is used with the same prompt and the same settings (except *steps*, which may vary), the same image will be generated. If left empty, a random seed will be used.

#### Negative prompt
<img width="300" alt="Image of Negative Prompt" src="https://user-images.githubusercontent.com/105890749/198899943-35b66e59-4a89-4770-b939-fb1d8de541ef.png">

Enabling the negative prompt option allows adding descriptions of things to avoid including in the image, in combination with the standard prompt. As with the standard prompt the model's understanding of the negative prompt is not perfect, so things described in the negative prompt may still occur in the image.

### Image to image
<img width="500" alt="Image of Image to image" src="https://user-images.githubusercontent.com/105890749/198898970-64efd0e5-4e10-433a-928c-7a6cd95d1a4f.png">

The image to image function can be used to create an image based on a starting image (often a very rough sketch) combined with a text description.

Click on the left pane to upload a sketch starting image (only png supported). Add a prompt description of the desired output and press _generate_. The generated image will be 512 x 512 pixels.

* The **Options** buttons gives the following options:
  * Input strength: This tells Moderno Diffusion how closely to stick to the sketch input image. For rough sketches you normally want a low value.
  * Num images: The number of images to generate.
  * Steps: This corresponds to how many steps are used to build the image information. Setting to a low number gives faster image generation, and may be useful while exploring different prompts.
  * Seed: A number between 0 and 4,294,967,295 that is used as starting point for the image generation. If the same seed is used with the same image, the same prompt and the same settings (except *steps*, which may vary), the same image will be generated. If left empty, a random seed will be used.

### Inpainting
<img width="500" alt="Image of Inpainting" src="https://user-images.githubusercontent.com/105890749/198899315-3c905257-192f-44f2-9bdf-02e454c276de.png">

The inpainting function is used to replace/repaint parts of an image, for example to add a bow tie to a cat or removing a car from a photo of a street.

To use the inpainting functions, add an image and scribble on it to mask the area you wish Moderno Diffusion to re-paint for you. You will usually get a better result if you mask a significantly larger area than the part you actually want to change. Right now, the inpainting model works with a max height of 512 pixels, so any images bigger than that will be scaled down proportionally to fit the model.


### Outpainting
<img width="500" alt="Picture of Outpainting" src="https://user-images.githubusercontent.com/105890749/198899711-05bca2fb-04ca-4bc4-9d7c-e276bf5db9d2.png">

The outpainting function is used to expand an image to a larger area.

To use the outpainting functions, add an image and move the 512×512 frame to a place where you want to expand the image, and provide a text prompt. The process may be repeated to expand the image several times and in different directions.


## History
<img width="500" alt="Image of History" src="https://user-images.githubusercontent.com/105890749/198899465-8d85d26d-5f28-4965-accc-e3fbba80c6dd.png">

The **History** tab show previously generated images along with prompts and settings (including seed).

## Sharing images
<img width="500" alt="Image of sharing images" src="https://user-images.githubusercontent.com/105890749/198900052-25632642-c46c-4163-9dee-9758ec6fa06a.png">

Sharing images uploads images along with prompt and settings to arthub.ai. Before uploading you may select which of the images in a batch to upload. You are required to create an account to share images.

## Custom models

Moderno Diffusion supports the ability to add and use custom models (.ckpt / .safetensors / .tdict).

### Importing custom models
Once you have found and downloaded the model file you wish to use, you can import it into Moderno Diffusion from the Settings menu ("Add New Model").

### Soporte y Comunidad
Para consultas técnicas y asistencia:
* Web: [https://moderno.com.ar](https://moderno.com.ar)
* Centro de Ayuda: [https://moderno.com.ar/ayuda](https://moderno.com.ar/ayuda)
* Contacto directo: `contacto@moderno.com.ar`
