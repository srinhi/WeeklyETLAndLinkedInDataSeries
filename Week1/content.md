Week 1: NYC HPD Housing Complaints (July 2026)

Source: NYC Open Data — 311 Service Requests, filtered to HPD (Department of Housing Preservation and Development) complaints, pulled via the Socrata API. [only accessed July records]

Questions:

1. What's the distribution of HPD complaints across NYC boroughs, and does one borough clearly dominate?
2. Where are HPD complaints geographically concentrated, and what might that clustering reflect (e.g. housing age, density, building type)?
3. What are the most common HPD complaint types, and what does that ranking suggest about the state of NYC's housing stock?

Stack: Python, pandas, matplotlib

What I did

Pulled a filtered slice of HPD complaint records directly from the Socrata API ($where=agency='HPD') rather than downloading the full multi-million-row dataset
Cleaned coordinate fields (pd.to_numeric with errors='coerce'), dropped nulls, and filtered out-of-bounds/placeholder coordinates outside NYC's real lat/long range
Analyzed complaint volume by borough, by complaint type, and by geographic location

Findings

Brooklyn (28.1%) and the Bronx (27.3%) together account for over half of all HPD complaints, more than Manhattan, Queens, and Staten Island combined
Complaints cluster geographically in specific corridors, upper Manhattan into the west Bronx, and central Brooklyn, rather than spreading evenly across each borough
Pests is the single most common complaint type (~640 records), well ahead of water leaks (~350) and mold (~325); the top complaint types overall point to aging building infrastructure rather than isolated incidents
