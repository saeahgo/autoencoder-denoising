# autoencoder-denoising

## Intro & Hypothesis
Denoising autoencoders are a type of neural network used to remove noise from images by learning robust representations. In this assignment, we evaluate the performance of a denoising autoencoder under different levels of noise. Specifically, we assess the model's effectiveness using Peak Signal-to-Noise Ratio (PSNR) and Structural Similarity Index (SSIM) as objective quality metrics.

In this experiment, we test five different noise levels: 10%, 20%, 30%, 40%, and 50%. The training phase maintains a constant corruption ratio of 10%. We hypothesize that:

- Denoised images with a lower noise percentage will closely resemble the original clean images.
- As the noise level increases, the quality of the denoised images will degrade, making them less clear.
- Both PSNR and SSIM values will be higher for lower noise levels and will gradually decrease as noise levels increase.

## Results
Since there are many images in this section, all of the original, noised, and denoised images have been placed in the Supplement section.

To quantify the model’s performance, we compute the average PSNR and SSIM values for each noise level. The results are summarized in the table below.

| Noise Level | Average PSNR (dB) | Average SSIM |
|------------|------------------|--------------|
| 10%        | 21.46            | 0.8929       |
| 20%        | 18.67            | 0.8283       |
| 30%        | 17.27            | 0.7635       |
| 40%        | 15.92            | 0.6997       |
| 50%        | 15.40            | 0.6609       |

Figures illustrate the qualitative results, showing denoised images for each noise level.

## Discussion & Conclusion
As observed in the results, at a noise level of 10%, the denoised images closely resemble the original clean images, demonstrating effective denoising performance. As the noise level increases, the model struggles to reconstruct the images accurately. At higher noise levels, the denoised images show noticeable distortion and residual noise, making it difficult to recognize the digits.

The average PSNR and SSIM results also support our hypothesis. At a 10% noise level, the denoised images are similar to the original images, as indicated by a high PSNR (21.46 dB) and SSIM (0.8929). As the noise level increases, both metrics gradually decline, confirming that the denoised images are different from the original images.

The decreasing PSNR values suggest that the denoised images contain more distortion at higher noise levels. Similarly, the decline in SSIM values indicates reduced structural similarity. At 50% noise, the denoised images struggle to recover meaningful details, making digit recognition more challenging.

This experiment demonstrates that a denoising autoencoder effectively removes noise when the noise level is low. However, as the noise level increases, the model's performance decreases, as evidenced by decreasing PSNR and SSIM values.
