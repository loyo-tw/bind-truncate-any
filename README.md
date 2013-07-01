bind-truncate-any
=================

Patch for ISC Bind(named) used for truncate TYPE ANY request.
This patch will make client's DNS query which TYPE=255/ANY with reply with truncate flag(TC flag) set, makeing client using TCP to query again.

Install
-------
- Patch File
`/bin/gpatch -p0 -i bind984p2-truncate-any.patch`

Usage
-----
In named.conf
###	
	option {
		...
		truncate-any-request  yes|no;
		...
	}
* truncate-any-request yes: Enable truncate TYPE ANY request.
* truncate-any-request no: Disable truncate TYPE ANY request. 

Author
------
Loyo Fulamce 


