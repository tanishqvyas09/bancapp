Reconciliation Challenge Report – Bancapp

To finish this test, I have used Python and Pandas to create a small data reconciliation script between the API and Bank datasets.
First, I loaded both CSV files and cleaned the data by converting amounts to numeric format and dates to proper datetime format. Further, standardization was done on columns so that both sources matched up properly.
Then I joined both files on txn_id and created the matching rules on utr, amount, and txn_date. Using simple conditions, I labeled each record as an exact match, amount mismatch, status mismatch, missing in bank, or missing in API.

Then, I created separate CSV reports for each category, along with a summary showing the total count and match rate. I calculated the TAT in days between transaction and settlement dates to understand settlement delays for exact matches.

Then, I visualized the summary and mismatch causes in the form of a bar chart. This helped me quickly see where most mismatches occurred. The main concepts I applied were data cleaning, data merging, and conditional filtering in Pandas. It did indeed take me quite some time to get the merge and matching logic right, but once it worked, everything fell into place.
