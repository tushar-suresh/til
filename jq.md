## Filter based on empty array
jq 'select(.fieldFoo | length > 0)'


## Aggregate stats on size of an array
jq '.fieldFoo | length' | sort | uniq | sort -nr
