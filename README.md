# Flask Image Classification

This repo comprises of training DenseNet from scratch on cifar10 and then using Flask for Model serving.

The directory is defined as 

![](dir_struct.png)



## Setting up the Environment

To setup the environment 
```bash
python3 -m pip install -U virtualenv # install the virtualenv
virtualenv -p python3 dev_env # creating an environment
source dev_env/bin/activate # activate environment
git clone https://github.com/entiretydotai/Image-Classification-and-Deployment #clone the repo
cd Image-Classification-and-Deployment
pip install -r requirements.txt # install the requirements
```



## For Training

[Run Training Notebook file](TrainingNotebook.ipynb)



## For Inference

 we need Cifar-10 data for inference. Execute the below to generate 10 random images from cifar-10 test data.

```bash
cd data
python generate_valid_data.py
```

Run [Inference Notebook file](InferenceNotebook.ipynb)




## Model Serving on Flask.

For Serving this model as a website. First generate  test images by executing above commands and then.


```bash
python flask_api/app.py
```
