
Version:
--------
v2-2A10  (May 2014)
 - works on Aras 10 only !!!
 - changed all programmed grids to dojo grids


Description (Package Utilities)
------------
This Add-On Package adds a stack to track the N recently visited items per user login.
Item Types to be tracked  can be configured to be any ItemType.
 (sample config is provided for: Document, Part, CAD,Project,Manufacturer Part,Manufacturer,Express ECO, PR, Express DCO)

It loads on top of the standard ARAS Solutions PE,PM,QP without any conflicts.
On the TOC, under „My Innovator“, a new line „My Recently Visited“ will show
Every user can „clear“ their own list from the grid (right mouse click action)
Administrators can see the lists added to users (as relationship). And delete from there, if necessary.
Administrators can set the max count of items to list per user. (if not set, it defaults to 15)

Know Issues:
------------
- adds a property is_recently_visited ItemType "all" definitions. When exporting packges form a system with
  this solution loaded the XML of all item types will list this property. If importing this package to another system
  that does not have this solution loaded the import tool will throw an error complyining about this property.
  --> you must remove this property definition from the XML or import Recently Visited to the other Aras system


Installation Steps
------------------
use package import utility to import packages in this sequence

	0_Common Grid Utitltites (logon as "admin" and use option "merge")

	1- Import - core Extensions  (logon as "root" and use option "merge")

	2- Import - AddOn-Solution   (logon as "admin" and use option "merge")

	3- Import - Tracking on Part,Document,CAD etc  (logon as "admin" and use option "merge")

	SetPackageVersion (optional)  - will fail, if "Package Utitlties" are not in your Aras system



Dependencies
------------
- com.aras.innovator.solution.PLM must be present


available as Community Project
------------------------------
Yes


Version History:
----------------
r1-1  (Fwb 2013)
	Initial release

r1-3  (Oct 2012)
      Improved performance.


Notice of Liability
-------------------
The information contained in this document and the import packages are distributed on an "As Is" basis, 
without warranty of any kind, express or implied, including, but not limited to, the implied warranties 
of merchantability and fitness for a particular purpose or a warranty of non-infringement. Aras shall have 
no liability to any person or entity with respect to any loss or damage caused or alleged to be caused 
directly or indirectly by the information contained in this document or by the software or hardware products 
described herein.

