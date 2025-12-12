# Yolo models on LARD V2
Repository dedicated to storing models trained on LARD_V2 with [Ultralytics](https://docs.ultralytics.com/models/yolo11) framework, and provided under AGPL-3.0 License

# Training reproductibility
The models provided here are trained with Ultralytics framework using the yaml file provided.
The first version provided here use the basic command line interface of Ultralytics for training:
```shell
yolo train data=data.yaml model=LARD_V2.yaml
```

# Data
These models were all trained on LARD_V2 which is a publicly available dataset for runway detection.
- The repository for generating new image data is available in open source at https://github.com/deel-ai/LARD/tree/LARD_V2
- The LARD V2 dataset is available on HuggingFace at https://huggingface.co/datasets/DEEL-AI/LARD_V2

# Licence
[AGPL](LICENSE): GNU Affero General Public inherited from Ultralytics
