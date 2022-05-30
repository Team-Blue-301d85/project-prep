## Vision

What is the vision of this product?

- To provide a study tool for Code 301 students, that will help them to retain and practice with the terms they learn throughout the course.

What pain point does this project solve?

- This solves the difficulty students may have finding one central resource for all terms and concepts they have learned for the course.

Why should we care about your product?

- It will help students to understand the material, will help instructors to provide a good resource to students and reduce some of their own workload, and will help ensure students will successfully pass the course and land high-paying tech jobs in the industry.

## Scope (In/Out)

**IN - What will your product do**

- Primary - To maintain a database encompassing all terms relevant to the course, and then present those terms in an aesthetically pleasing way to the user.

- Secondary - To allow students to log into an account so they can view, update, and delete terms to the glossary to form a more complete database.

- Tertiary - To allow the user to see spelling errors before submitting a new or updated term, to ensure all terms remain correctly spelled and gramatically correct.

**OUT - What will your product not do.**

- There will be no search functionality
- There will not be the ability for admin approvals

## What are your stretch goals?

- Flash-card mode
- Multi-lingual support

## Functional Requirements

- A user can log in for access to terms
- A user can view all terms currently in the glossary, and see a term-specific page for each
- User can add, delete, or update terms they have access to
- User can check spelling before submission of a new or updated term

## Data Flow

Upon login, an initial request to the database would load all terms currently in the glossary and save them in state. From a home page that lists all glossary terms, the user could then click on one term, which would pull up a modal with additional info (definition, details, example, etc.) which would be pulled directly from state.
Upon clicking the delete or update buttons within the modal, a new request would be sent to the database to PUT or DELETE, the item's info would be updated in state and re-rendered.
Upon clicking the add button on the home page, a new request would be sent to the database to POST a new term, and the info would be added to state and re-rendered.

## Non-Functional Requirements (301 & 401 only)

- The bootstrap modal would provide a user-friendly way of presenting the terms and allowing ease of update/deletion of a term
- Auth0 will help provide data integrity and security by only allowing logged in users access to the data
- Storing secure variables in environmental variables and not directly in the code will help maintain security as well
