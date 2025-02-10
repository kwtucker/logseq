icon:: 📚
input:: [[Dashboard]]

	- # Literature
	  id:: 6787b897-3802-4cfe-b4b9-12cc24321558
		- ## [[Books]]
			- {{query (and (property :input [[Books]] ) (not (page [[Templates]])) (not (property :input [[Technical Books]] )))}}
			  query-sort-by:: title
			  query-table:: true
			  query-sort-desc:: true
			  query-properties:: [:state :page :authors]
		- ## [[Articles]]
			- {{query (and (property :input [[Articles]] ) (not (page [[Templates]])))}}
			  query-table:: true
			  query-properties:: [:state :page :authors]
