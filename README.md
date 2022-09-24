# Monocular Unified Autonomous Robotics Perception Framework

The unified autonomous robotics perception framework is an anchor-free multi-task network that can jointly handle vision perception tasks such as object detection,semantic segmentation etc.. The multi-task paradigm not only can be efficiently customized to add new vision tasks but also reduces the computation costs which is crucial to be deployed on embedded devices. The current framework only supports 2D object detection and segmentation, keypoint estimation,3D task will be included in the future.

### Model Architecture

![image](https://github.com/Jumponthemoon/Unified_Robotic_perception/blob/main/Model%20architecture.png)

Model parameter and inference speed

| Model | Size | Params | Speed |
| --- | --- | --- | --- |
| CSPNet+FPN | 512 | 23.1M | 45fps |

## Result **Visualization**

Object detection

Semantic Segmentation

Keypoint Estimation

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%201.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%202.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%203.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%204.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%205.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%206.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%207.png)

![Untitled](Monocular%20Unified%20Autonomous%20Robotics%20Perception%20F%2037605f6c15a24d1b9f724d6676d01923/Untitled%208.png)

## **Requirements**

- Python >= 3.6
- PyTorch >= 1.11
- torchvision that matches the PyTorch installation.
- OpenCV
- pycocotools

```
# COCOAPI=/path/to/clone/cocoapi
git clone https://github.com/cocodataset/cocoapi.git $COCOAPI
cd $COCOAPI/PythonAPI
make
python setup.py install --user
```

### **Training**

The training code will be realeased after the model evaluated on open-dataset.

### **Visualization**

```jsx
python demo.py perception --demo /path/to/images --load_model ../exp/perception/0920_mat/model_last.pth --save_folder path/to/save --debug 4  
```

## TODO

- [ ]  Clean-up
- [ ]  Evaluate on open dataset
- [ ]  Support monocular 3d detection
