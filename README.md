# SuperResolution_Log
 
# Training_logs

### Training Setting:

- batch size: 64
- epochs: 1000
- LR decay strategy: half at [250, 500, 750, 1000]
- Loss: L1 loss
- DIV2K
- Data augmentation: Random rotation, random vertical flip, random horizontal flip

### X4
| Architecture      | # Parameters (K) | MFLOPs | Set5 (PSNR/SSIM) | Set14 (PSNR/SSIM) | B100 (PSNR/SSIM) | Urban100 (PSNR/SSIM) |
| ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| ECBSR | 603 | - | 31.92 / 0.8946 | 28.34 / 0.7817 | 27.48 / 0.7393 | 25.81 / 0.7773 |
| RLFN | 543 | - | 32.24 / 0.8952 | 28.62 / 0.7813 | 27.60 / 0.7364 | 26.17 / 0.7877 |
| 07/03 | - | - | 31.98 / 0.8917 | 28.45 / 0.7786 | 27.50 / 0.7338 | 25.77 / 0.7756 |


### X4 from hang
| Architecture      | # Parameters (K) | MFLOPs | Set5 (PSNR/SSIM) | Set14 (PSNR/SSIM) | B100 (PSNR/SSIM) | Urban100 (PSNR/SSIM) |
| ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| ECBSR | 603 | - | 31.92 / 0.8946 | 28.34 / 0.7817 | 27.48 / 0.7393 | 25.81 / 0.7773 |
| RLFN | 543 | - | 32.24 / 0.8952 | 28.62 / 0.7813 | 27.60 / 0.7364 | 26.17 / 0.7877 |
| 07/03 | - | - | 31.98 / 0.8917 | 28.45 / 0.7786 | 27.50 / 0.7338 | 25.77 / 0.7756 |
