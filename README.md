- This is the implementation of RACCM and  CCA-k-RFP-M1.

- Important things to do before testing:
  1) Extract the zip file.
  2) Open a terminal and move to the folder using the cd command.
  3) Install the necessary libraries.
  4) For Mac users, it is possible that the solver will not work for security reasons.
     In that case, go to the system security settings (System Preferences → Security & Privacy),
     allow access, and it will work.

- To generate k-RFPs, use the command below to run the solver.
  This is an example for generating k-RFPs for the "Vote" dataset with minimum support of 10 percent (435 × 0.1 = 43.5):

  ./xsat4DAR -kx=1 -ky=1 -minsupp=43 -gdar=1 -msi=43 dataset/votefinal.txt | grep "^[1-9]" >RelaxedPatterns/patternsk1.txt  

- For the parameters:
  - kx     ===>    relaxation (k=1)
  - minsupp     ===>    minimum support
  - Note: minsupp = msi for efficiency reasons

- Scripts:
  - CCA-k-RFP-M1.py  ===> CCA-k-RFP-M1 approach
  - RACCM.py          ===> Redundancy-Aware Conceptual Clustering Method
