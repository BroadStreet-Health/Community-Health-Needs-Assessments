# The BroadStreet Institute

## Introduction

[BroadStreet Institute](http://www.broadstreet.org) is 501(c)3 nonprofit organization created by data enthusiasts during the pandemic. We believe that all people deserve access to the best information possible. At BroadStreet, we work towards community change. We strive to ensure that data is accessible, affordable, and delightful to explore. BroadStreet has thousands of members all over the country, including students, non-profit leaders, and executives of multi-state and national organizations. We are proud of our team.
 
The Community Health Needs Assessments (CHNAs) Data Project began as a pilot in 2021 and a formal project in January 2022. Over 3 years, nearly 300 volunteers reviewed Community Health Needs Assessments published by nonprofit hospitals accross the U.S. and qualitatively coded the data for public release.
 
CHNAs refer to state, tribal, local, or territorial health assessments that identify key health needs and funding priorities through systematic, comprehensive data collection and analysis. Under the Affordable Care Act (ACA), nonprofit health facilities are required to conduct CHNAs every 3 years so that these facilities can better address the most pressing public health needs in their area. By comparing health needs, priorities, and other contents, CHNAs can be systematically analyzed and geographically compared without regard to the specific health system or size.
 
Since its inception, the CHNA Track has expanded to become multiple teams focused on collecting data on important public health topics outside of the pandemic, including five data entry (DE) teams, a quality assurance (QA) team, and a data release (DR) team.

## Structure of the Dataset

Below is a list of columns that are present in the dataset and their operational definitions:
<ul>
<li><strong>Healthcare_Name:</strong> The name of the healthcare facility.</li>  
<li><strong>Street_Address:</strong> Physical location of healthcare facility.</li>	
<li><strong>City:</strong> The city where the healthcare facility is located.</li>
<li><strong>Zip_Code:</strong> The zip code where the healthcare facility is located.</li> 
<li><strong>State:</strong> The state where the healthcare facility is located.</li> 
<li><strong>Associated_Health_System:</strong> The health system the healthcare facility is associated with, if any.</li>
<li><strong>Nonprofit:</strong> Yes, No, or N/A if unknown.</li>
<li><strong>CHNA_Year:</strong> The year the CHNA report was created.</li>
<li><strong>Service_Area_Type:</strong> The “service area” refers to the geographical area served by the hospital as reported in the CHNA. A CHNA that does not define a service area as a primary or secondary service area, the service area is included as a primary service area. When a CHNA includes a primary and secondary service area, only the primary service area is included. Service areas are often defined by different types of locations, such as county, zip code, city, or town. This column identifies the way that the service area is defined in the relevant CHNA:</li>
<ul style="list-style-type:circle;">
<li><strong>List of Counties:</strong> Service area is defined solely by counties.</li> 
<li><strong>List of Zip Codes:</strong> Service area is defined solely by zip codes.</li> 
<li><strong>List of Places:</strong> Service area is defined solely by cities, villages, or towns.</li>
<li><strong>Combination of ___ and ___:</strong> Service area is defined by a combination of counties; zip codes; and/or a list of places.</li></ul> 
<li><strong>Service_Area_Counties:</strong> Counties named in the CHNA’s defined service area.</li> 
<li><strong>Service_Area_Zip:</strong> Zip codes named in the CHNA’s defined service area.</li>
<li><strong>Service_Area_Places:</strong> Cities, villages, and/or towns named in the CHNA’s defined service area.</li>
<li><strong>Health_Needs:</strong> The health needs or health concerns identified in the CHNA for that service area.</li> 
<li><strong>Health_Priorities:</strong> The health needs or health concerns determined to be a priority for funding and will be included in the implementation plan for that service area.</li>
<li><strong>CHNA_URL:</strong> The direct link to the CHNA report.</li>
<li><strong>Implementation_URL:</strong> The direct link to the corresponding Implementation Plan.</li>
<li><strong>Contact:</strong> The name/phone/email that can be used to reach the primary contact listed on the CHNA/webpage for more information about that health facility.</li></ul>

## Methods

### Data Burst Schedule: 

A data burst is a once-per-week, weekly, synchronous team meeting during which each team member works on the data collection process. During the scheduled time, the team can converse on a Zoom call with their teammates and Team Lead about issues that arise, life, and personal experiences. 

### Data Entry Process:

Every intern is assigned to one of these five teams, and each team works on collecting CHNA data from a different state. We collect data from the most recent publicly available CHNA document that can be found by our team on the hospital facility websites. CHNAs are generally updated every 3 years, so it is very important that we capture data from the most recent version. Our dataset includes CHNAs for the years 2016 - 2022. The data entry process includes navigating through CHNA documents to capture data about the service areas (counties, zip codes and cities) covered, health needs and priorities listed, and the updated links to CHNA documents and implementation plans. In some cases, implementation plans are included in the same document as CHNAs; if not, implementation plans are searched and analyzed separately. Since these documents can be very long, interns often use the ‘Ctrl+F’ function and search for keywords such as ‘service area,’ ‘health needs,’ and ‘health priorities.’ Given that no two CHNAs look alike, interns are instructed to emphasize quality over quantity as they complete their assignments. Once finished with data entry, interns record their level of confidence for the data they entered (1=very unsure, 3=questioning, 5=positive), which is taken into close consideration by the QA Team as they review the quality and accuracy of each dataset row.


### Quality Assurance Process:

To ensure data entered in the initial pass by the Data Entry teams is as accurate as possible, the CHNA Track implemented a Quality Assurance process in April 2022. The quality assurance (QA) team is composed of experienced CHNA data entry members, and is managed by a team leader. During the quality assurance process, a QA Analyst Intern reviews the data previously entered in each row of the dataset. The process is outlined as followed:
<ul>
<li>Identify whether the hospital is a non-profit, as documented on their website or external source. If the hospital is non-profit, then it is more likely a CHNA is available per ACA requirements.</li>
<li>Review the information for the hospital or health care entity’s CHNA, as researched by the data entry intern, and correct entry as applicable.</li>
<li>First review the entire row, noting the Confidence Level (as described in the Data Entry Process Section). Although all rows are reviewed, special attention is given to assignments with an intern confidence level of 3 or lower.</li>
<li>Second, QA Analyst must attempt to find the CHNA/Implementation Plan for the hospital on their own.</li>
<li>Third, QA Analyst confirms that their findings match the CHNA listed in the dataset.</li>
<ul>
<li>If the QA Analyst finds a more recent CHNA, the Analyst replaces the</li> information in the row with the more recent information</li>
<li>If the QA Analyst uses the same CHNA and Implementation plan as the Data Entry Analyst, the QA Analyst reviews each entry and confirms whether the data entered matches the CHNA, changing where appropriate.</li>
<li>All changes are recorded for internal communication via color coding</li>
<li>All rows are adjusted to standardized data entry formatting as necessary, such as using commas to separate listed entries</li></ul>
<li>If the QA Analyst still has low confidence about the CHNA data collected, add contact information to internal tracking list of “Hospitals to Be Contacted” to clarify the CHNA data</li>
</ul>

### Modifications for Data Release:

After the CHNA data in the Google spreadsheet was reviewed, updated, and quality assured by our QA team, several modifications were made to make the dataset more user-friendly for public release. These changes are listed below:
<ul>
<li>Ensuring that all entered data and dropdown menus convert to a .CSV file well</li>
<li>Deleting columns that are only relevant to internal communications during DE and QA processes (i.e. intern confidence levels, intern names, QA check boxes, color coding)</li>
<li>Shifting columns with hospital information to the front of the dataset</li>
<li>Renaming column headers for conciseness</li>
<li>Ensuring consistent punctuation in the service areas, health needs, and health priorities columns</li>
</ul>

## Data Challenges & Changes in Process
 
#### Data Challenges:
 
<ul>
<li>Variation in CHNA document format by hospital</li>
<li>Distinguishing the difference between identified community health needs and health priorities that will actually receive funding</li>
<li>Data entry decisions for long lists of categories included in CHNA documents</li>
<li>State-by-state differences</li>
<li>CHNAs formatting spectrum ranges from large, broad and ambiguous to more concentrated and detailed (Urban vs. Rural)</li>
<li>CHNAs developed for counties and geographical areas as opposed to hospitals/multiple hospitals using one CHNA</li>
</ul>
 
 
#### Process Changes:
 
<ul>
<li>Developed Quality Assurance team (April 2022)</li>
<li>Decided to review all data entered by the DE team regardless of intern confidence level</li>
<li>Standardized formatting in list entries (separation by commas)</li>
<li>Started entering information on Primary Service Area only</li>
<li>Started collecting data on the non-profit status of all health facilities</li>
</ul>

## Future Releases

Throughout the coming months, we plan to release CHNA datasets for more states throughout the country, starting with the Great Plains region. The CHNA Track is dedicated to continuous improvement as it continues to grow and serve as an increasingly prominent track under BroadStreet’s Community Data Project. To meet this goal, future releases will include data from new initiatives like organizing the wide variety in terminology used by CHNAs to identify broad categories of health needs and priorities that align with Healthy People 2030.

The CHNA Track also plans to expand by addressing two new goals. The first goal is to include visual datasets from the data visualization team that will help elucidate the relationship between geographic location and health needs and priorities. The second goal is to develop datasets that dive deeper into Implementation Plans to see how well CHNAs translate into actionable outcomes for the communities being served by each hospital or hospital system.

## Suggested Citation

When using data images, downloaded data, or shared document formats, please attribute BroadStreet as well as the original source, when applicable. For examples and more information, review this article which answers the question ["How do I cite BroadStreet?"](https://help.broadstreet.io/article/citations/)

## Contributors

Project Leaders and Data Release Team Members (listed alphabetically by last name):

Ifeoluwa Adunnade; [Kimberly Barrett, MS](https://www.linkedin.com/in/1kimberlybarrett/); [Michael Cassidy, MPH](https://www.linkedin.com/in/michaeltcassidy/); Arslon Humayun; [Brenna Jarvis, MPH](https://www.linkedin.com/in/brenna-jarvis-88b4351b6/); Nicole Kinkade; [Madison Litterell](https://www.linkedin.com/in/madison-litterell-mph-a71244217/); [Tyler Lott](https://www.linkedin.com/in/tylerowenlott/); [Kelsey Peterson](https://www.linkedin.com/in/kelsey-peterson-15476a129/); [Kari Schoettler, MPH](https://www.linkedin.com/in/kari-schoettler/); [Dipali Shah](https://www.linkedin.com/in/dipali-shah-35b14214b/); [Caitlin Shaw](https://www.linkedin.com/in/caitlin-shaw-72876a62/); [Elaine Wu](https://www.linkedin.com/in/jiaxin-wu-a12142226/).

A full list of the Broadstreet Institute volunteers can be found at [https://covid19dataproject.org/team-2/](https://covid19dataproject.org/team-2/)

## Questions / Feedback
Email the primary contributors at: hello@broadstreet.io

