icon:: 📝
state:: [[🌱]]
input:: [[Dashboard]]
tags::

    - # [[Meetings]]
    	- {{query (and (property :input [[Meetings]] ) (not (page [[Templates]])))}}
    	  query-table:: true
    	  query-properties:: [:state :page :name :tags :project]
