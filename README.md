# MetaChaos
This Repository Contains the Software for MetaChaos **(The manuscript is prepared for submitting to the Journal of Computational Biology)

The metagenomics clustering method name MetaChaos was proposed. The two concepts for identifying the number of species were introduced. The first concept employs feature extraction of vectors of overlapping reads groups by using Chaos Game Representation. Feature vectors embedded in high-dimensional are reduced into low-dimensional by using t-SNE. Then, the second concept is the clustering process all of t-SNE scatter points using the modified k-nearest neighbor algorithm whose the number of k nearest neighbors is defined in terms of change-point.

=Run MetaChaos=

$ run_MetaChaos.sh

Please [input the fasta files of short or long reads] [the output files (.csv) from MetaProbS algorithm] [options]

	$ Options:
	$ types		: types of data set: 1 stands for a short reads datasets, 2 stands for long reads datasets.
				
	
	$ Usage:
	./run_MetaChaos.sh  LD_LIBRARY_PATH [types] [fasta files] [MetaProbS output files] 
	
	For example,
	Run MetaChaos on simulated datasets:
	$ ./run_MetaChaos.sh /usr/local/MATLAB/R2022a /home/admin1/MetaChaos/ 1 S1_1.fna S1_2.fna S1_1.fna.groups.csv S1_2.fna.groups.csv 
	$ ./run_MetaChaos.sh /usr/local/MATLAB/R2022a /home/admin1/MetaChaos/ 1 L1_1.fna L1_2.fna L1_1.fna.groups.csv L1_2.fna.groups.csv 
	$ ./run_MetaChaos.sh /usr/local/MATLAB/R2022a /home/admin1/MetaChaos/ 2 R1.fna [] R2.fna.groups.csv [] 

=Output=

  fasta files of the predicted clusters
  2D t-SNE points
  5-mer feature vector
  
Authors: Nipaporn Thipmanee (nipaporn.t@student.chula.ac.th), Chidchanok Lursinsap (lchidcha@gmail.com), and Jeerayut Chaijaruwanich (mr.jeerayut@gmail.com)
