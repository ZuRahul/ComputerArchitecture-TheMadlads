# PACMan: Data Prefetchers and Cache replacement interaction

This project is done as a part of [CS305: Computer Architecture](https://www.cse.iitb.ac.in/~biswa/courses/CS305/schedule.html) course at IIT Bombay. Project was exploratory in nature.

Please visit [here](https://www.cse.iitb.ac.in/~biswa/courses/CS305/schedule.html) for youtube presentation of the project and [here](https://www.cse.iitb.ac.in/~biswa/courses/CS305/schedule.html) is link to the presentation slide.

# Benchmark INFO

6<_><_>.<benchmark_name> refers to SPECspeed version (time based metric)

| Benchmarks | Application Area                 |
|:----------:|:--------------------------------:|	
| mcf        | Route Planning                   |
| lbm        | Fluid Dynamics                   |
| gcc        | GNU C Compiler                   |
| cactusbssn | Physics: Relativity              |
| roms       | Regional Ocean Modelling         |
| xalancbmk  | XML to HTML Conversion via XLST  |

More details on [Overview - CPU 2017](https://www.spec.org/cpu2017/Docs/overview.html#benchmarks)

# How to collect ipc data from this project?
Unmodified champsim is available [here](https://github.com/ChampSim/ChampSim). 

Read [README.md](https://github.com/ChampSim/ChampSim#readme) to know how to build and run champsim.

Download this project github repository.

Put traces file in the ChampSim/traces folder.

Copy replacement policies file from drrip/hawkeye/lru/ship++/suggested_improvements to ChampSim/replacement

Change Directory to ChampSim and run following command.

```console
The Madlads@CA-Project:~$ ./build_champsim.sh bimodal no ipcp ipcp no repl_pol_name 1 # repl_pol_name.llc_repl
The Madlads@CA-Project:~$ ./run_champsim.sh bimodal-no-ipcp-ipcp-no-repl_pol_name-1core 10 10 trace_file_name
```
Generated .txt will be stored in results_10M

# References

## IPCP - Prefetcher

IPCP prefetcher at L1 and L2. Code, slides and paper of IPCP is available [here](https://dpc3.compas.cs.stonybrook.edu/?final_programs).

## Replacement Policies
Ship++ and Hawkeye original codes are available [here](https://crc2.ece.tamu.edu/?page_id=53).

## Traces

SPEC 2017 traces download from [here](https://hpca23.cse.tamu.edu/champsim-traces/speccpu/index.html) that starts with 6XX, especially use mcf, lbm, gcc, cactusbssn, roms, and xalancbmk.


# Team - The Madlads

| Team Member - Name  | Team Member - Roll No |
| :--: | :--: |
| Divyansh Nankani | 190050035 |
| Pranjal Beniwal | 190050091 |
| Rahul Prajapat | 190050095 |
| Raja Gond | 190050096 |
| Tulip Pandey | 190050125 |