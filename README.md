# About the data

This dataset of auto loans was assembled from U.S. Securities and Exchange Commission filings submitted in 2019 and 2020. Seventeen major lenders made these required disclosures to auto-loan bond investors. The data includes 857,904 loans from 17 major lenders that were bundled together into asset-backed securities. It contains details about each loan and borrower, including the borrower’s credit score, monthly payment, estimated income level, employment status, vehicle value, loan amount, co-borrower status, vehicle make and model. The data are not nationally representative, since it only includes loans that were packaged into securities for investors.

# About the data cleaning

We cleaned the data in several ways before analyzing it. To ensure consistency within features, we trimmed unnecessary white space from the lender's names column, standardized all interest-rate percentages to decimal values, converted the borrower's credit score feature from non-numeric to numeric (replacing text describing no available credit score for that borrower with NA), and excluded cases where state abbreviations did not match standard U.S. state abbreviations. 

We excluded values of three numeric features that were not reasonable: We excluded borrower credit scores that were less than 300 and greater than 900, payment-to-income ratios less than or equal to 0 or greater than 1, and vehicle values less than $5,000 and greater than $100,000. To address potential outliers in numeric variables such as the borrower's credit score, vehicle value, estimated payment-to-income ratio, original loan term, and original interest rate, we removed the top and bottom 1% of the data in each of the columns. Finally, two lenders, Fifth Third Bank and World Omni, charged a fee in certain states (Fifth Third in OH, KY and IN; World Omni in FL and GA) that would have affected the original interest rates, so loans from those lenders in those respective states were excluded from the analysis.

# Read CR's 2021 investigation using this data
https://www.consumerreports.org/car-financing/many-americans-overpay-for-car-loans-a8076436935/

# Links to original raw data
* Ally Bank: https://www.sec.gov/Archives/edgar/data/1477336/000147733619000005/ex102jan2019aart201911.xml
* BMW: https://www.sec.gov/Archives/edgar/data/1136586/000092963820000701/bmw2020-a_exhibit102.xml
* CapitalOne: https://www.sec.gov/Archives/edgar/data/1133438/000095013120000420/copart201ex102_0204-1127lp.xml
* CarMax: https://www.sec.gov/Archives/edgar/data/1259380/000125938020000004/cart20201u.xml
* Exeter Finance: https://www.sec.gov/Archives/edgar/data/1654238/000092963820000909/exhibit102.xml
* Fifth Third Bank: https://www.sec.gov/Archives/edgar/data/1405332/000095013119001203/ftat191ex102_0422-0921.xml
* Ford: https://www.sec.gov/Archives/edgar/data/1129987/000112998720000017/spautoloaninitialdeal1021poo.xml
* GM: https://www.sec.gov/Archives/edgar/data/1347185/000134718519000039/exh1024030112019.xml 
* Honda: https://www.sec.gov/Archives/edgar/data/890975/000095013120000427/harot201ex102_0211-1525lp.xml
* Hyundai: https://www.sec.gov/Archives/edgar/data/1260125/000110465920046309/hca-autoloanex102_041020201.xml
* Mercedes: https://www.sec.gov/Archives/edgar/data/1463814/000095013120002018/mbart201ex102_0603-1600.xml
* Nissan: https://www.sec.gov/Archives/edgar/data/1129068/000095013120001411/narot20aex102_0416-1108lp.xml
* Santander Bank: https://www.sec.gov/Archives/edgar/data/1383094/000095013120001209/sdart201ex102_0408-1810lp.xml
* Toyota: https://www.sec.gov/Archives/edgar/data/1131131/000095013120000413/taot20aex102_0123-1428lp.xml
* USAA: https://www.sec.gov/Archives/edgar/data/1178049/000095013119002200/usaot191ex102_0716-2027.xml
* Volkswagen: https://www.sec.gov/Archives/edgar/data/1182534/000095013120001599/valet201ex102_0505-1811lp.xml
* World Omni: https://www.sec.gov/Archives/edgar/data/1083199/000110465920101638/wosat2020aaex102jul20upsize.xml
