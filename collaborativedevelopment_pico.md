Challenge: Collaborative Development

Objective:
Recover the hidden flag by examining a Git repository with multiple branches. The challenge requires merging or inspecting feature branches to piece together the complete flag.

Step-by-Step Walkthrough:

Download and unzip the challenge:
wget '<challenge_download_link>'
unzip challenge.zip
cd drop-in

Initialize the Git repository:
The .git directory indicates this is already a Git repo, but if not, run:

Inspect the repository:
You’ll see a flag.py file and a .git directory 

List all branches:
git branch -a

You'll see main plus multiple feature branches like feature/part-1, feature/part-2, and feature/part-3 

Inspect each branch to extract flag fragments:
git checkout feature/part-1
cat flag.py   # Shows first fragment

git checkout feature/part-2
cat flag.py   # Shows second fragment

git checkout feature/part-3
cat flag.py   # Shows third fragment
Each branch contributes a piece of the flag 


Combine fragments to form the complete flag:
The merged pieces reveal:
picoCTF{t3@mw0rk_m@k3s_th3_dr3@m_w0rk_2c91ca76}

What I Learned:
-To use git branch -a to list all branches.
-How to switch between branches with git checkout.
-That collaborative repo versions may hide the full flag across multiple branches.
-Merging or aggregating changes manually can be essential to recovering split data.