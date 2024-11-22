## <div align="center">Documentation</div>

See below for a quickstart installation and usage example, and see the [YOLOv8 Docs](https://docs.ultralytics.com) for
full documentation on training, validation, prediction and deployment.

<details open>
<summary>Install</summary>

Pip install the ultralytics package including
all [requirements.txt](https://github.com/ultralytics/ultralytics/blob/main/requirements.txt) in a
[**3.10>=Python>=3.7**](https://www.python.org/) environment, including
[**PyTorch>=1.7**](https://pytorch.org/get-started/locally/).

```bash
pip install ultralytics
```

</details>

<details open>
<summary>Usage</summary>

#### CLI

YOLOv8 may be used directly in the Command Line Interface (CLI) with a `yolo` command:

```bash
yolo predict model=yolov8n.pt source="https://ultralytics.com/images/bus.jpg"
```

`yolo` can be used for a variety of tasks and modes and accepts additional arguments, i.e. `imgsz=640`. See the YOLOv8
[CLI Docs](https://docs.ultralytics.com/cli) for examples.

#### Python

YOLOv8 may also be used directly in a Python environment, and accepts the
same [arguments](https://docs.ultralytics.com/cfg/) as in the CLI example above:

```python
from ultralytics import YOLO

# Load a model
model = YOLO("yolov8n.yaml")  # build a new model from scratch
model = YOLO("yolov8n.pt")  # load a pretrained model (recommended for training)

# Use the model
results = model.train(data="coco128.yaml", epochs=3)  # train the model
results = model.val()  # evaluate model performance on the validation set
results = model("https://ultralytics.com/images/bus.jpg")  # predict on an image
success = model.export(format="onnx")  # export the model to ONNX format
```
## <div align="center">Notice</div>
