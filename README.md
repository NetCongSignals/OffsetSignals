## Relating paper ##
Public Signals in Network Congestion Games. \
S. M. Griesbach, M. Hoefer, M. Klimm, T. Koglin. \
In Proc. 23rd Conference on Economics and Computation (EC), page 736, 2022, doi: 10.1145/3490486.3538349 \
[Link to paper](https://doi.org/10.1145/3490486.3538349)


## General information ##

This repository provides the code and data used in the computational study of the paper combined in a single zip-file.

The main code for computing the flows in Wardrop equilibrium is highly based on the work of Matteo Bettini (https://github.com/matteobettini/Traffic-Assignment-Frank-Wolfe-2021; last accessed: 2022-01-06). Yet, we adjusted it to our model and the information design framework.

The network data was obtained from the Transportation Networks for Research Core Team (https://github.com/bstabler/TransportationNetworks; last accessed: 2022-01-14.).

## Guiding notes for using the repository ##

### Code ###
- Main code for data generation, the next three codes contain subroutines ("./compute_data.py")
- Code for computing the statistic quantities in Tables 2 and 3 ("./compute_stats.py")
- Implementation of LP for determining range of supports ("./lp_solver.py")
- Methods for computing flow assignments ("./Traffic-Assignment-Frank-Wolfe-2021-main/assignment.py")
- Methods for loading and generating networks from the original data files ("./Traffic-Assignment-Frank-Wolfe-2021-main/network_import.py", "./Traffic-Assignment-Frank-Wolfe-2021-main/utils.py")
- Code for selecting the data files for evaluation ("./find_duplicates.py")

More information on each code file is provided in their respective headers.

### Data ###
For each instance, there is a file 'support_{ID}.txt' that stores all central results needed for computing the quantities in Table 2 and 3.
The ID consists of three or four digits which are assigned to the networks as follows:
- SF: 500 - 540
- EM: 600 - 640
- BF: 700 - 740
- BP: 200 - 240
- BT: 900 - 940
- BM: 1000 - 1040

"./TransportationNetworks-master/" contains the original network data from [29].

Navigation:
- All support-files generated in terms of our computational study ("./loop_results/stat_data/")
- Support-files considered in our results, i.e., after clearing by find_duplicates.py, are stored in "./loop_results/stat_data/cleared/"
- Results computed by compute_stats.py are stored in "./loop_results/stat_eval/"
- Original network data is stored in "./TransportationNetworks-master/"

### Miscellaneous ###
- Handbook for flow assignment techniques for references ("./traffic_assignment_book.pdf")
  Source: https://sboyles.github.io/teaching/ce392c/book.pdf (last accessed: 2022-01-07)
