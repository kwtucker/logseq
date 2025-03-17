icon:: 📋️
alias:: T
state:: [[🌲]]
name:: Tasks
input:: [[Dashboard]]
tags::

	- # [[Tasks]]
		- {{query (and #t (or(task LATER ) (task TODO ))   )}}
		  query-table:: true
		  query-properties:: [:page :block]