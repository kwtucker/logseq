icon:: 📋️
alias:: T
name:: Tasks
input:: [[Dashboard]]

	- # [[Tasks]]
		- All tasks marked with #t, are tasks I made actionable. This means I can do them in 5-10 minutes and the line is a clear thing I can do.
		- {{query (and #t (or(task LATER ) (task TODO ))   )}}
		  query-table:: true
		  query-properties:: [:page :block]
