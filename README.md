# Oregon Sound Circuit

Two things live on this domain.

**Policy tracker (`/`, members only).** Legislation and rulemaking on AI in the music industry (digital replicas, voice and likeness, provenance, training data) and secondary ticketing, for Music Oregon's AI Policy Committee. Login required; not indexable. The data comes from LegiScan under its non-commercial public API terms and is not published publicly. Data sources and attribution: LegiScan (CC BY 4.0), Oregon Legislature OLIS, Federal Register, Congress.gov. Relevance is keyword rules plus committee review, no AI scoring.

**Venue directory (`/venues`, public).** A census of live music venues in Oregon and the Portland area: what is open, what has closed and when, capacity, ages, ownership, how to book. Anyone can read it and download it as CSV; editors sign in to add venues, correct listings and record closures. Seed listings include data from OpenStreetMap contributors (ODbL). Unverified listings are marked as such until an editor confirms them.

Static site on Vercel, one page per product, using supabase-js with Supabase Auth email and password login. Row level security on the database does the real protection: the tracker's tables return nothing without a login, and the directory's editor-only columns are hidden from the public by column grants. The pages contain only the Supabase publishable key, which is safe to publish. No other secrets exist in this repository.

`robots.txt` and the `X-Robots-Tag` header block indexing of everything except `/venues`.

The collectors and import scripts that fill the database live outside this repository.
