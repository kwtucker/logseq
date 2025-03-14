icon:: 🧰
input:: [[Dashboard]]

	- # [[Projects]]
		- ## Active Projects
			- {{query (and (property :input [[Projects]]) (or (property :status "NOW") (property :status "DOING")))}}
			  query-table:: true
			  query-properties:: [:state :name]
			  query-sort-by:: status
			  query-sort-desc:: false
		- ## Planned Projects
			- {{query (and (property :input [[Projects]]) (or (property :status "LATER")  (property :status "TODO"))))}}
			  query-table:: true
			  query-properties:: [:state :name]
	-
