# Privileged-GAN  

Privileged-GAN introduces a novel way to train classical GAN models, ensuring consistent and stable results. This framework combines two GANs and an autoencoder and has been trained on the MNIST dataset.

---

## Overview  

Privileged-GAN is an unsupervised learning framework based on adversarial training. It consists of:  
- **Two GANs:** A parent GAN and a child GAN.  
- **An autoencoder:** Functions as the generator for the child GAN.  

---

## Architecture  

### Version 1  
The architecture for Version 1 is shown below:  

![Version 1 Architecture](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v1/nested_GAN_with_autoencoder.png)  

**Details:**  
- The **parent GAN** starts with a generator initialized with random noise.  
- The **child GAN's generator** is an autoencoder that processes outputs from the parent GAN, making it a "Privileged-GAN."  
- Both GANs follow the classical GAN training approach: the parent GAN is trained first, and the child GAN is trained afterward, learning from the parent's successes.  

#### Training Results:  
- **With ANN:**  
  ![Training with ANN (v1)](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v1/gans_training_ANN.gif)  
- **With CNN:**  
  ![Training with CNN (v1)](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v1/gans_training_CNN.gif)  

---

### Version 2  
The architecture for Version 2 is shown below:  

![Version 2 Architecture](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v2/nested_GAN_with_autoencoder_improved.png)  

**Improvements in Version 2:**  
- Similar structure to Version 1.  
- The child GAN learns from both the **successes** and **failures** of the parent GAN, further improving its training dynamics.  

#### Training Results:  
- **With ANN:**  
  ![Training with ANN (v2)](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v2/gans_training_ANN.gif)  
- **With CNN:**  
  ![Training with CNN (v2)](https://github.com/basantbhandari/Privilaged-GAN/blob/main/Privilaged%20GAN/previlaged_GAN_v2/gans_training_CNN.gif)  

---

## Key Features  
- **Stable Training:** Incorporates a privileged learning approach for smoother convergence.  
- **Modular Framework:** Combines GANs and autoencoders for flexible training pipelines.  
- **Scalability:** Demonstrated success on MNIST, adaptable to other datasets.  

---

## Usage  

Clone the repository and follow the provided documentation to train your own Privileged-GAN models.  

```bash
git clone https://github.com/basantbhandari/Privilaged-GAN.git
cd Privileged-GAN
