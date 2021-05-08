## Data Analysis arrived in the Quality Assurance department

In this project, I am working on a food company supplier list that contains two main columns: fei and brc codes.

The FEI number is the FDA Firm Establishment Identifier, and it is a unique indentifies assigned by the FDA.
Visiting the URL https://datadashboard.fda.gov/ora/firmprofile.htm?FEIs={'fei'}, quality specialists can access all FDA public information, including inspections, recalls, and other actions related to a facility.
For this project, the FDA inspection date and company address are the data necessary to scrape from the web.

BRC is an international Food Safety Management System standard recognized by the GFSI (Global Food Safety Initiative).
Visiting the url https://directory.brcgs.com/site/{'brc'}, quality specialists can access certification grade, date, scope of the certification and other information from a facility. The BRC site code is specific for a company address. Note that not all suppliers have this certification.

# Objective

Refer to the file supplier_info.csv file. Use the fei list to get the FDA last inspection date from each supplier. Use the brc code to get the company name, address, certification grade and expiration date from the brc website.

Generate a score for the suppliers. 
FDA Score - Based on the last FDA inspection:
- If FDA inspection it is over 3 years - 50 points
- If FDA inspection it is over 2 years - 20 points
- If FDA inspection it is less than 2 years - 0 points
- If no FDA inspection - 100 points

BRC Score - Based on BRC audit grade:
- If AA+ or AA - 0 points
- If A or B - 10 points
- If C or D - 30 points
- If no BRC certification or certificate expired - 100 points

Final score will be the sum of FDA and BRC scores and can vary from 0 to 200.


# Development

A file fda_brc_web was generated to get the data.
The final list withthe suppliers and scores are stored in XXX file.

