### Please Read the Following Instruction to Get Started ###

This repository is made to run the fits on our newly process Bs and B+ CMS 2017 pp 5.02 TeV datasets. If you successfully run the codes, you should be able to see clear Bs and B+ peaks

Some rename of the codes may need to be done since some of the codes' names are a little weird. Nonetheless, for the moment, let's stick to the names now and see if we can get the fits on the B mesons done.  

## To START ##

To start, first find a fresh folder on your local machine

Then get this repository first download it from github by doing:

git clone https://github.com/MYOMAO/BmesonppFits.git

All the input files are stored at InputFiles/

If you do ls, you should see


## Get the B+ Fits for pT = 5 - 50 GeV/c ##

cd  BPlus/

mkdir -p ROOTfiles

mkdir -p plotFits/final_roofit/

source doAnalysis3.sh

ls ROOTfiles 

You should see the output file named: yields_Bp_full.root

ls  plotFits/final_roofit/

You should see the png and pdf files named: data_PbPb_1_Bpt_510_doubly0_0_90_ntKp.png  mc_PbPb_1_Bpt_510_doubly0_0_90_ntKp.png  data_PbPb_1_Bpt_550_doubly0_0_90_ntKp.pdf  mc_PbPb_1_Bpt_550_doubly0_0_90_ntKp.pdf


You can have a look at the png or pdf file and you should be able to see a very clear B+ peak in the invariant mass distribution with fits to the data points

## Get the Bs Fits for pT = 5 - 50 GeV/c ##

cd  Bs/


mkdir -p ROOTfiles

mkdir -p plotFits/final_roofit/


source doAnalysis2.sh


ls ROOTfiles 

You should see the output file named: yields_Bs_full.root

ls  plotFits/final_roofit/

You should see the png and pdf files named: data_PbPb_1_BptNew_550_doubly0_0_90EffInfoTreeFit.pdf  mc_PbPb_1_BptNew_550_doubly0_0_90EffInfoTreeFit.pdf  data_PbPb_1_BptNew_550_doubly0_0_90EffInfoTreeFit.png  mc_PbPb_1_BptNew_550_doubly0_0_90EffInfoTreeFit.png

You can have a look at the png or pdf file and you should be able to see a very clear Bs peak in the invariant mass distribution with fits to the data points


## Change the fitting on different B mesons pT range ##

To change the fitting parameters, simply edit the file "parametersNew.h" under the BPlus/ or Bs/ folder


Inside the file, you can see, in line 44:

double ptBins_full[nBins_full+1] = {5,50};

Now you can change its range to something you want to explore. For instance, 50 - 100 by 


double ptBins_full[nBins_full+1] = {50,100};

Save you files and run the shell script 

doAnalysis3.sh for BPlus and doAnalysis2.sh for Bs and you should be able to get the output of the new fit plots in the folder

plotFits/final_roofit/


Have a look at the folder and see if you see different plots.


## Question and Contact Information ##

If you have any question, please feel free to contact me at zzshi@mit.edu
