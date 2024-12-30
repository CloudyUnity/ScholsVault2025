
> [!question]- #schols [2024] ![[Pasted image 20241027203514.png]]
(a)
Student
`+Name : String`
`+Age : int`
`-Issue : String` 
`+getIssue() : String`
.
HealthcareWorker
`+Name : String`
`-StartHour : Time`
`-EndHour : Time`
`+CanDoAppointment(app : Appointment) : boolean`
.
Receptionist
`+Name : String`
`-StartHour : Time`
`-EndHour : Time`
`+TryScheduleAppointment(schedule : Schedule, patient : Student) : boolean`
.
Doctor
`+QualifiedForSurgery : boolean`
`+QualifiedForAnasthetic : boolean`
`+QualifiedForEndocrinology : boolean`
`+TreatPatient(patient : Student) : void`
`+PrescribeMedication(patient : Student) : void`
.
Appointment
`+DateOf : Date`
`+TimeOf : Time`
`+Patient : Student`
`+Worker : HealthcareWorker`
`+IsValid() : boolean`
.
Schedule
`-AppointmentMap : Hashmap<DateTime, Appointment>`
`-AvailableWorkerMap : Hashmap<DateTime, Worker>`
`+CheckConflicting(app : Appointment) : boolean`
`+TryPlaceAppointment(app : Appointment, dateTime : DateTime) : boolean`
..
Doctor inherits/generalises from HealthcareWorker
`0..*` Appointment aggregates into `1` Schedule 
`0..*` Student is associated to `1..*` Doctor
`1` Appointment is associated to `1` Student
`1` Receptionist depends on `1` Schedule
.
(b)
Student has `Apply for Appointment`
Receptionist has `Schedule Appointment`
Doctor has `Treat Patient`
- (c) Student
	```xml
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE Students [
	<!ELEMENT Student (Students*)>
	<!ELEMENT Student (Issue+)> <!-- Students can have multiple issues --!>
	<!ELEMENT Student (Name, Age)>
	<!ATTLIST Student StudentNumber ID #REQUIRED> <!-- Students all have student numbers --!>
	<!ELEMENT Name (#PCDATA)>
	<!ELEMENT Age (#PCDATA)>
	]>
	<Students>
		<Student StudentNumber=23373087>
			<Name> Fiona Wright </Name>
			<Age> 20 </Age> 
			<Issue> The transgenda </Issue>
			<Issue> Too "cool" </Issue> 
			<Issue> Ego </Issue>
		</Student>
		<Student StudentNumber=88888888>
			<Name> 8 Man </Name>
			<Age> 8 </Age> 
			<Issue> Illiterate </Issue>
		</Student>
		<Student StudentNumber=69696969>
			<Name> John Johnson </Name>
			<Age> 31 </Age> 
			<Issue> Immature </Issue>
		</Student>
	</Students>
	```
- (c) Appointment
	```xml
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE Appointments [
	<!ELEMENT Appointments (Appointment*)>
	<!ELEMEMT Appointment (DateOf, TimeOf, Patient, HealthcareWorker+)> <!-- A patient can be treated by multiple healthcare workers --!>
	<!ATTLIST Patient StudentNumber ID #REQUIRED>
	<!ELEMENT DateOf (#PCDATA)>
	<!ELEMENT TimeOf (#PCDATA)>
	<!ELEMENT Patient (#PCDATA)>
	<!ELEMENT Worker (#PCDATA)>
	]>
	<Appointments>
		<Appointment>
			<DateOf> 05/12/24 </DateOf>
			<TimeOf> 12:02pm <TimeOf> 
			<Patient StudentNumber=23373087> Fiona Wright </Patient>
			<HealthcareWorker> Dr. Fixa </HealthcareWorker>
		</Appointment>
		<Appointment>
			<DateOf> 23/11/24 </DateOf>
			<TimeOf> 3:00am <TimeOf> 
			<Patient StudentNumber=88888888> 8 Man </Patient>
			<HealthcareWorker> Dr. English </HealthcareWorker>
			<HealthcareWorker> Dr. Numbers </HealthcareWorker>
		</Appointment>
	</Appointments>
	```
- (c) Doctor
	```xml
	<?xml version="1.0" encoding="UTF-8"?>
	<!DOCTYPE Doctors [
	<!ELEMENT Doctors (Doctor*)>
	<!-- See below how Doctor generalises from HealthcareWorker --!>
	<!ELEMENT Doctor (QualifiedForSurgery?, QualifiedForAnasthetic?, QualifiedForEndocrinology?, HealthcareWorker.Name, HealthcareWorker.StartHour, HealthcareWorker.EndHour)> <!-- Qualifications are optional. Not included is the same as false --!>
	<!ATTLIST Doctor id ID #REQUIRED> <!-- All doctors have ids --!>
	<!ELEMENT QualifiedForSurgery (#PCDATA)>
	<!ELEMENT QualifiedForAnasthetic (#PCDATA)>
	<!ELEMENT QualifiedForEndocrinology (#PCDATA)>
	<!ELEMENT HealthcareWorker.Name (#PCDATA)>
	<!ELEMENT HealthcareWorker.StartHour (#PCDATA)>
	<!ELEMENT HealthcareWorker.EndHour (#PCDATA)>
	]>
	<Doctors>
		<Doctor id=2093>
			<HealthcareWorker.Name> Dr. Fixa </HealthcareWorker.Name>
			<HealthcareWorker.StartHour> 9:00am </HealthcareWorker.StartHour>
			<HealthcareWorker.EndHour> 5:00pm </HealthcareWorker.EndHour>
			<QualifiedForEndocrinology> true </QualifiedForEndocrinology>
		</Doctor> 
		<Doctor id=8888>
			<HealthcareWorker.Name> Dr. English </HealthcareWorker.Name>
			<HealthcareWorker.StartHour> 1:00am </HealthcareWorker.StartHour> 
			<HealthcareWorker.EndHour> 8:00am </HealthcareWorker.EndHour>
			<QualifiedForSurgery> true </QualifiedForSurgery> 
		</Doctor> 
	</Doctors>
	```
