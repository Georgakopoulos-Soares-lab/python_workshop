# Intro to Roar Collab & Python


## Useful links

Penn State Roar Collab Page
[Roar Collab](https://www.icds.psu.edu/access-roar-and-roar-collab-online/)

Login to Interactive Dashboard
[Dashboard](https://rcportal.hpc.psu.edu/pun/sys/dashboard)

### Basic Jupyter Commands & Extensions

```
%load_ext autoreload
%autoreload 2
```

Run shell commands using exclamation mark (!):
(What's in there?)

```
!ls /storage/group
```

### Bash Commands

```
ls -lh -a
cd ..
cd
cd <path>
grep -a <path>
find . 
```

### How to Submit a job

#### Anatomy of the Bash Script


Specifying jobs parameters:

```
#!/bin/bash

# Job parameters
#SBATCH --job-name=HelloWorld
#SBATCH --output=res.txt
```

Specifying Job Resources

```
#SBATCH --mem=10GB
#SBATCH --time=48:00:00
#SBATCH --ntasks=1
#SBATCH --cpus-per-task=1
```

Finally, specifying job operations:

```
echo "My Hello World starts at $(date)"
sleep 20
echo "Hello World!"
echo "My Hello World ended at $(date)"
```
