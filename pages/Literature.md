icon:: 📚
state:: [[🌲]]
input:: [[Library]]
name:: Literature

	- # Literature
	  id:: 6787b897-3802-4cfe-b4b9-12cc24321558
		- ## [[Articles]]
			- {{query (and (property :input [[Articles]] ) (not (page [[Templates]])))}}
			  query-table:: true
			  query-properties:: [:state :page :authors]
		- ## [[Books]]
			- {{query (and (property :input [[Books]] ) (not (page [[Templates]])) (not (property :input [[Technical Books]] )))}}
			  query-sort-by:: title
			  query-table:: true
			  query-sort-desc:: true
			  query-properties:: [:state :page :authors]
		- ## [[Quotes]]
			- {{query (and (property :input [[Quotes]] ) (not (page [[Templates]])))}}
			  query-table:: true
			  query-properties:: [:state :page :name]
