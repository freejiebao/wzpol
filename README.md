# WZ VBS polarization
    git clone https://github.com/freejiebao/wzpol.git

## NanoGEN private producation
We use `CMSSW_11_2_0_pre8` for NanoGEN. *PhysicsTools/NanoAOD/plugins/GenWeightsTableProducer.cc* is modified to make **reweighting weights** stored.

### Submit jobs
```
cd nanogen
mkdir log
chmod +x wrapper.sh
condor_submit submit.jdl
```

## NanoAOD private producation
We follow **NanoAODv7** production of  [**WLLJJ_WToLNu_EWK**](https://cms-pdmv.cern.ch/mcm/chained_requests?contains=SMP-RunIIAutumn18NanoAODv7-00058&page=0&shown=15), official samples are generated in `slc6_amd64_gcc700`, we will use `slc7_amd64_gcc700`.

### Submit jobs
```
cd nanoaod
mkdir log
chmod +x wrapper.sh
condor_submit submit.jdl
```
## Tips
1. To change input gridpacks, jobs numbers: modify **Queue** in **submit.jdl**.

2. To change the number of request events: modify the 2nd **arguments** in **submit.jdl**.

3. Folder **log** is necessary.

4. The **wrapper.sh** must be executable.
