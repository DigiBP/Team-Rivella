# Team - Rivella - The Digitalisation of Business Processes in Clinical Trials
![_82635ccd-6750-4688-8faa-274657f6dd49](https://github.com/DigiBP/Team-Rivella/assets/149072194/d2bd0693-bb4b-44e5-b34f-d3c5f186c4ca)

- [Team Members](#team-members-👨🏽‍⚕👨🏽‍⚕️👩🏻‍⚕️👨🏽‍⚕️) 
- [Coaches](#coaches) 
- [Introduction](#introduction)
-



## Team-Members👨🏻‍⚕️👨🏼‍⚕️👩🏻‍⚕️👨🏽‍⚕️
|Name|Email|
|----------|---------------|
|Prerna Duhan|prerna.duhan@students.fhnw.ch|
|Marco De Luca|marco.deluca@students.fhnw.ch|
|Gabriel Flückiger|gabriel.flueckiger@students.fhnw.ch|
|Tim Frietsch|tim.frietsch@students.fhnw.ch|

## Links🔗
- API Deepnote(Latest Version): 
- Camunda Model:
- Make (1):
- Make (2):
- Google Forms (Informed Consent Form):
- Google Sheet (Patient Database):  


## Coaches
- Charuta Pande
- Andreas Martin

## Introduction 

Clinical research involves the examination of various elements related to a disease, such as its symptoms, risk factors, and pathophysiology. Clinical Trials are interventional investigations conducted on human volunteers and patients to evaluate the effectiveness of a therapetuic drug or medical device (Kandi & Vadakedath, 2023). Clinical trials include various phases starting from Phase 0, performing pharmacokinetic and pharmacodynamic analysis. Phase 1 is conducted in 10-100 healthy volunteers to to establish safety and the maximum tolerated dose (MTD). Phase 2 trials is conducted in a sample size of 100-300 patients, to establish the efficacy of the medical intervention. Phase 3 trials are conducted on 1000-3000 patients to confirm the safety and efficacy, and establish the efficacy of the drug. Finally, in Phase 4 post-marketing studies, the drug effect is monitered in the real world to determine drug-drug interactions and drug-disease interactions. 

Business process modelling has been recognized as an important means in the reorganization of management processes, and there are considerable opportunities to automate Clinical trial workflows. Through our research, we have determined that optimizing and digitalizing clinical trials could potentially: 
- Improve Flexibility
- Increase Patient Recruitment
- Reduce paper and manual workload
- Shorten Clinical Trial Timelines
- Reduce Costs


### Project Goals

Automation and optimization of the patient screening and patient recruitment process in Phase 1 clinical trials 


## Camunda Process

### Benefits

### Technologies
- Camunda
- Make
- Google Sheets
- Google Forms
- 

### Process Flow 

### Make Scenarios

1. Sending an Email: Are you eligible for this clinical trial?
![Screenshot 2023-12-05 211140](https://github.com/DigiBP/Team-Rivella/assets/149072194/7195242d-ede7-4f7e-96a7-7727d3de0821)

2. Fill out Informed Consent Form (ICF) and add information to the patient database (Google sheet), data base updating 
Clinical trial participation conformation  
![Screenshot 2023-12-05 210233](https://github.com/DigiBP/Team-Rivella/assets/149072194/36a79d03-38b8-4eaa-bdf4-1a105426e3b1)

### External worker - check study eligibility based on EHR data
- The external worker accesses the EHR API based on user & password input.
- Client side, fetches patient information
- Update url according to api url

### Flask API - acting as EHR database
- Simulates EHR database, providing patient medical records to users with password access.
- The API routes are secured by JWT authentication. Using JWT authentity the user only receives the medical data he's allowed to access.
- Getting basic patient information such as last name, first name, date of birth can be achieved via "/patient_data". Lab data can be accessed via "/lab_data".

## Conclusion

![_562d77fa-c84d-4f87-baeb-c97dc1ce00d4](https://github.com/DigiBP/Team-Rivella/assets/149072194/9abccddc-c1ed-4577-acbd-eff3f78e1205)



## References 
1. Kandi, V., & Vadakedath, S. (2023). Clinical trials and clinical research: A comprehensive review. Cureus, 15(2). https://doi.org/10.7759/cureus.35077
2. Rohilla, A., Singh, R. K., Sharma, D., Keshari, R., & Kushnoor, A. (2013). Phases of clinical trials: A review. Ijpcbs.com. https://www.ijpcbs.com/articles/phases-of-clinical-trials-a-review.pdf


## Disclaimer 
- 

 





