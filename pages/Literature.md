alias:: Literature
input:: [[Dashboard]]

- # Literature
  - ## [[Books]]
    - {{query (and (property :links [[Books]] ) (not (page [[Templates]])))}}
      query-sort-by:: page
      query-table:: true
      query-sort-desc:: true
      query-properties:: [:state :page :authors]
  - ## [[Technical Books]]
    - {{query (and (property :links [[Technical Books]] ) (not (page [[Templates]])))}}
      query-sort-by:: page
      query-table:: true
      query-sort-desc:: true
      query-properties:: [:state :page :authors]
  - ## [[Articles]]
    - {{query (and (property :links [[Articles]] ) (not (page [[Templates]])))}}
      query-sort-by:: page
      query-table:: true
      query-sort-desc:: true
      query-properties:: [:state :page :authors]
