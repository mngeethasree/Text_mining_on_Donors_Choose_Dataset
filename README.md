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
