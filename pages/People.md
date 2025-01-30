alias:: People
inut:: [[Dashboard]]

- # People
- {{query (and (property :input [[People]]) (not (page [[Templates]])))}}
  query-sort-by:: state
  query-sort-desc:: true
  query-table:: true
  query-properties:: [:state :page]
