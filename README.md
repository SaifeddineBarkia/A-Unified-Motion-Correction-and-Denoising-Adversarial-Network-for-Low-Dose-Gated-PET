# MDPET — Unified Motion Correction & Denoising for Low-Dose Gated PET (paper study)

> MVA (ENS Paris-Saclay) · Deep Learning for Medical Imaging (2022)
> **Team:** **Saifeddine Barkia**, Gonzalo Reinoso

A critical study of *MDPET: A Unified Motion Correction and Denoising Adversarial Network for Low-Dose Gated PET* (Zhou et al., IEEE TMI 2021), written in MIDL paper format.

## Why it matters

Low-dose PET reduces radiation exposure for patients and staff, but it makes images noisier. Breathing during the 10–20 minute scan also blurs them. Earlier methods treat **motion estimation** and **denoising** separately, and noise in low-dose gated images corrupts the motion estimate.

## What the report covers

- **Architecture:** a Temporal Siamese Pyramid Network (shared-weight Siamese pyramids plus a bidirectional ConvLSTM) estimates the deformation between each respiratory gate and a reference gate. The gates are then registered and averaged, and a GAN denoiser (generator plus discriminator) restores standard-dose quality.
- **Problem formulation** and the training losses.
- **Analysis** of the reported gains in motion estimation and denoising, with limitations and possible extensions.

📄 [Full report (PDF)](./DLMI_BARKIA_REINOSO.pdf)

**Topics:** medical imaging · PET · image registration · denoising · GANs
