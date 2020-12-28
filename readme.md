# EDN-AT
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

#################################TO evaluate the model####################################
Navigate to the downloaded folder, in terminal, type:
	python eval_EDN_AT.py --cuda
	
#################################TO train the model####################################
Navigate to the downloaded folder, in terminal, run the main files:
	python main_xxxx.py --cuda

## FILES
1. **eval_xxx.py**: 
The file includes test codes for our proposed network.
Parser arguments: 
	--cuda (default = store_true) for running on GPU to reproduce the submitted results,  
	--test (default="./NH-HAZE_testHazy") for the testset path.
Return: running time and the saving path for results.

2. **Model** is in: https://drive.google.com/open?id=1bEhbbnoqZ4HpH1zwB33QZjYy5kJVMbO5

3. **EDN_AT_results**: 
The folder includes the dehazed images of the test images provided in NTIRE 20 Dehazing Challenge.
	(1) ##.png: the dehazed images using our proposed network.
	(2) readme.txt: the information for running time, GPU and Data usage

4. **NH-HAZE_testHazy**: 
The folder includes the test images from NTIRE 20 Dehazing Challenge.

5. **utils.py**: function codes that can be used through the application.

6. **dense_xxx.py**: model file which would be imported when training and testing
- dense_deep_residual_AT_adaptive.py: the network structure for our "EDN-AT" model
- dense_deep_3JW.py: the network structure for our "EDN-3J" model
- dense_deep_EDU.py: the network structure for our "EDN-EDU" model

7. **main_xxx.py**: main files for training
- main_deep_residual_AT_adaptive.py: training file for EDN-AT
- main_deep_3JW.py: training file for EDN-3J
- main_deep_EDU.py: training file for EDN-EDU




