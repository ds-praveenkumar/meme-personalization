# meme-personalization
This repo has in creating personalization of memes.


### Running Instuctions
```
wget https://huggingface.co/runwayml/stable-diffusion-v1-5/resolve/main/v1-5-pruned-emaonly.ckpt -O ./models/pointrend_resnet50.pkl

python create_mask.py \
  --video_path="templates/dimitri_finds_out/source.mp4" \
  --save_path="templates/dimitri_finds_out/mask.mp4"

python run.py \
  --meme_template="dimitri_finds_out" \
  --fine_tuned_model_path="./models/pointrend_resnet50.ckpt"