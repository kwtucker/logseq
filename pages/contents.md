# Contents
	- {{query (property :input "Dashboard")}}
	  query-table:: true
	  query-sort-by:: page
	  query-sort-desc:: false
	  query-properties:: [:icon :page]
- ## Todo
	- query-table:: true
	  query-properties:: [:page :block]
	  #+BEGIN_QUERY
	  {:title [:b "🔨 NOW"]
	  :query [:find (pull ?h [*])
	       :in $ ?start ?today
	       :where
	       [?h :block/marker ?marker]
	       [(contains? #{"NOW" "DOING"} ?marker)]
	       [?h :block/page ?p]
	       [?p :block/journal? true]
	       [?p :block/journal-day ?d]
	       [(>= ?d ?start)]
	       [(<= ?d ?today)]]
	  :inputs [:14d :today]
	  :result-transform (fn [result]
	                   (sort-by (fn [h]
	                              (get h :block/priority "Z")) result))
	  :group-by-page? false
	  :collapsed? false}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:page :block]
	  collapsed:: true
	  #+BEGIN_QUERY
	  {:title [:b "🕗 OVERDUE"]
	  :query [:find (pull ?b [*])
	        :in $ ?start ?end
	        :where
	        (or 
	          [?b :block/scheduled ?d] 
	          [?b :block/deadline ?d]
	        )
	        (not
	          [?b :block/marker ?marker] 
	          [(contains? #{"DONE" "CANCELLED"} ?marker)]
	        )
	        [(>= ?d ?start)]
	        [(<= ?d ?end)]
	  ]
	  :inputs [:1500d-before :today]
	  :collapsed? true}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:page :block]
	  collapsed:: true
	  #+BEGIN_QUERY
	  {:title [:b "📅 NEXT"]
	  :query [:find (pull ?b [*])
	        :in $ ?start ?end
	        :where
	        (or 
	          [?b :block/scheduled ?d] 
	          [?b :block/deadline ?d]
	        )
	        (not
	          [?b :block/marker ?marker] 
	          [(contains? #{"DONE"} ?marker)]
	        )
	        [(>= ?d ?start)]
	        [(<= ?d ?end)]
	  ]
	  :inputs [:today :7d-after]
	  :collapsed? true}
	  #+END_QUERY
	- query-table:: true
	  query-properties:: [:page :block]
	  collapsed:: true
	  #+BEGIN_QUERY
	  {:title [:b "🔭 HORIZON"]
	  :query [:find (pull ?b [*])
	        :in $ ?start ?end
	        :where
	        (or 
	          [?b :block/scheduled ?d] 
	          [?b :block/deadline ?d]
	        )
	        (not
	          [?b :block/marker ?marker] 
	          [(contains? #{"DONE"} ?marker)]
	        )
	        [(>= ?d ?start)]
	        [(<= ?d ?end)]
	  ]
	  :inputs [:today/+7d  :today/+90d]
	  :collapsed? true}
	  #+END_QUERY
