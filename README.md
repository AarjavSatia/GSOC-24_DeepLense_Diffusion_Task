# GSOC-24 DeepLense Diffusion Task

![Generated Lense samples](https://github.com/AarjavSatia/GSOC-24_DeepLense_Diffusion_Task/blob/main/diffusion_samples/diffusion_sample-1.png?raw=true)

<p>1) Denoising Diffusion Probalistic Model (DDPM) /cite{} is used for all experimentations, the code takes from /cite{} and /cite{}.</p>
<p>2) For the forward process Sigmoid Beta Scheduling is used to create beta timesteps as it gives better results on images greater than 64x64 /cite{https://arxiv.org/abs/2212.11972} </p>
<p>3) DDIM sampling method /cite{} is used for sampling as it is decreases the time taken for sampling thus allowing for calculation of FID on large number of samples giving a more robust FID score.</p>
<p>4) Exponential Moving Average /cite{} is used for updating the weights which enables smoother training make the model more stable. </p>
<p>5) U-Net model takes from the original Open-AI architecture /cite{}, but uses a scaled down version with fewer parameters due to unavailability of large amount of computing resources.Flash attention /cite{} is used in the attention layers to increase training speed.</p>
<p>6)FID score is calculated by generating 2,000 samples at 250 sampling steps. Final FID value comes out to be 12.3997.</p>

### Further Modifications and Ideas:
<p>1) Given a large dataset (>200,000 images) U-Net backbone can be replaced with a Transformer backbone to create a Diffusion Transformer architecture /cite{}.</p>
<p>2) Vector-Quantized Variational Auto-Encoder's (VQ-VAE) /cite{} Encoder and Decoder can be used to compress the images to a Lantent space and diffusion process can be applied on that latent space so as to reduce the computational complexity.</p>
<p>3) Given more information, U-Net can be conditioned on various properties of strong lensing images (like their substructure and various other parameters about their vortex, subhalo etc.) to generate accurate and specific lensing images.</p>

### References:
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
<p></p>
