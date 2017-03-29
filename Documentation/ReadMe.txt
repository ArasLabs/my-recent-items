Notice of Liability
-------------------
The information contained in this document and the import packages are distributed on an "As Is" basis, 
without warranty of any kind, express or implied, including, but not limited to, the implied warranties 
of merchantability and fitness for a particular purpose or a warranty of non-infringement. Aras shall have 
no liability to any person or entity with respect to any loss or damage caused or alleged to be caused 
directly or indirectly by the information contained in this document or by the software or hardware products 
described herein.


Version:
--------
v3-1  (October 2014)
 - added logic to clean up stale entries (items that got deleted elswhere)

v3-0  (October 2014)
 - works with A11 and A10
 - removed properties and server method from ItemType and User
 - Configuration of item types to enable are now under "Preferences"
 - Multi-Language of grid headings can be set in Preferences
 - Configurable context menu actions by grid row type.


Description (Package Utilities)
------------
This Add-On Package adds a stack to track the N recently visited items per user login.
Item Types to be tracked  can be configured to be any ItemType (by Preferences).  
It loads on top of the standard ARAS Solutions PE,PM,QP without any conflicts.
On the TOC, under „My Innovator“, a new line „My Recently Visited“ will show
Every user can „clear“ their own list from the grid 
Administrators can see the lists added to users (as relationship). And delete from there, if necessary.
Administrators can set the max count of items to list per user, menu actions by item type, and other options on user‘s preferences. (default preferences are connected to „World“)

Optional import step will add tracking for: Document, Part CAD,Project,Manufacturer Part,Manufacturer,Express ECO, PR, Express DCO)


Installation Steps
------------------
use package import utility to import packages in this sequence. (logon as "admin" and use option "merge" for all steps)

	0-Delete - core Extensions (of prev Version)  <-- only if you already have a previous version of this package

	1-Common Grid Utilities v3-0 (partial)

	2-Import - AddOn-Solution

	3-Configuration Data

	SetPackageVersion (optional)  - will fail, if "Package Utitlties" are not in your Aras system



Dependencies
------------
- com.aras.innovator.solution.PLM must be present
- CommonBase GridUtilities


available as Community Project
------------------------------
Yes


Version History:
----------------
r1-1  (Fwb 2013)
	Initial release

r1-3  (Oct 2012)
      Improved performance.

v2-2A10  (May 2014)
 - works on Aras 10 only !!!
 - changed all programmed grids to dojo grids


