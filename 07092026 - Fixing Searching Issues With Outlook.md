Maureen from Robinson Hill Architecture had filed a ticket saying that one of her employees couldn't get any results when searching for a client's name on their Outlook application.

When accessing their device through Remote Desktop, I noticed that there seemed to no issue with searching on my end. However, because Maureen had noted that her employee had been dealing with this problem over the course of a few months, I thought it'd be best to try to apply a solution for the search issue (assuming that the employee is searching properly).

The solution I had ended up using for this ticket was to rebuild the Instant Search catalog through Indexing Options.

To rebuild a search catalog on a Windows device:
- Control Panel → Indexing Options → Advanced
- ![[Pasted image 20260710083722.png|378]]
- Rebuild
- ![[Pasted image 20260710083808.png]]

As a safeguard for this solution, I also adjusted the user's sync settings for their Outlook from 1 year to All. [By default, Outlook may only download the last 12 months of mail for Exchange or Microsoft 365 accounts, and anything older remains on the server, making it invisible to local search.](https://learn.microsoft.com/en-us/answers/questions/5708103/why-can-i-not-see-all-the-emails-when-i-am-searchi) 

This can be done by:
- Going to File → Account Settings → Account Settings → Change
- Then adjust the slider under Download email for the past to **All**

---

References:
- https://learn.microsoft.com/en-us/answers/questions/5708103/why-can-i-not-see-all-the-emails-when-i-am-searchi
- https://support.microsoft.com/en-us/outlook/fix-search-issues-by-rebuilding-your-instant-search-catalog
