icon:: 📝
input:: [[Dashboard]]

	- # [[Meetings]]
		- {{query (and (property :input [[Meetings]] ) (not (page [[Templates]])))}}
		  query-table:: true
		  query-properties:: [:state :page :host :name]
