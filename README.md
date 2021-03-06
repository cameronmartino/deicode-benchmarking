# simulations

Scripts and visualization notebooks used to generate simulations on real data (keyboard dataset: [Qiita 232](https://qiita.ucsd.edu/study/description/232)) and benchmark rclr transform. 

- simulations.ipynb
- intro_fig.ipynb
- figures
    - figure2.png (figure generated in simulations.ipynb)
- scripts
    - cluster_build.py (script runs simulation building on keyboard data in cluster_models)
    - cluster_results.py (runs simulation results in cluster_models)
- cluster_models (simulations and results)
    - keyboard.biom.gz (Real data used to fit simulations)
    - keyboard.txt.gz (Real meta-data used to fit simulations)
    - simulation_subsampled_noisy.csv.gz (simulation with noise/sparsity generated from cluster_build.py)
    - base_model_keyboard_table.csv.gz (simulation without noise/sparsity noise generated from cluster_build.py)
    - ordination (benchmark ordinations from cluster_results.py)
    - results.csv.gz (results kl-div from cluster_results.py) 

# case_studies (Requires Qiime2, run here on qiime2-2018.6)

Scripts and visualization notebooks used to benchmark rclr-RPCA against Bray-Curtis and Weighted UniFrac for two case studies:

- Case Study 1: The Sponge Microbiome Project ([Qiita 10793](https://qiita.ucsd.edu/study/description/10793))
- Case Study 2: Sleep Apnea ([Qiita 10422](https://qiita.ucsd.edu/study/description/10422))
- figures
    - figure3.png (benchmarking results on subsamples from subsample_results.tar.gz)
    - figure4.png (use case example from sub_sample max samples in both cases)
- case_studies.ipynb (visualization notebook)
- data.tar.gz (data used acquired from Qiita 10/01/2019)
- subsample_results.tar.gz (results from running all scripts)
- scripts
    - subsample.py (generate subsamples from the data.tar.gz dir)
    - distances.py (run distances for each subsample RPCA, WU, and BC)
    - sub_results.py (return PERMANOVA and KNN results)
- sub_sample
    - biom_tables_Sleep_Apnea (all sleep apnea subsamples [70,184] 10-fold generaterd by subsample.py)
    - biom_tables_Sponges (all sponge subsamples [70,248] 10-fold generated by subsample.py)