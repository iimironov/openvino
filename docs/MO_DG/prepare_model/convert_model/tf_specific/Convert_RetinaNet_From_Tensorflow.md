# Converting RetinaNet Model from TensorFlow* to the Intermediate Representation {#openvino_docs_MO_DG_prepare_model_convert_model_tf_specific_Convert_RetinaNet_From_Tensorflow}

This tutorial explains how to convert RetinaNet model to Intermediate Representation (IR).

[Public RetinaNet model](https://github.com/fizyr/keras-retinanet) does not contain pretrained TensorFlow* weights. To convert this model to the TensorFlow* format you can use [Reproduce Keras* to TensorFlow* Conversion tutorial](https://docs.openvinotoolkit.org/latest/omz_models_model_retinanet_tf.html).

After you convert model to TensorFlow* format you can run the Model-Optimizer command below:
```sh
python mo.py --input "input_1[1 1333 1333 3]" --input_model retinanet_resnet50_coco_best_v2.1.0.pb --data_type FP32 --transformations_config ./extensions/front/tf/retinanet.json
```