- (d) Get all doctors available during appointment time
	```xquery
	for $doctor in doc("doctors.xml")/Doctors/Doctor
	let $appointment := doc("inputAppointment.xml")/Appointment
	let $appTime := xs:time($appointment/TimeOf/text())
	let $doctorStart := xs:time($doctor/HealthcareWorker.StartHour/text())
	let $doctorEnd := xs:time($doctor/HealthcareWorker.EndHour/text())
	where $appTime ge $doctorStart and $appTime le $doctorEnd
	return $doctor
	```
- (d) Get valid students (Age > 16)
	```xquery
	for $student in doc("students.xml")/Students/Student
	where $student/Age >= 16
	return $student
	```
- (d) Get all current appointments based on current time
	```xquery
	declare variable $curTime as xs:string external;
	for $app in doc("appointments.xml")/Appointments/Appointment
	where $app/TimeOf/text() = $curTime
	return $app
	```

> [!question]- #schols [2023] ![[Pasted image 20240909164204.png]]
UML is very useful for both of these practises. It can be used to understand and learn about the given domain and explain the design to all interested parties. 
Use case diagrams are very useful for showing how each key actor interacts with the system and the different functionalities of the design. They can be used to mock-up and plan the overarching system alongside research. In this phase of development mistakes are almost free and UML makes it easy to experiment and iterate quickly. Use case diagrams are also extremely readable, large subsystems can be encapsulated within use cases to hide the messy details to uninterested stakeholders. Stakeholders can also quickly see who is involved in the systems operations and what kind of functionality will be required. Shareholders can mock-up business expense estimates from the diagram and software developers can begin to understand what functions or applications will be required for the system. 
.
Class diagrams are also useful as they are an efficient plan for the software part of the design. The idea is to figure out the overall structure of the codebase before you begin production, this can help to reduce wasted time on unnecessary features/classes/functions and suboptimal code structure. For teams it is also very beneficial to communicate ideas, without UML miscommunication could occur and people would have different views of what the codebase should look like in their heads. Class diagrams are very important as they also plan out how relevant data should be stored in databases or otherwise. Particularly with regards to XML, class diagrams can have a direct translation which makes the move from pre-production to production very swift and painless. 
.
In conclusion UML is very powerful when designing large information systems. It is an efficient way to conduct research and understand the domain as well as helping to communicate the concepts and ideas to all relevant stakeholders.

#schols [2022]
![[Pasted image 20240909164359.png]]

> [!question]- #schols [2020] ![[Pasted image 20240909164740.png]]

(a)
Pilot
`+name : String`
`+age : int`
.
Flightpath
`+startAirportCode : String`
`+endAirportCode : String`
.
Flight
`+flightPath : Flightpath*`
`+pilot : Pilot*`
`+departTime : Time`
`+plane : Plane*`
.
DepartureTracker
`+flights : Flight[]`
`+GetNextDeparture() : Flight`
`+GetTimeOfDeparture(endAirportCode : String) : Time`
.
Plane
`+model : String`
`+capacity : int`
`+fuelLevelPercent : double`
.
PrivatePlane
`+mphSpeed : float`
`+owner : String`
..
`0..*` Flight aggregates into `1` DepartureTracker
`1` Pilot associates with `1` Flight
`1` Flightpath associates with `1` Flight
`1` Pilot depends on `1` Plane
PrivatePlane is generalised from Plane
.
(b)
Passenger has use case `View Departure Tracker` supported by DepartureTracker
Pilot has use case `Fly Plane to Destination` supported by Plane
.
(c)
![[Pasted image 20241208125655.png]]
.
(d)
```xml
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE Passenger [
<!ELEMENT Passenger (Name, Age)>
<!ATTLIST Passenger id ID #REQUIRED>
]>
<!DOCTYPE Flightpath [
<!ELEMENT Flightpath (StartAirportCode, EndAirportCode)>
<!ATTLIST Flightpath id ID #REQUIRED>
]>
<!DOCTYPE Flight [
<!ELEMENT Flight (Flightpath, Pilot, DepartTime, Plane)>
<!ATTLIST Flight fuckthisshit
]>
```

#schols [2019]
![[Pasted image 20240909164825.png]]

#schols [2018]
![[Pasted image 20240909164904.png]]

#schols [2017]
![[Pasted image 20240909164942.png]]

#schols [2016]
![[Pasted image 20240909165026.png]]
![[Pasted image 20240909165120.png]]

#schols [2015]
![[Pasted image 20240909165235.png]]

#schols [2014]
![[Pasted image 20240909165559.png]]

#schols [2013]
![[Pasted image 20240909165704.png]]