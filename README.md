# Team - Rivella - The Digitalisation of Business Processes in Clinical Trials
- [Team Members](#team-members-👨🏻‍⚕️👨🏼‍⚕️👩🏻‍⚕️👨🏽‍⚕️) 
- [Coaches](#coaches) 
- [Introduction](#introduction)
- [Project Goals](#project-goals)
- [Process Flow](#process-flow)  
- [How to run](#how-to-run)
- [To-Be Process](#to-be-process)
- [Make Scenarios](#make-scenarios)
- [Flask API - acting as EHR database](#flask-api-acting-as-ehr-database)
- [Technologies](#technologies)
- [Conclusion](#conclusion)
- [References](#references)
- [Disclaimer](#disclaimer)

![_82635ccd-6750-4688-8faa-274657f6dd49](https://github.com/DigiBP/Team-Rivella/assets/149072194/d2bd0693-bb4b-44e5-b34f-d3c5f186c4ca)

## Team Members👨🏻‍⚕️👨🏼‍⚕️👩🏻‍⚕️👨🏽‍⚕️
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

## Introduction 🔍

Clinical research involves the examination of various elements related to a disease, such as its symptoms, risk factors, and pathophysiology. Clinical Trials are interventional investigations conducted on human volunteers and patients to evaluate the effectiveness of a therapetuic drug or medical device (Kandi & Vadakedath, 2023). Clinical trials include various phases starting from Phase 0, performing pharmacokinetic and pharmacodynamic analysis. Phase 1 is conducted in 10-100 healthy volunteers to to establish safety and the maximum tolerated dose (MTD). Phase 2 trials is conducted in a sample size of 100-300 patients, to establish the efficacy of the medical intervention. Phase 3 trials are conducted on 1000-3000 patients to confirm the safety and efficacy, and establish the efficacy of the drug. Finally, in Phase 4 post-marketing studies, the drug effect is monitered in the real world to determine drug-drug interactions and drug-disease interactions. 

Business process modelling has been recognized as an important means in the reorganization of management processes, and there are considerable opportunities to automate Clinical trial workflows. Through our research, we have determined that optimizing and digitalizing clinical trials could potentially: 
- Improve Flexibility
- Increase Patient Recruitment
- Reduce paper and manual workload
- Shorten Clinical Trial Timelines
- Reduce Costs

A major contributor to clinical trial delays and a failure to reach clinical research targets is not reaching patient recruitment targets. Our research indicates that leveraging digital strategies for patient recruitment in clinical trials can expedite the recruitment process and potentially mitigate trial delays (Katz et. al., 2019). Digitalzed patient recruitment is not only more time-efficient but also more cost-effective compared to traditional offline methods (Brøgger-Mikkelsen et.al., 2020).  

### Project Goals 🎯

Automation and optimization of the patient screening and patient recruitment process in Phase 1 clinical trials by leveraging data from the patient's electronic health record (EHR).

## Process Flow 

### How to run 🚀
1. Start (User Information)
2. Open 
3. User tasks and Recieving Emails

### Issues with the current Clinical Trial process 🐛
1. Patient Engagement and Communication:
- Limited patient awareness and engagement in clinical trials.
- Ineffective communication between researchers, sponsors, and participants.
  
2. Technological Integration:
- The need for better integration of technology in the clinical trial process, including electronic health records (EHRs) and digital data collection methods.
  
3. Costs and Resource Allocation:
- High costs associated with clinical trial conduct and management.
- Efficient allocation of resources, including personnel and funding.

4. Complex Protocols:
- Overly complex study protocols that can lead to challenges in execution and understanding.

### To-Be Process

<img width="1100" alt="MicrosoftTeams-image (2)" src="https://github.com/DigiBP/Team-Rivella/assets/149072194/7ba7bd1a-8985-4c69-9eac-e6d4ab0d2d0e">


### Make Scenarios

1. Sending an Email: Are you eligible for this clinical trial?
 An email is sent to a potential volunteer, "Do you want to participate in Clinical Trial 1?". Once the potential volunteer provides their consent, their eligibility for the participating in the trial is checked.

![Screenshot 2023-12-05 211140](https://github.com/DigiBP/Team-Rivella/assets/149072194/7195242d-ede7-4f7e-96a7-7727d3de0821)

2. Clinical trial participation conformation  
Once the elgibility of the volunteer is confirmed, they recieve an Informed Consent Form (ICF) to fill out. Their information is stored on a patient database in a tabular form automatically. The database updates every 15 minutes to check for new changes.

![Screenshot 2023-12-05 210233](https://github.com/DigiBP/Team-Rivella/assets/149072194/36a79d03-38b8-4eaa-bdf4-1a105426e3b1)

### Flask API - acting as EHR database
Simulates EHR database, providing patient medical records to users with password access. The API routes are secured by JWT authentication. Using JWT authentity the user only receives the medical data he's allowed to access. Getting basic patient information such as last name, first name, date of birth can be achieved via "/patient_data". Lab data is accessed via "/lab_data".


### External worker - check study eligibility based on EHR data
The external worker is provided with a username, password, EHR API URL and clinical trial number through camunda input. The external worker executes a post request to retrieve the user-specific access token from the EHR API. This authentication token is then used to access and retrieve patient-specific EHR data.
In a second step, the patient's medical history is extracted and compared with the specific requirements of the clinical trial. If the requirements of the study are met, the patient is classified as eligible. Basic patient information (patient ID, name, date of birth) and study eligibility are sent back to the camunda process as variables.

Depending on the clinical trial number, this worker can quickly and easily assess patient eligibility.

### Benefits ✅
1. Potentially shortens clinical trial timelines
2. Increases volunteer and patient engagement in Phase 1 safety trials
3. Reduces clinical trial management and conduct costs
4. Leverages technology

### Technologies 🌐
- Camunda
- Make
- Google Sheets
- Google Forms
- Deepnote (for Python programming - Flask API / External worker)


## Conclusion
![_562d77fa-c84d-4f87-baeb-c97dc1ce00d4](https://github.com/DigiBP/Team-Rivella/assets/149072194/9abccddc-c1ed-4577-acbd-eff3f78e1205)

Through this project, under the leadership of our coaches Andreas Martin and Charuta Pande, our team aimed to optimize and shorten Phase 1 clinical trial timelines by improving patient recruitment timelines. The current clinical trial process requires a lot of manual documentation and screening patients singularly in a time consuming manner. To overcome these challenges, we introduced an automated and digitalized patient screening and patient recruitment workflow, which is cost-effective and easy to integrate. This ease would push for online recruitment campaigns that would be primary strategies to maximize recruitment rates. 
We hope to integrate this model for larger Phase 2, Phase 3 and Phase 4 clinical trials, additionally automating other clinical trial documentation and regulatory documentation. This would create a centralized system for clients and regulators to integrate in their companies, ensuring effective communication between patients and stakeholders. 

In conclusion, a digitalized and automated patient screening and recruitment process can effectively shorten clinical trial timelines, providing patients with efficacious drugs in a timely manner. 

## Acknowledgments 🙏
We are grateful to our incredible coaches and mentors, Andreas Martin and Charuta Pande. Thank you for generously sharing your knowledge, wisdom, and expertise, helping us improve our process through each stage. 

## References 📚
1. Kandi, V., & Vadakedath, S. (2023). Clinical trials and clinical research: A comprehensive review. Cureus, 15(2). https://doi.org/10.7759/cureus.35077 
2. Rohilla, A., Singh, R. K., Sharma, D., Keshari, R., & Kushnoor, A. (2013). Phases of clinical trials: A review. Ijpcbs.com. https://www.ijpcbs.com/articles/phases-of-clinical-trials-a-review.pdf 
3. Katz, B. E., Aleksander, E., Valerija, M., & Zibert, J. R. (2019, January 4). Optimize clinical trial recruitment with digital platforms. Dermatology Times. https://www.dermatologytimes.com/view/optimize-clinical-trial-recruitment-digital-platforms 
4. Brøgger-Mikkelsen, M., Ali, Z., Zibert, J. R., Andersen, A. D., & Thomsen, S. F. (2020). Online patient recruitment in clinical trials: Systematic review and meta-analysis. Journal of Medical Internet Research, 22(11), e22179. https://doi.org/10.2196/22179 
5. Pufahl, L., Zerbato, F., Weber, B., & Weber, I. (2022). BPMN in healthcare: Challenges and best practices. Information Systems, 107(102013), 102013. https://doi.org/10.1016/j.is.2022.102013 

## Disclaimer 📝
1. This project is a digitalized clinical trial project that involves the collection, processing, and storage of sensitive volunteer and patient data.
2. All data collected as part of this clinical trial is treated with the utmost confidentiality and is securely stored.
Participation in this clinical trial is voluntary, and participants have the right to withdraw at any stage.By participating, volunteers and patients acknowledge and consent to the collection and processing of their sensitive data for research purposes.
3. Data collected as part of this clinical trial is used solely for research purposes and will not be sold or shared with third parties for commercial purposes.
4. For questions or concerns regarding data privacy and security, participants can contact gmake7896@gmail.com


 





