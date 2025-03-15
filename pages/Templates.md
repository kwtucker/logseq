icon:: 🏗️
exclude-from-graph-view:: true
input:: [[Dashboard]]

- # Templates
	- See [[Properties]] for more information.
	- ## Page Template
	  template:: Page
	  template-including-parent:: false
		- icon::
		  state:: [[🌱]]
		  name::
		  input::
		  tags::
			- # <% current page %>
				-
	- ## Block Template
	  template:: Block
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input::
		  tags::
	- ## Project Template
	  template:: Project
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input:: [[Projects]]
      status:: [[LATER]]
		  tags::
			- # <% current page %>
        - ## Summary
          - 
        - ## Tasks
          - LATER <% current page %>
            - 
	- ## Person Template
	  template:: Person
	  template-including-parent:: false
		- state:: [[🌱]]
		  input:: [[People]]
		  tags::
		  name::
		  phone::
		  email::
		  birthday::
		  company::
		  job-title::
	- ## Book Template
	  template:: Book
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input:: [[Books]]
		  tags::
		  genre::
		  authors::
		  date-finished::
		  recommended-by::
		  rating::
			- # [Book Title Here]
				- ### **1. Key Points/Plot Summary:**
					- (Summarize key events or ideas in each chapter or section. Keep it brief.)
				- ### **2. Characters/Important People:**
					- (List the main characters, their traits, motivations, and how they evolve. Also, include any important supporting characters.)
				- ### **3. Themes/Ideas:**
					- (What are the major themes or concepts explored in the book? What is the author trying to communicate?)
				- ### **4. Favorite Quotes/Passages:**
					- (Write down any memorable lines or paragraphs and why they stood out to you.)
				- ### **5. Questions/Confusions:**
					- (Write any questions that arise as you read, things you don’t quite understand, or points that need further clarification.)
				- ### **6. Connections/Reflections:**
					- (How does the book relate to your life, other books you’ve read, or current events? Do you find personal meaning or lessons from it?)
	- ## Article Template
	  template:: Article
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input:: [[Articles]]
		  tags::
		  genre::
		  authors::
		  date-finished::
		  recommended-by::
		  source::
		  rating::
	- ## Meeting Template
	  template:: Meeting
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input:: [[Meetings]]
		  tags::
		  company::
		  project::
			- ### Participants
				-
			- ### Agenda
				-
			- ### Notes
				-
			- ### Action Items
				-
	- ## Place Template
	  template:: Place
	  template-including-parent:: false
		- state:: [[🌱]]
		  name::
		  input:: [[Places]]
		  tags::
		  phone::
		  email::
		  website::
		  address::
		  rating::
