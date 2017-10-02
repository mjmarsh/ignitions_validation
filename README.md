# ignitions_validation
Documentation for validating vegetation fire ignitions for Fire Danger Operating Plan

**Weekly Ongoing Process:** 
(this should be done weekly, as it makes the validation process much more accurate and manageable due to incomplete LE-66 data)

   **1.** Using [Incident Viewer](http://incidents.slocountyfire.org/) 'Filter' incident categories by 'Fire'
  
   **2.** Record all incidents with dispatches that potentially could have caused a vegetation fire in SLO County at the [google drive link](https://docs.google.com/spreadsheets/d/1Q5jG-l3zrVk_KewulYnyV7hiYdzqAW0jLGpAjOuZw0g/edit?usp=sharing)  
    ** Login with slugis3400@gmail credentials **
  
   **3.** Complete 'Incident ID' and 'Dispatch type'(you will find more information using the FC-34 and LE-66 reports later on in step 4) 
   
        - Generally, anything like 'Fire, Wildland xxx'
        - Other possibilities include; 'Fire, Veh Commercial', 'Fire, Smoke Check'. 'Fire, Debris', 'Fire, Residential'
        ** Note: these dispatch types are the initial type and may have later been changed **
  
 *Now, validate ignitions using Crystal Reports (FC34 & LE-66)*
  
   **4.** Login into [Crystals](https://webrpt.fire.ca.gov/BOE/BI)
   
        - Navigate to 'FC34 Detail-All Seg (Incident Number)
        - Authentication must be 'Enterprise'
        - Enter 2nd set of login credentials
        - Leave the top 2 fields (Start of Range & End of Range) blank
        - At bottom left box, type year of incident + 00 + #### (Incident Number)  ALWAYS WITH 4-DIGIT YEAR + 6-DIGIT INCIDENT ID
         eg. 2017001981
      ** Note: If the incident number has 5 digits (common at end of a year) use only 1 zero before incident Number eg. 2017010117
        - Click the '>' to transfer your incdient into the 'Selected Values' box
        - Then click 'OK'
        - Utilize the entire document to fill in the remaining information on the google spreadsheet
       - Top right will give Incident Name
        - 'Fire Information' heading will give name or jurisdiction of reporting person
        - 'Total Acres Burned' (compare this number to acreage at end of 'Incident Remarks' on page 2 or 3)
        - Latitude & Longitude (this is almost always the CAD location, so be sure to find an improved location at end of 'Incident Remarks' or use best judgement
         eg. Fire Type= FWLCD (Center divide fire) & location geolocates to middle of road (use google maps to determine a more appropriate lat & long)
      - 'Cause' (at times will be necessary to read all 'Incident Remarks' and deduce a probable cause of ignition) Otherwise, a majority of small fires will have a cause of 'Undetermined' which is not very helpful)
      **Note: In instances where an LE-66 report is not completed (for small fires generally) gleaning data from this FC-34 report has been the best resource 
      
**Periodically, (maybe every 2 weeks) check LE-66 reports (these are the authority, however they are not done for very small fires)**
     
   **5.** Use all same login info as in step 4 above
   
        - Navigate to 'LE-66 Detail'
        - In the 'Available Values' box, select 'SLU' then '>" 
        - In the 'Enter Date Range' boxes at bottom of page choose a start and end date
        - Click 'Add Range' and 'OK'
        - Once the report loads, click the 'Export this Report' (button with arrow pointing right) in the top left corner
        - Choose Microsoft Excel (97-2003) Data-Only, then 'Export'
        - Once exported, you can open this file and copy paste needed information
    
 *Google Sheet Notes*
 
   **6.** Miscellenous information about the spreadsheet 
   

   
        - 'Day' column will auto-populate once the date has been manually filled in (hover over bottom right corner of cell, click, and drag down)
        - Minimum fire size must be .1 acres (FireFamilyPlus will throw out all fires <.1 acres)
        - The bold font time in cell 'D2' uses a formula to compile the average report time.  Bold font in cell 'I2' tallies all acreage
        - Use Column Q ('Location Verified') as a check for validation of ignition locations (yes or No drop-down menu)
        - In Column L ('Comments'), note 'FC34' if that is the data source, or copy/paste any pertinent info from LE-66 report
        - '2017 LE-66 Detail' is meant as the most up-to-date sheet, and sends data to '2017 Graphs' tab 
        - 'master_Fire_Data_1950&1992-2017' is the master ignitions sheet for FDOP
        - '2017 TAB Report' and 'Sheet7' are rough draft tabs that may be able to be deleted
        - '2017 Graphs' sheet pulls all data from '2017 LE-66 Detail' to create statistically useful graphs by year
        - 'Miscellaneous Ignitions' sheet categorizes by type using the 'Sub Class' column (K)
      
**Note: LE-66 data is the authority dataset, so it is preferred over FC34, however, there are many more ignitions that do NOT get reported in LE-66 and therefore FC34 is the best resource**
          - LE-66 reports also have a bit of lag time in their completion, check the LE-66 report periodically as older fire reports may have been added

*Weather and Burning Index*

 1. Use the Lat & long and location address information to geolocate the ignition area
 
 2. Go to https://www.wunderground.com/wundermap and navigate to the area you wish to find the weather for
 
 3. Click a station that is relatively close and has reasonable weather readings.  Click hyperlink 'Station ID'
 
 4. In the new window scroll down the page to the heading 'Weather History for ..."  Change the date to the ignition date, then click 'view'
 
 5. Change the data type to 'Table' instead of the default 'Graph'.  Browse for the closest weather reading to the ignition time.  Be sure to fill in Temperature, Relative Humidity, Wind Speed, and Wind Direction in the 'master_fire_data' Google Sheet
 
  (Only complete this next step for fires 10+ acres in size)
  
  6. Naviagte to http://www.wfas.net/index.php/search-archive-mainmenu-92 . Check bubble entitled 'Do not use pop-up windows'.  Click in the empty box to select desired date, then click 'Submit'.
  
  7. On the new tab that opens, click the link for 'Observed Fire Danger Map Data'.  Once this text file opens type Ctrl + f, and in the box that appears in the upper right corner, type the name of weather station closest to desired ignition.  Record the BI on the Google Sheet.
  
        Options are: Arroyo Grande, Las Tablas, La Panza, SLO Coastal
