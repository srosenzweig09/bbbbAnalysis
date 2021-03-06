To copy a file from EOS, use command xrdcp <url-of-file> <destination>
    for example:
```bash
xrdcp root://cmseos.fnal.gov//store/user/srosenz/path/to/file.filetype
```


**Useful commands:**

----- To run the skim code --------------------------------------------------------------------------------------------

```bash
skim_ntuple.exe --cfg config/Resonant_NMSSM_bbbb/skim_2016Resonant_NMSSM_XYH_bbbb_Fast.cfg --input inputFiles/2016_NMSSM_XYH_bbbb_Datasets/NMSSM_XYH_bbbb_MX_700_NANOAOD_v7.txt --output test_NMSSM_XYH_bbbb_MC_20200502.root --is-signal --xs=1 --puWeight weights/2016_NMSSM_XYH_bbbb_weights/NMSSM_XYH_bbbb_MX_700_NANOAOD_v7_PUweights.root --maxEvt 100000 --yMassSelection=300
```


----- To run the signal regions --------------------------------------------------------------------------------------------


```bash
fill_histograms.exe config/Resonant_NMSSM_bbbb/MXless1000_MYgreater140/plotter_2016Resonant_NMSSM_XYH_bbbb.cfg
```


----- To run the efficiencies --------------------------------------------------------------------------------------------

>> modify `read_OutPlotter.py` to reflect the most recent job tag and its predecessor so it can rewrite the file logs.
