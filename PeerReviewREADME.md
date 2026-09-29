Brandon Langehennig
Bug Hunt DockingBayAPI
Peer Reviewer Name: Valery Lot
Review: Still a few bugs left as the end result didn't match what was expected.

Ships:
The 03 GET /api/ships/999 is giving 500 Internal Server Error instead of 404. 
The 09 DELETE /api/ships/3 is also giving 500 Internal Server Error rather than 204. 
The 10 GET /api/ships/3 also gives 500 error.

Pilots:
The 20 GET /api/pilots/3 doesn't result in 100 flight hours.
The 21 PUT /api/pilots/3/log-hours/0 doesn't result in a 400 status code.
The 24 POST /api/pilots doesn't result in 0 flight hours.
The 25 POST /api/pilots doesn't increase the ID to 5.
The 26 GET /api/pilots/total-hours doesn't result in 1640 hours.