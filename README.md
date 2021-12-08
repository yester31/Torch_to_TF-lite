# pytorch_to_tensorflow
- CPU 11th Gen Intel(R) Core(TM) i7-11375H @ 3.30GHz (cpu)
- tensorflow 2.7.0

## 0. Pytorch Resnet18
- resnet18 Model
- Performace evaluation(Execution time of 100 iteration for one 224x224x3 image)
- PyTorch (cpu) -> 3235 [ms]
- PyTorch (gpu) -> 363 [ms]

## 1. Pytorch to Tensorflow by ONNX
- Conversion pytorch to tensorflow by onnx
  - TF (cpu) -> 3748 [ms]
  - TF (gpu) -> 832 [ms]

## 2. Pytorch to Tensorflow by functional API
- Conversion pytorch to tensorflow by using functional API 
- TF (cpu) -> 4804 [ms]
- TF (gpu) -> 3227 [ms]

## 3. Tensorflow lite on CPU
- Conversion pytorch to tensorflow by functional API
  - TF lite f32 (cpu) -> 7781 [ms], 44.5 [MB]
    - max index : 388 , prob : 13.55378, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
  - TF lite f16 (cpu) -> 5447 [ms], 22.3 [MB]
    - max index : 388 , prob : 13.54807, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
  - TF lite int8 (cpu) -> 977569 [ms], 11.2 [MB]
    - max index : 388 , prob : 13.71834, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
- Conversion pytorch to tensorflow by onnx
  - TF lite f32 (cpu) -> 6133 [ms], 44.5 [MB]
    - max index : 388 , prob : 13.80411, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
  - TF lite f16 (cpu) -> 6297 [ms], 22.3 [MB]
    - max index : 388 , prob : 13.79882, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
  - TF lite int8 (cpu) -> 1072768 [ms], 11.2 [MB]
    - max index : 388 , prob : 14.05152, class name : giant panda panda panda bear coon bear Ailuropoda melanoleuca
- Calculated on 2021-12-09

## 4. Tensorflow lite on raspberry pi 4


## Reference : 
- <https://www.tensorflow.org/lite/convert?hl=ko>
- <https://dmolony3.github.io/Pytorch-to-Tensorflow.html>