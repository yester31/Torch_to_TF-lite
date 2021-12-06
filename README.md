# pytorch_to_tensorflow

## 0. Pytorch Resnet18
- resnet18 Model
- Performace evaluation(Execution time of 100 iteration for one 224x224x3 image)
- PyTorch (cpu) -> 3235 [ms]
- PyTorch (gpu) -> 363 [ms]

## 1. Pytorch to Tensorflow by ONNX
- ONNX TF (cpu) -> 3748 [ms]
- ONNX TF (gpu) -> 832 [ms]

## 2. Pytorch to Tensorflow by functional API
- TF functional API (cpu) -> 4804 [ms]
- TF functional API (gpu) -> 3227 [ms]

## 3. Tensorflow lite


## Reference : 
- <https://www.tensorflow.org/lite/convert?hl=ko>
- <https://dmolony3.github.io/Pytorch-to-Tensorflow.html>