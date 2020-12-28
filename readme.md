# Ensemble Dehazing Network: EDN-AT, EDN-3J, EDN-EDU
The folder includes all the training testing codes, saved models and testing results prepared for NTIRE 2020 Dehazing Challenge.

Proposed network: "Dense ‘EDN’ Dehazing Network" 

Team name: iPAL_EDN

Team leader: Mingzhao Yu(ethanyu@psu.edu)

Team members:  Venkateswararao Cherukuri, Tiantong Guo, Vishal Monga 

Time: 03/26/2020
## PRE-REQUEST
To correctly run the test model, the following packages are required.
1. Python 3.7
2. py-torch 1.0
3. openCV

## To evaluate the model
1. download the whole folder
2. download models from below link to the folder
	- EDN-AT is in: https://drive.google.com/open?id=1bEhbbnoqZ4HpH1zwB33QZjYy5kJVMbO5
	- EDN-3J is in: https://drive.google.com/open?id=1tajihAfoFYAN7XoYFfjXJcY20Eww-csh
	- EDN-EDU is in: https://drive.google.com/open?id=1EKWivnW2u9Y0PZGFuavXMkvcK8bFG0Hm
3. Navigate to the downloaded folder, in terminal, type:
	`python eval_EDN_AT.py --cuda`
	
## To train the model
- Make sure training dataset to be in .h5 file. In addition, input dataset are stored of size NxCx256x256 under 'INPUT' dataset name and target dataset are stored of size NXCX256X256 under dataset name 'TARGET'.
- Make sure packages to be installed.
- Navigate to the downloaded folder, in terminal, run the main files: 
	`python main_xxxx.py --cuda`

## FILES
1. **dense_xxx.py**: model file which would be imported when training and testing
- dense_deep_residual_AT_adaptive.py: the network structure for our "EDN-AT" model
- dense_deep_3JW.py: the network structure for our "EDN-3J" model
- dense_deep_EDU.py: the network structure for our "EDN-EDU" model

2. **main_xxx.py**: main files for training
- main_deep_AT.py: training file for EDN-AT
- main_deep_3JW.py: training file for EDN-3J
- main_deep_EDU.py: training file for EDN-EDU

3. **eval_xxx.py**: 
The file includes test codes for our proposed network.
Parser arguments: 
	--cuda (default = store_true) for running on GPU to reproduce the submitted results,  
	--test (default="./NH-HAZE_testHazy") for the testset path.
Return: running time and the saving path for results.


7. **utils.py**: function codes that can be used through the application.

8. **pytorch_msssim**: files for calculating SSIM loss.

9. **Vgg16.py**: file for Vgg model, which is used for computing vgg loss.

10. **dataset.py**: file for loading training data to dataloader.







