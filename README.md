This repository contains the final project for the course:

# [Python for (open) Neuroscience](https://github.com/vigji/python-cimec)

taught by [Luigi Petrucco](https://github.com/vigji) at the Doctoral school in [Cognitive and Brain Sciences](https://www.unitn.it/drcimec/), Center for Mind/Brain Sciences (CIMeC), University of Trento. 

---

The project consists of a simple convolutional neural network (CNN) for image recognition. It is structured across three files:
- `matteos_module.py`: a custom Python module that contains classes and functions to define, train, validate, test, and inspect the CNN 
- `master_script.py`: instantiates and calls `matteos_module.py`'s classes and functions in the right order
- `config.py`: a set of dictionaries that contain important hyperparameters to control the structure and behaviour of the CNN
- `visual_cnn_notebook.ipynb`: a notebook version of the project that collects all the above in a single file

# **Dependencies:**

- [NumPy](https://github.com/numpy/numpy)
- [Matplotlib](https://github.com/matplotlib/matplotlib)
- [PyTorch](https://github.com/pytorch/pytorch) for dataset management and network definition, training, and testing 
- [torchvision](https://github.com/pytorch/vision) for computer vision-specific functionalities

---

The CNN is trained, validated and tested on the [MNIST dataset of handwritten digits](https://en.wikipedia.org/wiki/MNIST_database), a standard (actually, overused) benchmark for machine learning models. However, it works on virtually any other vision dataset with little-to-no modifications.

Training and validating CNNs can be computationally intensive. For this reason, PyTorch is geared towards parallel computing on [CUDA-enabled GPUs](https://en.wikipedia.org/wiki/CUDA). If you have one on your machine, the model will run there. If you don't, it will run on your CPU. 
Training on CPU might take too long. To avoid this, you can run `visual_cnn_notebook.ipynb` on Google Colab. This will provide the same results as running the three `.py` files locally, as these are just a better organized, modular version of the `.ipynb`. However, training will be significantly shorter because it will be run on Google's CUDA-enabled GPUs.

You can check if your GPU is CUDA-enabled [here](https://nvidia.custhelp.com/app/answers/detail/a_id/2137/~/which-gpus-support-cuda%3F). TL;DR: it must be NVIDIA.

---

# **DISCLAIMER**:

This CNN was first submitted as assignment for the course [Neural Networks & Deep Learning](https://didattica.unipd.it/off/2019/LM/IN/IN2371/005PD/INP9086459/N0) (NNDL) taught at the University of Padova (Fall 2019 iteration). 
- The three `.py` files represent a major refactoring of the code submitted for that assignment. The refactoring was geared towards modularity and reusability
- The `.ipynb` is the exact same file that was submitted for the NNDL assignment. As mentioned above, it is provided for the sole purpose of shortening computation time by leveraging Google Colab's capabilities (if needed)
