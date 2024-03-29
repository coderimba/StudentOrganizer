# Student Organizer

## Never miss a deadline again!

*Student Organizer* aims to help university students keep track of their never-ending pile of assignments. In light of the COVID-19 pandemic, it has come to my attention that many of my peers are struggling to stay organized, leading to them feeling overwhelmed. This application will help reduce levels of anxiety by allowing students to do the following:
- add new assignments and include
	- a course code (e.g. CPSC 210)
	- a due date
	- an estimated time for completion
- sort outstanding assignments by their fields
- mark assignments as complete

Start using *Student Organizer* today and **never miss a deadline again!**

## User Stories
- As a user, I want to be able to add an assignment to my student organizer
- As a user, I want to be able to delete an assignment from my student organizer
- As a user, I want to be able to mark an assignment as complete in my student organizer
- As a user, I want to be able to view the list of all assignments sorted by course code in my student organizer
- As a user, I want to be able to view the list of incomplete assignments sorted by course code in my student organizer
- As a user, I want to be able to view the list of incomplete assignments sorted by the due date in my student organizer
- As a user, I want to be able to view the list of incomplete assignments sorted by estimated time for completion in my student organizer
- As a user, I want to be able to save my student organizer to file
- As a user, I want to be able to load my student organizer from file

## Phase 4: Task 2
- Chose to test and design the Assignment class in the model package such that it is robust
- The methods with a robust design in the Assignment class are:
    - setName(String name)
    - setCourseCode(String courseCode)
    - setDueDate(String dueDate)
    - setEstimatedHours(double estimatedHours)
    
## Phase 4: Task 3
Refactoring I would do to improve my design:
- From StudentOrganizerPanel, extract the loadData and saveData fields and the createMenuBar() and actionPerformed(ActionEvent e) methods into a new class "StudentOrganizerMenu", which will be in the ui package
- StudentOrganizerMenu will implement ActionListener (StudentOrganizerPanel will no longer implement ActionListener)
- There will be a bi-directional association between StudentOrganizerPanel and StudentOrganizerMenu, with a multiplicity of 1 on both ends
- The bi-directional association will allow assignments to be loaded to and saved from the StudentOrganizerPanel when the respective menu items in StudentOrganizerMenu are triggered