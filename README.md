# Exchange Rate Policy and Heterogeneity in SOE
 Replication code for "Exchange Rate Policy and Heterogeneity in Small Open Economies"

This folder contains the following notebooks:

- <font color='blue'>float</font>setup.ipynb: defines functions and structures
- **fill_grids_parameters.ipynb**: uses number from calibration and data to construct storage files **parameters.jld2** and **external_parameters.jld2**

Notebooks with computations:
- **compute_steady_state.ipynb**: uses **parameters.jld2** and **external_parameters.jld2** to compute the steady state and save steady-state objects
    * options include setting the productivity gap between the sectors to *"baseline"*, *"equal"*, and *"switched"*
    * these options generate respective files with steady-state objects: **steady_state_output.jld2**, **steady_state_output_equal.jld2**, and **steady_state_output_switched.jld2**
- **compute_transition.ipynb**: uses storage files with the steady-state objects to compute the transition dynamics
    * setting elasticities, setting the slope of the Phillips curve, setting the exchange rate regime, setting the fiscal regime
    * these options generate storage files with time series in the folder *transition_results*
- **compute_TSRANK.ipynb**: uses uses storage files with the steady-state objects to calibrate the two-sector RANK model and compute the transition dynamics
    * storage files with time series are in the folder *transition_results*

Notebooks for plots and tables:
- **plot_steady_state.ipynb**: plots Figure 1 in the paper
- **basic_IRF.ipynb**: plots Figure 2 in the paper
- **response_decomposition.ipynb**: plots Figure 3 in the paper
- **variance_decomposition.ipynb**: computes entries for Table 2 in the paper
- **welfare_gains.ipynb**: plots Figure 4 in the paper
- **elasticities_IRF.ipynb**: plots Figure 5 in the paper
- **alternative_rules.ipynb**: plots Figure 7 in the paper
- **alternative_rules_elasticities.ipynb**: plots Figure 8 in the paper
- **alternative_IRF.ipynb**: plots Figures 9 through 18 in the Appendix
- **fiscal_IRF.ipynb**: plots Figure 19 in the Appendix
The folder *graphs* containts these figures. Figure 6 and Table 1 in the paper are made by hand.
