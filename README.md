# UC3 UNITOBrain 


# Requirements
* numpy
* pyeddl
* pyecvl
* cv2
* wandb
* scipy

# Train Run Command
```
python3 -u train_model.py --shape 128 --lr 1e-5 --weight-decay 0.0 --gpu 1 --mem full_mem --name <run-name> <dataset-path>
``` 

# Inference Run Command
```
python3 -u test_model.py --shape 128 --gpu 1 --mem full_mem <dataset-path>
``` 

# Preprocessing Run Command
```
python3 -u dicomtopt.py --rescale_size 128 --outroot <output-path> --target 'TTP'
python3 -u dicomtopt.py --rescale_size 128 --outroot <output-path> --target 'CBF'
python3 -u dicomtopt.py --rescale_size 128 --outroot <output-path> --target 'CBV'
#Without target, it computes the inputs
python3 -u dicomtopt.py --rescale_size 128 --outroot <output-path>
``` 
