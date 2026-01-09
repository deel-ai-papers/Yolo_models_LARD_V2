# Yolo models on LARD V2
Repository dedicated to storing models trained on LARD_V2 with [Ultralytics](https://docs.ultralytics.com/models/yolo11) framework, and provided under AGPL-3.0 License

# Repository
Models are divided into 3 categories:
- `yolo_v8_models/` folder contain all the models trained from a yolov8 architecture with different label configurations, as described in our paper (only on `IN_ODD` or on both `IN_ODD` and `IN_EXTENDED_ODD`). 
- `yolo_v11_models/` folder contains all the models trained from a yolov11 architecture with different data source configuration, as described in our paper: in **single-source** configurations, in **leave-one-out** configurations, or on the **complete** dataset.
- `piano_calibration_model/` folder contains the model trained on the piano detection task used during the calibration process of the different simulators, as described in our paper.

# Training reproductibility
The models provided here are trained with Ultralytics framework using the yaml file provided. The training is based on the command line interface of Ultralytics, for example:
```shell
yolo train data=LARD_V2.yaml model=models/yolo11n.pt
```
We used different type of folders from different data sources (GES, BingMaps, ArcGIS, XPlane and Flight Simulator) and specific tags (`IN_ODD` and `IN_EXTENDED_ODD`) for the training of the different models described in our paper.

# Data
Except for the models dedicated to piano_calibration, all the models provided here were trained on LARD_V2 which is a publicly available dataset for runway detection.
- The LARD V2 dataset is available on HuggingFace at [huggingface.co/datasets/DEEL-AI/LARD_V2](https://huggingface.co/datasets/DEEL-AI/LARD_V2)
- The repository for generating new image data is available in open source at [github.com/deel-ai/LARD](https://github.com/deel-ai/LARD)



Finally, the dataset for *piano_calibration* will be made publicly available on HuggingFace soon.

# Paper
The paper will be available in the proceedings of the ERTS 2026 conference and soon on Arxiv.

# Licence
[AGPL](LICENSE): GNU Affero General Public inherited from Ultralytics
- The provided pretrained YOLO weights are under AGPL-3.0 (per Ultralytics’ licensing statement). Please keep the LICENSE with any redistribution.
- Our libraries (provided at https://github.com/deel-ai) are independent. If you package/distribute a combined application that includes Ultralytics (AGPL) code, the distribution must comply with AGPL.
