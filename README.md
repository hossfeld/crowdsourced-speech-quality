# Crowdsourced subjective speech quality assessment database

The subjective quality of transmitted speech is traditionally assessed in a controlled laboratory environment according to ITU-T Rec. P.800. In turn, with crowdsourcing, crowdworkers participate in a subjective online experiment using their own listening device, and in their own working environment.

The work by Naderi et al. (2020) investigates the impact of the number of judgments on the reliability and the validity of quality
ratings collected through crowdsourcing-based speech quality assessments, as an input to [ITU-T Rec. P.808](https://www.itu.int/rec/T-REC-P.808/en) . Three crowdsourcing
experiments on different platforms were conducted to evaluate the overall quality of three different speech datasets, using the
Absolute Category Rating procedure. The results provide a suggestion on the required number of votes per condition, and allow to
model its impact on validity and reliability.

## Database Description
The database is published to the community and provides the subjective data from one of the crowdsourcing studies. A detailed description of the crowdsourcing study and the results can be found in the paper below. 

For each of the three crowdsourcing experiments (XYZ = 401,501,701), the following two files are available which contain the subjective data from the crowdsourcing experiments as described in the **[QoMEX 2020] paper** below.

The crowdsourcing experiments contain the following nubmer of conditions and votes.

| CS Experiment | #Conditions | #User  | Avg. votes per condition | Min. #votes per cond. | Total #votes |
| ------------- |:-----------:| ------:|-------------------------:|----------------------:|-------------:|
| 401 | 48 | 71 | 217 | 207 | 10412 |
| 501 | 50 | 64 | 102 | 83 | 5109 |
| 701 | 72 | 144 | 97 | 83 | 6990 |

### JSON Format
* `csXYZ_ratingsPerCondition.json`
  * condition: integer
  * ratings: [list of ratings from users with ratings on a 5-point scale (1,2,3,4,5)]
* `csXYZ_ratingsPerUser.json`
  * userid: integer
  * conditions: [list of conditions rated by the user]
  * ratings: [list of ratings for the corresponding conditions]

### CSV Format
* `csXYZ_ratingsPerCondition.csv`: The first column indicates the condition (integer). The other columns contain the ratings from all subjects. Please note that the number of votes per condition varies.  
* `csXYZ_ratingsPerUser.csv`: The CSV file contains three columns `userid, condition, ratings`

## Investigators
The investigators in this research are
* Babak Naderi, (babak.naderi@tu-berlin.de), Senior Researcher at [Quality and Usability Lab, Technische Universität Berlin](https://qu.tu-berlin.de/)
* Tobias Hoßfeld (tobias.hossfeld@uni-wuerzburg.de), Professor and head of [Chair of Communication Networks, University of Würzburg](http://www.comnet.informatik.uni-wuerzburg.de/)
* Matthias Hirth (matthias.hirth@tu-ilmenau.de), Jun.-Professor and head of [User-centric Analysis of Multimedia Data Group, TU Ilmenau](https://www.tu-ilmenau.de/en/mt-nam/)
* Florian Metzger (florian.metzger@uni-wuerzburg.de), Postdoc Researcher at the [Chair of Communication Networks, University of Würzburg](http://www.comnet.informatik.uni-wuerzburg.de/)
* Sebastian Möller, (sebastian.moeller@tu-berlin.de), Professor and head of [Quality and Usability Lab, Technische Universität Berlin](https://qu.tu-berlin.de/)
* Rafael Zequeira Jiménez, (rafael.zequeira@tu-berlin.de), Research Scientist at [Quality and Usability Lab, Technische Universität Berlin](https://qu.tu-berlin.de/)

## Copyright Notice
This database is published under the license: [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/).
Permission is hereby granted, without written agreement and without license or royalty fees, to use, copy, modify, and distribute this database and its documentation for any purpose, provided that the copyright notice in its entirety appear in all copies of this database, and the original source of this database is acknowledged in any publication that reports research using this database. If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

Originial source: The following paper is to be cited in the bibliography whenever the database is used.
* **[QoMEX 2020]** Babak Naderi, Tobias Hoßfeld, Matthias Hirth, Florian Metzger, Sebastian Möller, Rafael Zequeira Jiménez, "Impact of the Number of Votes on the Reliability and Validity of Subjective Speech Quality Assessment in the Crowdsourcing Approach", 2020 Twelfth International Conference on Quality of Multimedia Experience (QoMEX)
