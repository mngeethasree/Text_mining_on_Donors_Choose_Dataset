# Text_mining_on_Donors_Choose_Dataset

## Background:
DonorsChoose.org receives hundreds of thousands of project proposals each year for classroom projects in need of funding. Inorder to mitigate the issue of manual screening by large number of volunteers, a machine learning model can be leveraged to identify projects most likely to need further review before approval.

## Objective:

This project aims to predict if a project proposal submitted by a teacher will be approved, considering information regarding project descriptions, resource summaries, additional metadata about project, teacher and school.

| Feature | Description |
|----------|:--------:|
| project_id   | unique identifier   |
| project_title   | title of project   |
| project_grade_category   | Grade level of students for which the project is targeted   |
| project_subject_categories   | Subject categories for each project   |
| school_state   | State where school is located   |
| project_subject_subcategories   | Subject subcategories for each project   |
| project_resource_summary   | explaination of resources requested   |
| project_essay_1   | First Application Essay   |
| project_essay_2   | Second Application Essay   |
| project_essay_3   | Third Application Essay   |
| project_essay_4   | Fourth Application Essay   |
| project_submitted_datetime   | date application was submitted   |
| teacher_id   | Unique id for teacher   |
| teacher_prefix   | Teacher's title   |
| teacher_number_of_previously_posted_projects   | Number of applications previously submitted by the same teacher   |

## Exploratory Data Analysis:

**1. Percentage of proposals accepted:** <br>

<img width="330" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/78888a2e-f58c-4dd8-859f-319b2d86f0d0">
<img width="375" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/d3f56d7f-3d3d-404c-959f-c4c03e95f6cf"> <br>

Only **~15%** of the proposals are not approved for funding. 

**2. Percentage of approved proposals displayed at state level:** <br>

<img width="533" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/a9d2e97a-b2bf-4a49-a6d7-c21859eb0932"> <br>

Proposals from california state have higher approval rates than other states. <br>

**3. Word Count of Project title in Approved vs Rejected Projects:** <br>

<img width="242" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/a6e8635f-d74b-4974-8d99-89fdf39cdea9"> <br>
<img width="387" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/03b2dfa4-4470-411b-a979-af283a6b7dd7"> <br>

Approved proposals have slightly longer project titles than Rejected proposals. <br>

**3. Cost of project comparison for Approved vs Rejected Projects:** <br>

<img width="377" alt="image" src="https://github.com/mngeethasree/Text_mining_on_Donors_Choose_Dataset/assets/68059811/cb755979-5bfa-4808-b087-cc446135b108"> <br>

No significant difference in project costs between Approved and Rejected Projects.

## PreProcessing Text features:

**Categorical features:** <br>
1. Features like project_grade_category, project_subject_categories, teacher_prefix, project_subject_subcategories, school_state are cleaned to minimize the redundancy in category names. <br>
2. Features like project_title, project_essay_1, project_essay_2, project_essay_3, project_essay_4, advanced text processing is performed as they can contain multiple words and/or sentences. Few such examples are, <br>
   a. Using a custom stop word list to remove words that are of no value <br>
   b. Decontracting phrases to actual phrases. For example, after decontraction of a word like **I'll**, we obtain **I will** <br>

**Numerical features:**
Numerical features like price and quantity are available in 'resources.csv' which need to first aggregated by resource_id before merging with preprocessed text data. <br>
Standard scaler and MinMax scaler are then used to normalize these numerical values. <br>




