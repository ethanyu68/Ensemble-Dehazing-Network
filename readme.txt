################################## EDN-AT #################################
The folder include all the codes, saved models and testing results prepared for NTIRE 2020 Dehazing Challenge.

Proposed network: "Dense ‘EDN’ Dehazing Network" 
Team name: iPAL_EDN
Team leader: Mingzhao Yu(ethanyu@psu.edu)
Team members:  Venkateswararao Cherukuri, Tiantong Guo, Vishal Monga 
Time: 03/26/2020

##############################PRE-REQUEST###################################
To correctly run the test model, the following packages are required.
1. Python 3.7
2. py-torch 1.0
3. openCV

#################################TO#RUN####################################

Navigate to the downloaded folder, in terminal, type:
	python eval_EDN_AT.py --cuda

#################################FILES######################################
1. eval_EDN_AT.py: 
The file includes test codes for our proposed network.
Parser arguments: 
	--cuda (default = store_true) for running on GPU to reproduce the submitted results,  
	--test (default="./NH-HAZE_testHazy") for the testset path.
Return: running time and the saving path for results.

2. Model is in: https://drive.google.com/open?id=1bEhbbnoqZ4HpH1zwB33QZjYy5kJVMbO5

3.EDN_AT_results: 
The folder includes the dehazed images of the test images provided in NTIRE 20 Dehazing Challenge.
	(1) ##.png: the dehazed images using our proposed network.
	(2) readme.txt: the information for running time, GPU and Data usage

4. NH-HAZE_testHazy: 
The folder includes the test images from NTIRE 20 Dehazing Challenge.

5. utils.py: function codes that can be used through the application.
6. dense_deep_residual_AT_adaptive.py: the network structure for our "EDU" model

