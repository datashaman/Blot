# Routing

URL routes to blog

sidenote -> expose req.query as {{query}} in templates?
  could be useful… how could we pass this into templates?{{recentEntries:query.from query.to}}? mental…

Entry URLs should have:
- leading slashes
- no trailing slashes

3. check if ‘/assets/*’
  -> assets route

3. check if ‘/plugins/*’
  -> plugins route

4. check if ‘/draft/*’
  -> draft route

3. check if ‘/tagged/*’
  -> tag route

2. check if ‘/search’
  -> search route

2. check if ‘/robots.txt’
  -> robots route for preview URLs

3. check if ‘/verify/domain-setup’
  -> verify route

1. check if ‘/‘
  -> entries route

2. fall through to ‘/*’

  if view matches route exactly
    -> render view

  if entry url matches route exactly
    -> render entry

  extract entry ID from URL (first term before slash)
  and if entryID matches entry:
    -> render entry

  404 page




