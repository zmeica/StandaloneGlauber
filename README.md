# Standalone Glauber Model from arXiv:0805.4411

## Setting up ROOT at ACCRE

```
We will use ROOT in CMSSW at ACCRE.
In any directory at ACCRE, do the following (find available release by doing 'scram list'):
[tuos@gw345 glauber]$ cmsrel CMSSW_10_3_0
[tuos@gw345 glauber]$ cd CMSSW_10_3_0/src/
[tuos@gw345 src]$ cmsenv
[tuos@gw345 src]$ root -l
root [0] .q
```
## Getting the code

```
git clone https://github.com/tuos/StandaloneGlauber.git 
```

## Running the code

```
[tuos@gw343 glauber_v1p5]$ root -l
root [0] .L runglauber_v1.5.C+
Info in <TUnixSystem::ACLiC>: creating shared library /gpfs23/scratch/tuos/PbPb2015/glauber/glauber_v1p5/./runglauber_v1.5_C.so
root [1] runAndSaveNtuple(10000,"Pb","Pb",67.6,0.4,"glauber_PbPb_default_v1p5_10k.root")
Setting up nucleus Pb
Setting up nucleus Pb
Event # 9950 x-sect = 7.69905 +- 0.0771798 b        
Done!
root [2] .q
```

### Changing collision energy

```
Find the input value of nucleon-nucleon inelastic cross section (67.6 mb in the above example) in table 2 of the paper:
 
https://arxiv.org/abs/1710.07098
```


