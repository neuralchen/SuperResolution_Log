# SuperResolution_Log
 
# Training_logs
 
# Mobilenet V2

### Mobilenet V2 Setting:

- batch size: 64
- epochs: 1000
- LR decay strategy: 
- Loss: L1 loss
- DIV2K
- Data 

### X4
| Architecture      | # Parameters (K) | MFLOPs | Set5 (PSNR/SSIM) | Set14 (PSNR/SSIM) | B100 (PSNR/SSIM) | Urban100 (PSNR/SSIM) |
| ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| ECBSR | 603 | - | 31.92 / 0.8946 | 28.34 / 0.7817 | 27.48 / 0.7393 | 25.81 / 0.7773 |
| RLFN | - | - | 32.24 / 0.8952 | 28.62 / 0.7813 | 27.60 / 0.7364 | 26.17 / 0.7877 |
| 07/03 | - | - | 31.87 / 0.8913 | 28.09 / 0.7786 | 27.50 / 0.7338 | 25.76 / 0.7764 |