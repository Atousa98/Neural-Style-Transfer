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

To run this application locally, you must have a Python environment configured with the required deep learning and image processing libraries. The core dependencies include TensorFlow for the neural network computations, NumPy for tensor manipulations, and Pillow for image encoding and decoding. Ensure these are installed via your preferred package manager.

Once the environment is prepared, place your target images in the root directory. Rename the base image to `content.jpg` and your artistic reference to `style.jpg`. Execute the `style_transfer.py` script. The network will perform 3000 optimization steps, calculating the gradient descent to minimize both content and style loss simultaneously. The final rendered artwork will be saved automatically to the directory as `Final_Result.jfif`.