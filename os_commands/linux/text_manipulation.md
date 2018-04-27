# Sorting and unique operations

## "sort -u" - unique lines only
`cat access.log | cut -­‐d  " " -f 1 | sort -u`

## number of duplicates using "uniq -c"
`cat access.log | cut -­‐d  " " -f 1 | sort | uniq -c | sort -urn`
