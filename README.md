# plane-alert-db


This project consists of lists of 'interesting' aircraft, formatted as CSV files. **The list is designed to work with the excellent https://github.com/kx1t/docker-planefence** and takes the form 

- $ICAO,$Registration,$Operator,$Type,$ICAO Type,#CMPG,$Tag 1,$#Tag 2,$#Tag 3,Category,$#Link

e.g 502C5C,YL-KSH,Baltic Bees display team,Aero L-39 C,L39,Civ,Do A Barrel Roll,Display Team,,Aerobatic Teams,https://en.wikipedia.org/wiki/Baltic_Bees_Jet_Team

Add these characters to the column headers to control the behavior of PlaneAlert

- "$" \- Tweet this column as #hashtag
- "#" \- Don't show on the website (it will ignore this for the ICAO field, which is always shown)
- "$#"\- Don't show on the website, tweet as a #hashtag

in the example above the #hashtags would be 'Air Ambo','Choppa' and 'EXPL'. Tag2, Tag3 and Link will not be shown on the PA website. Please be aware if your tweets are too long they will be truncated by PF/PA. To prevent this you should exclude CMPG and Category from your tweets - this will ensure all tweets fits inside the char limit.

- CMPG = Civilian, Military, Police, Government
- Tag 1 = Funny/amusing
- Tag 2 = Useful/relevant
- Tag 3 = Anything goes
- Link - Either an informative or funny link. All are SFW, except maybe the Disney plane.

# Planefence
To use this list with Planefence, simply configure your planefence.config setup to include the following line:

- PF_ALERTLIST=https://raw.githubusercontent.com/Sportsbadger/plane-alert-db/main/plane-alert-db.csv

If you want to add the list in addition to your local plane-alert-db.txt list, you can do the following:

- PF_ALERTLIST=plane-alert-db.txt,https://raw.githubusercontent.com/Sportsbadger/plane-alert-db/main/plane-alert-gov.csv,https://raw.githubusercontent.com/Sportsbadger/plane-alert-db/main/plane-alert-pol.csv

**Note -- the priority of use is first-to-last, so if you want your local list to be interpreted first, move it to the front of the list**

# Current Content

The list contains **7554** unique aircraft in **46** different categories.

