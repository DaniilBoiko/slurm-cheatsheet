# slurm-cheatsheet

## Helpful resources
* https://slurm.schedmd.com — official docs
* https://www.sherlock.stanford.edu/docs/user-guide/running-jobs/ — Stenford's Sherlock docs
* https://www.psc.edu/resources/bridges-2/user-guide-2-2/ — PSC Bridges-2 docs

## Sructure of a file with a slurm job
```bash
#!/bin/bash
#SBATCH -n 8
#SBATCH -t 48:00:00
#SBATCH --gpus 1

source .bashrc

<your code>
```

## List your tasks
```bash
squeue --me
```

## Save current queue as JSON
```bash
squeue --json > jobs_2023-03-08.json
```

## Listing available resources
```bash
sinfo -o "%20N  %10c  %20m  %30G "
```

## How to check GPU utilization on a specific machine?
You can SSH directly to any machine that is running any of your tasks.
