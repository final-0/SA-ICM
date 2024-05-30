<div align="center">

### Image Coding for Machines with Edge Information Learning <br>
### Using Segment Anything

---

### [SA-ICM](https://arxiv.org/abs/2403.04173)
</div>

---
---

This is the official implementation of the following paper.<br>
<br>
・Image Coding for Machines with Edge Information Learning Using Segment Anything
([arXiv](https://arxiv.org/abs/2403.04173))<br>

---

<div align="center">
  
### Installation
</div>

1. Clone this repository from GitHub.
```
git clone https://github.com/final-0/SA-ICM.git
```
2. Change the current directory to the "SA-ICM" folder.
```
cd SA-ICM/
```
3. Install the required dependencies in the current directory.

```
pip3 install -r requirements.txt 
```

---

<div align="center">

### Recommended Specs
</div>

For testing only, a GPU with about 11GB of memory is sufficient. (e.g. 1080ti, 2080ti)

---

<div align="center">
  
### Usage
</div>

###  image compression

Download [model weights](https://drive.google.com/drive/folders/1J7rsrEFn20zLginAcyDzY5DdCMbYamgC?usp=drive_link). 
You can obtain "icm_78.pth.tar" and "icm_93.pth.tar" from this link. 
These weights can be used by placing them in the "param" folder.<br>
``` 
param ---- param_details.txt
       |-- icm_78.pth.tar
       |-- icm_93.pth.tar 
```

If you want to compress images for "Machines" with , run the following command :
``` 
python3 coding_m.py --checkpoint param/icm_78.pth.tar --input image/input
```
``` 
python3 coding_m.py --checkpoint param/icm_93.pth.tar --input image/input
```

Add “--real” to the command to obtain a bit-stream:
``` 
python3 coding_m.py --checkpoint param/icm_78.pth.tar --input image/input --real
```
```
python3 coding_m.py --checkpoint param/icm_93.pth.tar --input image/input --real
```

Compressed images will be saved in the folder "output_icm_78" or "output_icm_93".
``` 
image ---- input
       |-- output_icm_78
       |-- output_icm_93 
```

###  object detection ([yolov5](https://github.com/ultralytics/yolov5))

Download [model weights](https://drive.google.com/drive/folders/1UZ4VyDeS4XyvPMbWQzqz4p3cQq3lzOKU?usp=drive_link).
You can obtain "yolov5_78.pt" and "yolov5_93.pt" from this link. 
These weights can be used by placing them in the "param" folder.<br>
``` 
param ---- param_details.txt
       |-- icm_78.pth.tar
       |-- icm_93.pth.tar
       |-- yolov5_78.pt
       |-- yolov5_93.pt
```
<br>

🚧
