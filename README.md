# Social Responses to Errors in HRI Dataset

Dataset of Social Response (facial AUs) to Errors in physical human-robot interaction containing three folders representing the three data collection scenarios: Human-Robot Collaborative Assembly (HRC-A), Human-Robot Collaborative Cooking (HRC-C),  and Programming by Demonstration Data (PbD). 


In each folder, there are csv files for each error instance and a ground truth annotations file. Each error instance consists of one error and one reaction.


The error instance csv files have a naming convention of XXX_OpenFaceOutput_XXX.csv, where the X’s depend on the data collection scenario described below. These files are comprised of AUs calculated by OpenFace with each row being a timestep representing 1/3 of a second. The first column, “Originating Time,” corresponds to the time that row is in the error instance. The second column, “Confidence,” is the facial detection confidence as outputted by OpenFace, ranging from 0 to 1. The remaining (34) columns are the outputted AUs at a particular timestep. The naming convention for those columns are as follows:
AUXX_YY
The XX is the AU number and the YY is either “i” (AU intensities ranging from 0 to 5) and “o” (AU occurrence either 0 or 1).


The ground truth annotation files are named like XXX_Labels_React.csv file, where each row is an error instance. The first column “Filename” are the names of the data entries in each data collection scenario. “Error start” is the perceived error start, as annotated by two independent coders, and is defined as when the coder is sure that the error is happening. The third column, “Start React,” is the timestep in which the participant started to react. The fourth column, “End React,” is the timestep in which the participant ends their reaction to the error. If the “Start React” and “End React” columns are both 0, then the participant did not react to the error.


1. HRC-A: 
A total of 12 participants.
The ground truth annotation file is HRC-A_Labels_React.csv 
There are 23 data files present in the HRC-A folder. 
Following is the nomenclature of the data files: 


                                PXX_OpenFaceOutput_YY.csv


The XX represents participant number. The YY represents an error type. If “1,” then the error is a physical error (the robot failing to grip a PVC pipe). If “2,” then the error is a conceptual error (the robot grabbing the incorrect colored pipe).


2. HRC-C: 
A total of 33 participants.
The ground truth annotation file is HRC-C_Labels_React.csv
There are 65 data files present in the HRC-C folder.
Following is the nomenclature of the data files: 


                                PXXYY_OpenFaceOutput_ZZ.csv
 
XX represents the participant number. YY represents the interaction condition of social vs. non-social. If “S,”  it was social (robot verbally gave participants instructions) and if “O,” it was non-social (instructions were provided via text). ZZ represents two different conceptual errors, in both cases providing the wrong object to a request (either “1” or “2”). 


3. PbD: 
A total of 28 participants.
The ground truth annotation file is PbD_Labels_React.csv.
There are 38 data files present in the PbD folder.
Following is the nomenclature of the data files: 
                                
                                PXX_OpenFaceOutput_YY.csv


XX represents the participant number. YY represents different error types. If “a” or “p1,” the error is a physical error (robot dropping a box). If “p2,” the error is physical (robot hitting an object with another). If “c1,” the error is conceptual (robot incorrectly sorted an object). If “c2,” the error is conceptual (robot placed object outside of correct target). If “g1,” the error is generalization error (robot missed picking up an object because it did not correctly generalize pick-and-place to that object). If “g2,” the error is generalization error (robot missed picking up an object because the gripper was not oriented correctly).

----

## BibTeX
If you use this robotic system in a scientific publication, please cite our work:
```
@inproceedings{stiber2023using,
  title={On Using Social Signals to Enable Flexible Error-Aware HRI},
  author={Stiber, Maia and Taylor, Russell H and Huang, Chien-Ming},
  booktitle={Proceedings of the ACM/IEEE International Conference on Human-Robot Interaction},
  year={2023}
}
```