- [plane-alert-db.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/plane-alert-db.csv) - The list of interesting aircraft, with tags,categories and links. (7554)
- [plane-alert-civ.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/plane-alert-civ.csv) - Civilian Registered Aircraft, includes Historic and Distinctive. (1243)
- [plane-alert-mil.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/plane-alert-mil.csv) - Military Only. (4411)
- [plane-alert-pol.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/plane-alert-pol.csv) - Police Forces. (860)
- [plane-alert-gov.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/plane-alert-gov.csv) - Governments, Gov Agencies and Dictators. (1040)
- [badgers-best.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/badgers-best.csv) - My own personal selections from the main list. (2560)
- [community-list.csv](https://github.com/Sportsbadger/plane-alert-db/blob/main/community-list.csv) - Open list to add your suggestions to. These will be moved to the main list in time.

This [Dashboard](https://datastudio.google.com/reporting/eb19ab53-b622-4946-b34a-9667232c136d/page/4taCC) contains details of the main list and the most recent additions.

# Description of Categories

Think of categories like groups, with similar or related aircraft listed together. This allows you to easily select a subset of the list for your own use. The category names (and tags) come from my rather idiosyncratic sense of humour. If you have better suggestions I'm all ears.

- Aerobatic Teams \- Red Arrows, Blue Angels etc. (58)
- Army Air Corp \- UK Army Air Corp. Mainly Helicopters. (91)
- As Seen on TV \- Companies and Brands (119)
- Battle of Britiain Memorial Flight \- Historic British aircraft from WW2 (13)
- Big Hello \- Large Helicopters (sic) (38)
- Bizjets \- Fancy pants planes for fancy pants people (68)
- Coastguard \- Coastguard, Customs and Border Patrols (44)
- Da Comrade \- Russian or Soviet Aircraft. I love their design, so they get their own category (91)
- Dictator Alert \- People of potentially questionable morals and values (292)
- Distinctive \- Unique and/or special aircraft e.g The AN-225 Myria, NASA aircraft (230)
- Dogs with Jobs \- Aircraft with specific roles and/or modifications (81)
- Football  \- Actual, Aussie Rules or American. We don't discriminate. (2)
- GAF \- Aircraft of the German Air Force, thank to Rhodan76 (288)
- Gas Bags \- Would you like to ride in my beautiful balloon ? (4)
- Governments \- Aircraft registered to Governments (208)
- Gunship \- Brrrrrrrrrrrrrrrrrrrt (256)
- Hired Gun \- Why do the dirty work when someone else can do it for you ? (58)
- Historic \- It's older than I am, and most likely has a prop. (139)
- I For One Welcome our new Overlords \- Clippy et al. (23)
- Jesus he Knows me \- Aircraft owned and operated by Religious organisations (11)
- Just Because \- I don't know why I like you, but I do. (7)
- M\*A\*S\*H \- Air Ambulance and Medical Flights
- Nuclear \- Nuclear Emergency Support Team etc (12)
- Other Air Forces \- Air Force aircraft that are not RAF or USAF (530)
- Other Navies \- Navy Aircraft that are not Royal Navy Fleet Air Arm or United States Navy (67)
- Police Forces \- Your friendly neighbourhood flying (insert local colloquialism here) (840)
- Ptolemy would be proud \- Mapping and Aerial Survey aircraft.  (35)
- Quango \- Nato, United Nations, World Bank etc (42)
- Radiohead \- Very Very special aircraft. Think VC25. (5)
- RAF \- Aircraft of the Royal Air Force (237)
- Royal Aircraft \- Aircraft used or owned by the UK Royal Family (8)
- Royal Navy Fleet Air Arm \- Aircraft of the Royal Navy Fleet Air Arm (105)
- Sam Tân \- Firefighting Aircraft. (285)
- Sock Puppet \- Someone Pretending to be something they are not e.g. Covert DOJ Aircraft (105)
- Special Forces \- The best of the best of the best. Sir. (151)
- Toy Soldiers \- Armies from around the world (99)
- UAV \- It's not natural, I tell 'ya (12)
- UK National Police Air Service \- Your friendly neighbourhood flying bobby (24)
- Under Observation \- Up to something dodgy, maybe (65)
- United States Navy \- United States naval avaitors. Some say they are the best of the best. (56)
- USAF \- Aircraft of the United States Air Force (2286)
- Vanity Plate \- Distinctive registrations (51)
- Watch Me Fly \- Flying and Training Schools (74)
- Who needs an Engine ? \- Gliders etc (63)
- You came here in that thing ? \- Microlights, tiny planes and helis..think Yakima Super Breezy (thanks skstrand) (41)
- Zoomies \- Fast jets, fighters. Anything that moves fast (127)

# To do / Ideas

No 1 - Update USAF aircraft to use Reg/serial number in place of Ident/Callsign

- RAF Typhoon Display Team
- Breitling Jet Team (not complete)
- US Dept of Interior
- US Dept of Energy
- Other US Gov Depts
- B737 with Gravel Kits - Nolinor, Air Inuit, Canada North, Chron Aviation
- Defense Helicopter Flying School
- Identify more Aircraft owned by Religious organisations
- Acrobat Ltd (Uk Gov Sock puppet ?)
- UK Ministry of Defence
- UK Border Force
- Shuttleworth Collection
- Other Warbirds
- List of DA42 MPP / DA62 MPP Operators
- Thales UK
- Survey / Mapping Aircarft
- Other surveillance aircraft types
- 750 Naval Air Squadron (Observers)
- Coulson Aviation
- Australian Aircraft called firebird (fire spotter and fighters)
- S-64 Skycrane - list only partially completed (what is the list of names)
- Japanese Flying Boats Shin Maywa US-2/US 1 (US2 are 9901 through 9907 - mode s ?)
- Private Adversary Squadrons (Air Usa etc)
- Operators of old Jets/Fighters (e.g. Hawker Huner Aviation)
- Callspan Corp In-Flight Simulators
- GAMA Avaiation (ex RAF spy planes)
- Flying Hospitals (eye Hospital ?)
- Other Coast Guards (e.g. USCG)
- Air Ambulances (Wikipedia List)
- Big Russian Helis
- Babcock MCS Spain (and any other countries)
- Lewis Hamilton Jet(s)
- Open Skies Flights
- Eurpoean Union
- Scienctific / Weather planes
- Flight Precision Ltd (and Similar)
- World Bank etc
- Red Cross / MSF
- Special Convertions e.g. Engine testbeds
- Duxford and other historic flight collections
- Historic Aircraft Flight Trust
- Low volume Airliners / Special Models
- Football Teams and other sporting organisations
- Beechcraft RC-12 Guardrail
- Meteorological research flights
- Film and Televison Companies
- News Choppers
- RCAF Snowbirds
- RAAF Roulettes
- Helicopter Transport Services
- Arena Aviation
- Slagboom & Peeters nv (Aerial Surveys)
- Air Affairs Australia
- ADAC Germany
- Denmar Technical Services (Stealth radar testing)
- IAS Medical (Air Evac)
- Aviation Services Australia
- Historic Army Aircraft Flight
- Odd C130 Hercules - EC130H, EC130E, EC130J, MC130H, WC130J
- AeroRescue
- Air-Glaciers
- Alci Avaiation
- Baltic Bees Display Team
- Bundesamt für Landestopografie
- Bundesamt für Zivilluftfahrt BAZL
- Bundespolizei
- GFD.de
- Royal Flying Doctors Service
- Top Aces Inc.
- Russian FSB
- Aircraft and companies in this article - https://www.cjr.org/watchdog/how-buzzfeed-news-revealed-hidden-spy-planes-in-us-airspace.php
- Chapparral Air Group
- Acorn Growth Companies
- Aircraft owned/Operated by Sultan/State of Brunei (esp his very plush 747)
- Aircraft - Lake Renegade
- Special Hurons - MC-12W, MC-12S, RC-12H, RC-12N
- Edgley Optika
- Columbian C47 Gunships - Got 1 are there more ?
- Artic and Antartic Aircraft (Got some - but are there more ?)
- Thunder City (SA Company flying old jets)
- Meta Special Aerospace
- FAA and CAA
- US Missile Defence Agency
- A4 Skyhawks
- Italian Guardia di Finanza
- <strike>Network Rail Helicopter(s)</strike>
- <strike>Multinational MRTT Fleet</strike>
- <strike>Fly Navy Heritage Trust</strike>
- <strike>Check Saudi Armed Forces Medical Services is complete</strike>
- <strike>Aircraft operated by Comlux</strike>
- <strike>Icelandic Coastguard</strike>
- <strike>The Flying Bulls</strike>
- <strike>Check Empire Test Pilots School is complete</strike>
- <strike>Qinetiq</strike>
- <strike>Air Koryo</strike>
- <strike>Lynden Air Cargo</strike>
- <strike>UK Coast Guard</strike>
- <strike>Basler BT-67 Operators</strike>
- <strike>Kamov KA32's</strike>
- <strike>United Nations</strike>
- <strike>A10 Thunderbolt II</strike>
- <strike>China National Antarctic & Arctic Research Expedition</strike>
- <strike>Police Scotland Air Support Unit (NI Equivalent)</strike>
- <strike>French Armed Forces</strike>
- <strike>Firefighting Aircraft / Companies</strike>
- <strike>Cal Fire</strike>
- <strike>Gunships (Spooky, Central American DC3's)</strike>

Any other idea's welcome.

# Disclaimer, excuses and dodges

This is not intented to be a definitive list, especially when it comes to aircraft models. Where the same model of aircraft is made by several manufacturers I wont always have the correct one. If you thought it was a Beechcraft King Air 200 and actualy it was a Textron Super King Air B200GT I won't be losing any sleep. There are other data sources (see below) if you want absolute accuracy. 

# Data Sources

This data has been gathered from far too many sources to mention, but some sites have been *really* useful.

https://whatisflying.com/en/database/aircraft-types

https://github.com/jbroutier/whatisflying-db

https://www.flightdb.net/index.php

http://www.rotorspot.nl/

http://www.dtvmovements.co.uk/

http://www.ads-b.nl/

https://www.live-military-mode-s.eu/

https://dictatoralert.org/ 

http://www.j-hangarspace.jp/

https://scramble.nl/

https://www.foxtrotcharlie.ovh/

https://www.planelogger.com/
