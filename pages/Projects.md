icon:: 🧰
input:: [[Dashboard]]

	- # [[Projects]]
		- ## Active Projects
			- {{query (and (property :input [[Projects]]) (not (page [[Templates]])) (or (property :status "NOW") (property :status "DOING")))}}
			  query-sort-by:: status
			  query-table:: true
			  query-sort-desc:: false
			  query-properties:: [:state :name]
		- ## Planned Projects
			- {{query (and (property :input [[Projects]]) (not (page [[Templates]])) (or (property :status "LATER")  (property :status "TODO"))))}}
			  query-table:: true
			  query-properties:: [:state :name]
	-
