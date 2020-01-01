# How to use
## collect images
```
pip install googleimagesdownload
googleimagesdownload -k "first_word" -sk "second_word"
```
## learning
```
python retrain.py \
  --bottleneck_dir=bottlenecks \
  --how_many_training_steps=100 \
  --model_dir=inception \
  --summaries_dir=training_summaries/basic \
  --output_graph=retrained_graph.pb \
  --output_labels=retrained_labels.txt \
  --image_dir=target_dir
```
## predict
```
python label_image.py --image target.jpg --graph retrained_graph.pb --labels retrained_labels.txt --input_layer=Placeholder
```
