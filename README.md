# permit-index
## Problem to be solved:
To get a copy of a DCRA building permit from 1949 to 1995, a researcher has to go to DCRA with the property address, and DCRA then will fax a request sheet to the DC Archives indicating which boxes hold permits for that addresses. The DC Archives then pulls the boxes, finds the relevant folders, and makes an appointment with the researcher. This is time-consuming, confusing, and frustrating for the researcher. The DC Archives has the indexes for the boxes of permits, but does not have the staff time for the one step of identifying which boxes are associated with which addresses. 
## Solution:
Create a portal where a researcher can enter an address in DC, and output a list of boxes.
## Underlying data:
There are index documents that I will try to figure out how to post in the repo. They are currently PDF documents but I am also working on converting them to .csv.
## Coding needs:
1. Input method 
2. Compare address to each index file; index files contain the first and last address in each box, organized alphabetically. The code will need to find the box where the first address comes before (<=) and the last address comes after (>=) the address entered.
3. Output method

## Cherry on top:
It would be great for our researchers if this also included a "click to submit your request" function. This would require the user's name, email, phone number, and the address and box numbers being requested.
## Data problems to be aware of:
1. In some cases, the last address in one box may come after the first address in the next box. (See, e.g., file for accession 351-85-0050. Box 3 ends with 1128 1st Street while box 4 begins with 1127 1st Street.) (Desired result: both boxes are listed in output.)
2. In some cases, permits for a single address may be continued in a second box. (Desired result: both boxes are listed in output.)
3. Addresses may fall between the last address in one box and the first address in the next. (Desired result: no box is listed in output.)
4. "Half Street" is categorized as a numbered street (1st, 2nd, etc.) but written as a named street (that is, not "1/2 Street").
