# Oregon Sound Circuit

Members-only policy tracker for Music Oregon's AI Policy Committee: legislation and rulemaking on AI in the music industry (digital replicas, voice and likeness, provenance, training data) and secondary ticketing.

Static site on Vercel. One page, `index.html`, using supabase-js with Supabase Auth email and password login. Row level security on the database does the real protection: without a login the API returns nothing. The page contains only the Supabase publishable key, which is safe to publish. No other secrets exist in this repository.

The site is intentionally not indexable (`robots.txt`, `X-Robots-Tag`, meta robots). The data comes from LegiScan under its non-commercial public API terms and is not published publicly.

Data sources and attribution: LegiScan (CC BY 4.0), Oregon Legislature OLIS, Federal Register, Congress.gov. Relevance is keyword rules plus committee review, no AI scoring.

The collectors that fill the database live outside this repository.
