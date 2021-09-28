# RIFE
Video Frame Interpolation
 ## Installation
 For installing, follow these intructions
 ```
numpy>=1.16
tqdm>=4.35.0
sk-video>=1.1.10
torch>=1.3.0
opencv-python>=4.1.2
moviepy>=1.0.3
 ```
 
## Run
### Video Frame Interpolation

You can use our demo video or your own video.
 ```
 python3 inference_video.py --exp=1 --video=video.mp4 --scale=0.5 --fps=60
 ```
 (If your video has very high resolution such as 4K, we recommend set --scale=0.5 (default 1.0).
 ### Image Interpolation
 ```
 python3 inference_img.py --img img0.png img1.png --exp=4
  ```
  
## Training and Reproduction

Download Vimeo90K dataset.
 ```
 python3 -m torch.distributed.launch --nproc_per_node=4 train.py --world_size=4
  ```
