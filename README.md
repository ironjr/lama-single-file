# 🦙 Simple-lama

Your LaMa inpainter in a single file.

### Prerequisite

```bash
pip install numpy torch
```
Of course you can install PyTorch from the [official page](https://pytorch.org/get-started/locally/).

### Usage

1. Intall stuffs: `pip install numpy torch` will do.
2. Download only a single file `lama.py` to your favorite location.
    ```bash
    wget https://raw.githubusercontent.com/ironjr/simple-lama/main/lama.py
    ```
3. Prepare your image: Numpy array of size `(H, W, 3)` and scale `[0, 255]`.
4. Load LaMa in one-(two-)liner.
    ```python
    from lama import LaMa
    
    model = LaMa('cuda:0')
    ```
5. Inpaint in one-liner.
   ```python
   inpainted = model(masked, mask)
   ```

Done!

### Reference

This project is heavily inspired by an awesome project [Lama Cleaner](https://github.com/Sanster/lama-cleaner)!
In addition, if you find this repository useful, consider visiting the [original project page](https://github.com/advimman/lama) of LaMa!

```
@article{suvorov2021resolution,
  title={Resolution-robust Large Mask Inpainting with Fourier Convolutions},
  author={Suvorov, Roman and Logacheva, Elizaveta and Mashikhin, Anton and Remizova, Anastasia and Ashukha, Arsenii and Silvestrov, Aleksei and Kong, Naejin and Goka, Harshith and Park, Kiwoong and Lempitsky, Victor},
  journal={arXiv preprint arXiv:2109.07161},
  year={2021}
}
```
