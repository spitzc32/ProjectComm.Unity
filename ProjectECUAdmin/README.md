![logo](images/HeadECU.jpg)

 
## About
Head ECU is one of the roles in [Project ECU](https://github.com/spitzc32/Project-ECU) that mainly acts as a server in a distributed server system. It is mainly focused on the Information and Volunteer Services side of the whole Community. It regulates the necessary level of cooperation and information needed to be passed incase an emergency request or an event needing a volunteer occurs. You can see them in the Home Panel in the announmcent Page when you use pawn ECU or if any notifications you receive has an update or announcement attached to it.       

## How it Works
There are two roles it mainly plays: one is an announcer for important events or happenings and two, is a host to cooperation of our pawns. Using OneSignal API, it distributes the information locally obtained to update the pawns of either an announcement or an update to the happenings around the community. The boundaries are then decided by [Geopy](https://geopy.readthedocs.io/en/stable/), a Python client for locating which pawns are going to be notified inside the domain set of the Head.           

![Pic1](images/Head.png)

This is the basic flow of the Head on which, as mentioned before, mainly focuses on the Volunteering and Information Services. We can see the information being gathered here is being stored as an update like a ledger that keeps on track the ongoing events or requests if it is within the vicinity of the Head. The same goes for the Pawns. The Volunteer Pawns here are being deployed and used incase of an important matter where the other pawns direly need them.


### Who can use Head ECU?
This website is intended for the use of the head or someone in charge of the community that can deploy volunteers and frontliners that can help a person in need. The person who can use this website can be a head of an organization that sets out to help a particular area as long as it is nearby their vicinity. For establishments and partnered hospitals see the other folders in the source code and for individual users please use the application.

### Getting Started
Before proceeding please do the prerequisites in [Project ECU](https://github.com/spitzc32/Project-ECU). Those are the dependencies needed in order for this web application to work. Also do take note that each page has its specified purpose please read their usage in each of their source code before using it. This web application runs on local host port 5000. Make sure that any other service that uses this port are turned off. 

#### Setup
Please follow the prerequisites in [Project ECU](https://github.com/spitzc32/Project-ECU) before running the program.There are numerous setup of credentials and API keys in numerous files namely: 

In app.py, there are numerous comments that states where they are using the API keys and credentials for the database and also the file given to you. First of all let us set up the **firebase-sdk.json** that was given during the submission.

```
#first of all please go to this directory of the file.

cd ProjectECUAdmin

# Then add a copy of firebase-sdk.json in this directory.
```
In **oneSignalAppID**, paste the credential named **firebaseConfig** in this comment
```
oneSignalAppID= "" #paste oneSignalAppID here
```
In **app.py**, paste the credential named **firebaseConfig** in this comment
```app.py
firebaseConfig = {} # Paste firebaseConfig Credentials here
```
In databaseURL, paste the credential named **dbURL**
```app.py
firebase_admin.initialize_app(cred,{
	'databaseURL': '' # Paste firebaseConfig Credentials here
	}) 
```
In **index.html**, paste the credential named **firebaseConfig** in this comment
```
var firebaseConfig = {}; // Paste firebaseConfig Credentials here
```
In **index.html**, paste the credential named **googleAPIkey** in this comment
```
 src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap&libraries=&v=weekly" // Paste firebaseConfig Credentials here
```
In **Volunteer.html**, paste the credential named **firebaseConfig** in this comment
```
var firebaseConfig = {}; // Paste firebaseConfig Credentials here
```
In **Volunteer.html**, paste the credential named **googleAPIkey** in this comment
```
 src="https://maps.googleapis.com/maps/api/js?key=YOUR_API_KEY&callback=initMap&libraries=&v=weekly" // Paste firebaseConfig Credentials here
```








#### Running the Application
After doing the prerequisites in [Project ECU](https://github.com/spitzc32/Project-ECU), run the program in cmd with the following command. This instruction is for windows users only. 

```running
cd ProjectECUAdmin

python app.py
```

On the application, You will need to register as a Head Account. Please be notified that only a handful of users may sign in as the Head. If you are the head of an organization, see to it that there is only one centralized controller on your vicinity.









