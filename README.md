# CogVideoX

![](./overview.png)

This code contains CogVideoX and the evaluation metric Vbench.
## Usage: 
For generating video.
 First download the pretrain model from huggingface https://huggingface.co/spaces/THUDM/CogVideoX-5B-Space
 Then run cli_demo.py under inference in CogVideoX-main with prompt.
```matlab
python cli_demo.py --prompt "A girl riding a bike." --model_path THUDM/CogVideoX-5b
```

For evaluating human perceptions, using prompt list under prompts in Vbench_master to generate videos.
Then using the video generated for evaluation
```matlab
python evaluate.py \
    --dimension $DIMENSION \
    --videos_path /path/to/folder_or_video/ \
    --mode=custom_input
```

## Citation
```bib
@misc{yang2024cogvideoxtexttovideodiffusionmodels,
      title={CogVideoX: Text-to-Video Diffusion Models with An Expert Transformer}, 
      author={Zhuoyi Yang and Jiayan Teng and Wendi Zheng and Ming Ding and Shiyu Huang and Jiazheng Xu and Yuanming Yang and Wenyi Hong and Xiaohan Zhang and Guanyu Feng and Da Yin and Xiaotao Gu and Yuxuan Zhang and Weihan Wang and Yean Cheng and Ting Liu and Bin Xu and Yuxiao Dong and Jie Tang},
      year={2024},
      eprint={2408.06072},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2408.06072}, 
}
```
