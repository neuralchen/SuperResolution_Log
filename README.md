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
| Date | Architecture      | # Parameters (K) | MFLOPs | Set5 (PSNR/SSIM) | Set14 (PSNR/SSIM) | B100 (PSNR/SSIM) | Urban100 (PSNR/SSIM) | Manga109 (PSNR/SSIM) |
| -------- | ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
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
| 7.8 | RLFN inception C (kill at 670 epoch) | - | - | 32.03 / 0.8940 | 28.28 / 0.7828 | 27.57 / 0.7369 | 25.97 /  0.7840 |
| 7.8 | RLFN inception A & cat ESA  | - | - | 32.08  / 0.8945| 28.27 / 0.7826 | 27.60 / 0.7371 | 26.09 / 0.7867 |
| 7.8 | RLFN inception A & cat inv  | - | - | 32.06 / 0.8944 | 28.28 / 0.7826 | 27.59 / 0.7371 | 26.08 / 0.7866 |
| 7.10 | RLFN inception A & cat ESA with prelu 52 channel | - | - | 32.13 / 0.8949 | 28.28 / 0.7831 | 27.60 / 0.7375 | 26.11 / 0.7879 |
| 7.10 | RLFN inception A & cat ESA with 64 channel | - | - | 32.17 / 0.8957 | 28.29 / 0.7834 | 27.64 / 0.7379 | 26.16 /0.7889 |
| 7.11 | RLFN inception A & cat ESA 8 layer | - | - | 32.20 / 0.8962 | 28.31 / 0.7838 | 27.62 / 0.7383 | 26.19 / 0.7901 |
| 7.11 | RLFN inception A & cat ESA 10 layer| - | - | 32.18 / 0.8960 | 28.33 / 0.7842 | 27.63 / 0.7388 | 26.27 / 0.7925 |
| 7.11 | RLFN inception A & cat ESA 12 layer | - | - | 32.22 / 0.8958 | 28.37 / 0.7841 | 27.64 / 0.7386 |26.27 / 0.7920 |
| 7.11 | RLFN inception A & cat ESA 16 layer | - | - | 32.15 / 0.8954 | 28.32 / 0.7842 | 27.61 / 0.7383 | 26.14 / 0.7886 |
| 7.11 | RLFN inception A & cat ESA cat attn 6 layer | - | - | 32.26 / 0.8965 | 28.34 / 0.7840 | 27.64 / 0.7391 |26.25 / 0.7911|
| -------- | ----------------- | ------------ | ------ | -------------------------- | -------------------------- | -------------------------- | -------------------------- | -------------------------- |
| -- | RLFN | 543K | - | 32.24 / 0.8952 | 28.62 / 0.7813 | 27.60 / 0.7364 | 26.17 / 0.7877 |
| -- | RLFN we run | 543K | - | 32.08 / - | 28.26 / - | 27.59 / - | 26.12 / - |
| 7.31 | KernelFormer (919 epoch) Eval@Matlab| 367K | - | 32.31 / 0.8964 | 28.67 / 0.7832 | 27.63 / 0.7380 | 26.22 / 0.7899 | 30.60 / 0.9100 |
| 7.29 | ESRT | 751K | - | 32.19 / 0.8947 | 28.69 / 0.7833 | 27.69 / 0.7379 | 26.39 / 0.7962 | 30.75 / 0.9100 |
| 7.31 | KernelFormer (724 epoch) Eval@Matlab| 671K | - | 32.35 / 0.8972 | 28.78 / 0.7858 | 27.68 / 0.7400 | 26.39 / 0.7958 | 30.86 / 0.9136 |
| 8.1 | KernelFormer w Rep (506 epoch) Eval@Matlab| 671K | - | 32.38 / 0.8974 | 28.76 / 0.7855 | 27.67 / 0.7398 | 26.41 / 0.7965 | 30.82 / 0.9131 |
