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
| Date | Architecture      | # Parameters (K) | MFLOPs | Set5 (PSNR/SSIM) | Set14 (PSNR/SSIM) | B100 (PSNR/SSIM) | Urban100 (PSNR/SSIM) |
| -------- | ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| -- | ECBSR | 603 | - | 31.92 / 0.8946 | 28.34 / 0.7817 | 27.48 / 0.7393 | 25.81 / 0.7773 |
| -- | RLFN | 543 | - | 32.24 / 0.8952 | 28.62 / 0.7813 | 27.60 / 0.7364 | 26.17 / 0.7877 |
| -- | RLFN we run | - | - | 32.08 / - | 28.26 / - | 27.59 / - | 26.12 / - |
| -- | RLFN wo ESA | - | - | 31.86 / - | 28.19 / - | 27.54 / - | 25.85 / - |
| -- | VDSR | - | - | 19.13 / - | 18.85 / - | 20.40 / - | 17.66 / - |
| -- | VDSR w 4ESA | - | - | 31.98 / - | 28.19 / - | 27.55 / - | 25.96 / - |
| -- | VDSR w 8ESA | - | - | 32.05 / - | 28.23 / - | 27.58 / - | 26.01 / - |
| 7.7 | VDSR w 8ESA res  | - | - | 32.06 / 0.8944 | 28.26 / 0.7823 | 27.59 / 0.7370 | 26.06 / 0.7863 |
| 7.7 | VDSR w 8ESA res & c5| - | - | 32.13 / 0.8949 | 28.29 / 0.7828 | 27.60 / 0.7376 | 26.06 / 0.7867 |
| 7.7 | RLFN inception| - | - | 31.91 / 0.8914 | 28.11 / 0.7792 | 27.52 / 0.7345 | 25.88 / 0.7797 |
| 7.7 | RLFN inception A| - | - | 32.07 / 0.8943 | 28.28 / 0.7824 | 27.58 / 0.7371 | 26.05 / 0.7861 |
| 7.8 | RLFN inception C  | - | - |  /  |  /  |  /  | 25.96 /  0.7832 |
| 7.8 | RLFN inception A & cat ESA  | - | - | 32.09  /  | 28.24 /  | 27.59 /  | 26.08 / 0.7864 |
| 7.8 | RLFN inception A & cat inv  | - | - |  /  |  /  |  /  | 26.05 / 0.7860 |
