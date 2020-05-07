# adv_soft_eng


# Presentation

The meeting started with a round table, people presented themselves and the role they hold 
in their work package. The people present were :

PAL

* Sara
* Luca

INRIA

* Matthieu
* Soraya
* Alex


HWU

* Daniel 
* Nancie
* Oliver 
* Weronika
* Yanchao


BIU

* Sharon 
* Pinchas

CVUT

* Stan

APHP

* Etienne
* Samuel

UNITN

* Paolo

ERM

*  Florian
*  Pascal

Probably a couple of people missed in this list that I could not identify.

# Agenda presentation

We then proceeded to present the topics, and the tasks:

* T1.1 (APHP): Privacy and Ethics (contr): INRIA, ERM). M1-M48
* T1.2 (ERM): Initial Data Collection (contr:CVUT, HWU, BIU, APHP). M1-M12
* T1.3 (ERM): Preliminary Experimental Validation (contr: INRIA, UNITN, CVUT, HWU, BIU). M4-M18
* T7.1 (PAL): Robot Customisation Design (contr: CVUT, BIU). M1-M3
* T7.2 (PAL): Platform Manufacturing, Validation and Deployment (contr: CVUT, BIU). M4-M8
* T7.3 (PAL): Preliminary Software Integration Cycle (contr: INRIA, UNITN, CVUT, HWU, BIU, ERM). M4-M15



# Topic discussions

*	Sara (PAL) lists the tasks of WP1, highlighting the recent deliverable of T1.1 Privacy 
    and Ethics. PAL will look forward to feedback from the risk assessment and is aware 
	that further robot testing needs to be done (maximum possible impacts to tilt robot, 
	etc) and overall a more in-depth analysis
    *	APHP mentions that due to the COVID19 situation data collection at hospitals will 
	    be delayed
	*	Due to technical issues ERM was not present at this section, therefore no further 
	    points were raised
*	Sara (PAL) summarises the outcomes of D7.1 on ARI Robot specifications, displaying 
    the output of the torso fisheye and head RGB-D cameras
	*	Stan (CVUT) mentions they would be interested in getting calibration data of the 
	    cameras once they have been integrated in the ARIs, with just an empty office
*   The microphone array issue is still unresolved, right now ARI’s are being manufactured 
    with a hole on the front cover so that different boards may be evaluated. 
    *	Sharon (BIU) suggests that they can already evaluate audios from the current ARI 
	    audio set-up with the ReSpeaker following a set testing procedure. Right now it 
		is still not possible to proceede with CEVA board testing and its size is a major 
		limitation. A separate meeting will be arranged between PAL and BIU to pick up 
		the discussion
*	T7.2: ARI robot manufacturing. Sara (PAL) indicates that the manufacturing of the 
    robots is going smoothly, with covers missing, and that PAL expects to have them 
	finished on time. Any delays on the delivery and deployment at partner sites, as well 
	as the integration week, are subject to travel regulations.
*	Sara (PAL) suggests the use of ARI simulator in the mean while (wiki.ros.org/Robots/ARI) 
    which runs on an Ubuntu PC or Docker. Several issues and suggestions were made by partners:
    *	Sharon and Pinchas (BIU) would like to be able to simulate audio
    *	Alex and Soraya (INRIA) feel the Gazebo is not running as smoothly as it should. 
	    Further indications on the tutorials may be needed from PAL’s side, especially 
		when using the simulation on a Docker
*	T7.4 Continuous Integration:  Sara (PAL) summarises what was discussed in a previous 
    meeting with INRIA. It is still undecided whether we will use INRIA's internal gitlab 
	or public gitlab. It would be most suitable to have one project per WP, and a 
	maintainer for each to revise and accept changes.
	*	Sharon (BIU) asked how they can start developing audio software without the robot 
	    or audio simulation. Luca (PAL) proposes several options:
		*	Use ROS’s rosbag for audio processing, analysis and test: create infrastructure 
		    for recording rosbag of audio, playback this recorded messages, and interface 
			audio processing algorithm with ROS topic interfaces.
		*	Enable realistic audio simulation in Gazebo by extending the current simulation 
		    environment for providing the audio input that can later be processed on the 
			simulator as we would do on the real robot
		*	Inject audio as an external plugin, external process running in parallel with 
		    the simulation
*	Necessary to have a dataset of robot inputs so that partners can begin working on their 
    software (provided by PAL)




# Next

In order to begin with the software development required by the tasks PAL will start generating a 
dataset of ARI images, rosbags, audio to share with partners. It remains to be decided where the 
datasets will be stored. Further details on ARI simulation set-up and optimisation may be needed 
by PAL to include in the tutorials. A separate meeting will be held to pick up the microphone
array and audio testing between BIU and PAL. 
