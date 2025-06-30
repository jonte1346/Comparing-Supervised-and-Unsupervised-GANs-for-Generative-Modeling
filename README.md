
# YalıGAN: Generating Ottoman Waterfront Architecture with GANs and Diffusion

This project explores generative modeling for architectural heritage, focusing on Istanbul’s historic **Yalı houses**. Using a combination of supervised, unsupervised, and fine-tuned diffusion models, we aim to generate high-quality façade imagery that reflects the stylistic features of traditional Ottoman waterfront architecture.

## 📂 Project Structure

- **Pix2Pix / Pix2PixHD** (Supervised GANs)
- **Wasserstein SAGAN-GP** (Unsupervised GAN)
- **Stable Diffusion** (Fine-tuned for Yalı imagery)
- **Evaluation Metrics**: SSIM, FID, Inception Score, CLIP Score
- **Preprocessing**: Background removal, augmentation, mask generation

## 📊 Evaluation Summary

| Model                          | FID     | Inception Score | CLIP Score | SSIM    |
|-------------------------------|---------|------------------|------------|---------|
| Pix2PixHD (Supervised)        | 72.90   | -                | 0.2262     | 0.8207  |
| SAGAN-WGAN-GP (Unsupervised)  | 306.28  | 2.93 ± 0.21      | 0.2270     | -       |
| Stable Diffusion (Fine-Tuned) | 210.18  | 1.36 ± 0.06      | 0.2485     | -       |

## 🧠 Technologies Used

- PyTorch
- torchvision / torchmetrics
- OpenAI CLIP
- Segment Anything (SAM)
- rembg / U-2-Net
- Stable Diffusion + LoRA (fine-tuning)

## 🛠️ How to Run

1. Clone the repository and open in Google Colab or local Jupyter environment.
2. Prepare the dataset: background removal, resizing, and augmentation.
3. Train models using the provided `.ipynb` notebooks.
4. Evaluate performance with provided metrics (FID, SSIM, CLIP).
5. Compare generated outputs and save best checkpoints.

## 📁 Dataset

- 538 manually curated façade images of Yalı houses.
- Augmented to 1,646 samples.
- Binary masks generated via SAM for supervised models.

## 🎯 Objective

To compare the performance of supervised (Pix2Pix), unsupervised (W-SAGAN-GP), and fine-tuned (Stable Diffusion) models on generating semantically and structurally accurate architectural imagery.

## 📄 Authors

- **Jonathan Giegold** (Computer Science MSc, Lund University)
- **Biçem Kaya** (Architectural Design MSc, Istanbul Technical University)

---

*This project was conducted as part of MBL 559E — Machine Learning for Architectural Design, Spring 2024-25.*
