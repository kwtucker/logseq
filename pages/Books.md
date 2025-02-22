icon:: 📖
state:: [[🌲]]
name:: Books
input:: [[Literature]]
tags::

	- # [[Books]]
		- {{query (and (property :input [[Books]] ) (not (page [[Templates]])) (not (property :input [[Technical Books]] )))}}
		  query-sort-by:: title
		  query-table:: true
		  query-sort-desc:: true
		  query-properties:: [:state :page :authors]
