# Organic or Recyclable AI

This AI can detect if something is organic or recyclable, which could help with the environment.

![test1](https://github.com/user-attachments/assets/3e4775ef-fb13-473a-be15-9ed23a5320a4)

## The Algorithm

The algorithm works by using the ResNet-18 model that has been retrained to recognize the difference between something organic and something recyclable by analyzing images that fall into either category.

## Running this Project

1. **Ensure Python3 and Jetson Inference Library are Installed:**
   Make sure Python3 and the Jetson Inference library are installed on your Jetson Nano.

2. **Create Directory for Model:**
   Create a directory called `Organic_Recyclable` in `jetson-inference/python/training/classification/models/` and place the `resnet18.onnx` file inside it.

3. **Set Up Environment:**
   Navigate to `jetson-inference/python/training/classification` and run:
   ```bash
   ls models/Organic_Recyclable/ Then set the NET and DATASET variables:NET=models/Organic_Recyclable DATASET=(What you have set for your data set)
4. **Run the Model:**
   Execute the following command to test the model:
   imagenet.py --model=$NET/resnet18.onnx --input_blob=input_0 --output_blob=output_0 --labels=$DATASET/labels.txt $DATASET/(The name of your test image) test1.jpg

For more details, [view a video explanation here](video link).



