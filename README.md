### Please Read the Following Instruction to Get Started ###

This repository is made to run the fits on our newly process Bs and B+ CMS 2017 pp 5.02 TeV datasets. If you successfully run the codes, you should be able to see clear Bs and B+ peaks

Some rename of the codes may need to be done since some of the codes' names are a little weird. Nonetheless, for the moment, let's stick to the names now and see if we can get the fits on the B mesons done.  

## To START ##

To start, first find a fresh folder on your local machine

Then get this repository first download it from github by doing:

git clone https://github.com/MYOMAO/BmesonppFits.git


## Get the B+ Fits for pT = 5 - 50 GeV/c ##

cd  BPlus/

mkdir -p ROOTfiles 

mkdir -p plotFits/final_roofit/

source doAnalysis3.sh

cd ../../



## Get the Bs Fits for pT = 5 - 50 GeV/c ##

cd  Bs/

mkdir 

source doAnalysis3.sh

cd ../../




## Change the fitting on different B mesons pT range ##

To change the fitting 
