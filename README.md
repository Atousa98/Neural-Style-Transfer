# Neural Style Transfer: Bridging Traditional Art and Digital Media

This repository contains a high-resolution implementation of Neural Style Transfer using TensorFlow and the VGG19 deep learning architecture. The primary objective of this project is to explore the intersection of traditional painting techniques, such as heavy oil brushstrokes and impasto, with algorithmic digital rendering. By manipulating second-order statistics through Gram matrices, the network effectively superimposes the profound textures of classical art onto standard digital content.

The architecture strictly avoids excessive total variation loss optimization. This design choice was made to intentionally retain the raw, chaotic, and authentic textures inherent to physical painting mediums, rather than producing an overly smoothed or artificial digital filter. The algorithm prioritizes artistic fidelity and complex color blending over flat gradient approximations.

## Visual Results

The demonstration below showcases the algorithmic translation of Leonardo da Vinci's classic portrait into the post-impressionist vocabulary of Vincent van Gogh. 

### Original Content
<img src="https://github.com/Atousa98/Neural-Style-Transfer/releases/download/v1.0.0/content.jpg" width="600" alt="Content Image">

### Style Reference
<img src="https://github.com/Atousa98/Neural-Style-Transfer/releases/download/v2.0.0/style.jpg" width="600" alt="Style Image">

### Stylized Output
<img src="https://github.com/Atousa98/Neural-Style-Transfer/releases/download/v3.0.0/Final_Result.jfif" width="600" alt="Final Result">

## Setup and Execution

### Option 1: Running in Google Colab (Recommended for quick testing)
If you are running this project inside Google Colab to leverage free GPU acceleration, you can easily handle image uploads and directly display the output inside your notebook.

1. **Upload your images:** Create a cell at the top of your notebook, paste the following code, and execute it to upload your target images. Make sure to rename your core image to `content.jpg` and your artistic reference to `style.jpg` (or update the file paths inside `style_transfer.py`).
```python
from google.colab import files

uploaded = files.upload()
```

2. **Run the core script:** Execute the main `style_transfer.py` script to begin the 3000 optimization steps.

3. **Display the result:** To visualize the generated artwork directly beneath your notebook cells without downloading it first, run this snippet:
```python
from IPython.display import Image, display

display(Image('Final_Result.jfif'))
```

### Option 2: Running Locally (Desktop IDE)
To run this application locally on your machine:

1. Ensure your local environment is configured with the required dependencies: `pip install tensorflow numpy pillow`.
2. Place your base image as `content.jpg` and your artistic style reference as `style.jpg` directly in the root directory alongside the script.
3. Execute the python file via your terminal:
   ```bash
   python style_transfer.py
   ```
4. The network will compute the gradient descent and automatically save the high-resolution output artwork to the root directory as `Final_Result.jfif`.
