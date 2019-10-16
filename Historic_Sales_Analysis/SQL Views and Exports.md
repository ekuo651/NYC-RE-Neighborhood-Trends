## Views and Queries for Historic Real Estate Data


### Views were created to merge the sales data of each borough throughout the years, from 2003 to 2018. This was done for each borough.

```
--- view of staten from 2003 to 2018
CREATE VIEW staten_sales AS
 SELECT staten_2003."NEIGHBORHOOD",
    staten_2003."BUILDING CLASS CATEGORY",
	staten_2003."BLOCK",
	staten_2003."LOT",
    staten_2003."ZIPCODE",
    staten_2003."SALE PRICE",
    staten_2003."SALE DATE"
   FROM staten_2003
UNION ALL
 SELECT staten_2004."NEIGHBORHOOD",
    staten_2004."BUILDING CLASS CATEGORY",
	staten_2004."BLOCK",
	staten_2004."LOT",
    staten_2004."ZIPCODE",
    staten_2004."SALE PRICE",
    staten_2004."SALE DATE"
   FROM staten_2004
UNION ALL
 SELECT staten_2005."NEIGHBORHOOD",
    staten_2005."BUILDING CLASS CATEGORY",
	staten_2005."BLOCK",
	staten_2005."LOT",
    staten_2005."ZIPCODE",
    staten_2005."SALE PRICE",
    staten_2005."SALE DATE"
   FROM staten_2005
UNION ALL
 SELECT staten_2006."NEIGHBORHOOD",
    staten_2006."BUILDING CLASS CATEGORY",
	staten_2006."BLOCK",
	staten_2006."LOT",
    staten_2006."ZIPCODE",
    staten_2006."SALE PRICE",
    staten_2006."SALE DATE"
   FROM staten_2006
UNION ALL
 SELECT staten_2007."NEIGHBORHOOD",
    staten_2007."BUILDING CLASS CATEGORY",
	staten_2007."BLOCK",
	staten_2007."LOT",
    staten_2007."ZIPCODE",
    staten_2007."SALE PRICE",
    staten_2007."SALE DATE"
   FROM staten_2007
UNION ALL
 SELECT staten_2008."NEIGHBORHOOD",
    staten_2008."BUILDING CLASS CATEGORY",
	staten_2008."BLOCK",
	staten_2008."LOT",
    staten_2008."ZIPCODE",
    staten_2008."SALE PRICE",
    staten_2008."SALE DATE"
   FROM staten_2008
UNION ALL
 SELECT staten_2009."NEIGHBORHOOD",
    staten_2009."BUILDING CLASS CATEGORY",
	staten_2009."BLOCK",
	staten_2009."LOT",
    staten_2009."ZIPCODE",
    staten_2009."SALE PRICE",
    staten_2009."SALE DATE"
   FROM staten_2009
UNION ALL
 SELECT staten_2010."NEIGHBORHOOD",
    staten_2010."BUILDING CLASS CATEGORY",
	staten_2010."BLOCK",
	staten_2010."LOT",
    staten_2010."ZIPCODE",
    staten_2010."SALE PRICE",
    staten_2010."SALE DATE"
   FROM staten_2010
UNION ALL
 SELECT staten_2011."NEIGHBORHOOD",
    staten_2011."BUILDING CLASS CATEGORY",
	staten_2011."BLOCK",
	staten_2011."LOT",
    staten_2011."ZIPCODE",
    staten_2011."SALE PRICE",
    staten_2011."SALE DATE"
   FROM staten_2011
UNION ALL
 SELECT staten_2012."NEIGHBORHOOD",
    staten_2012."BUILDING CLASS CATEGORY",
	staten_2012."BLOCK",
	staten_2012."LOT",
    staten_2012."ZIPCODE",
    staten_2012."SALE PRICE",
    staten_2012."SALE DATE"
   FROM staten_2012
UNION ALL
 SELECT staten_2013."NEIGHBORHOOD",
    staten_2013."BUILDING CLASS CATEGORY",
	staten_2013."BLOCK",
	staten_2013."LOT",
    staten_2013."ZIPCODE",
    staten_2013."SALE PRICE",
    staten_2013."SALE DATE"
   FROM staten_2013
UNION ALL
 SELECT staten_2014."NEIGHBORHOOD",
    staten_2014."BUILDING CLASS CATEGORY",
	staten_2014."BLOCK",
	staten_2014."LOT",
    staten_2014."ZIPCODE",
    staten_2014."SALE PRICE",
    staten_2014."SALE DATE"
   FROM staten_2014
UNION ALL
 SELECT staten_2015."NEIGHBORHOOD",
    staten_2015."BUILDING CLASS CATEGORY",
	staten_2015."BLOCK",
	staten_2015."LOT",
    staten_2015."ZIPCODE",
    staten_2015."SALE PRICE",
    staten_2015."SALE DATE"
   FROM staten_2015
UNION ALL
 SELECT staten_2016."NEIGHBORHOOD",
    staten_2016."BUILDING CLASS CATEGORY",
	staten_2016."BLOCK",
	staten_2016."LOT",
    staten_2016."ZIPCODE",
    staten_2016."SALE PRICE",
    staten_2016."SALE DATE"
   FROM staten_2016
UNION ALL
 SELECT staten_2017."NEIGHBORHOOD",
    staten_2017."BUILDING CLASS CATEGORY",
	staten_2017."BLOCK",
	staten_2017."LOT",
    staten_2017."ZIPCODE",
    staten_2017."SALE PRICE",
    staten_2017."SALE DATE"
   FROM staten_2017
UNION ALL
 SELECT staten_2018."NEIGHBORHOOD",
    staten_2018."BUILDING CLASS CATEGORY",
	staten_2018."BLOCK",
	staten_2018."LOT",
    staten_2018."ZIPCODE",
    staten_2018."SALE PRICE",
    staten_2018."SALE DATE"
   FROM staten_2018;
   
```

### Query was written to eliminate small transactions that were likely to be transfers, and not sales. The dataset was then exported to a csv, ready to be analyzed with Jupyter Notebook.

```
--- query to eliminate transactions that are likely transfers rather than sales
SELECT "NEIGHBORHOOD", "BUILDING CLASS CATEGORY", "ZIPCODE", "SALE PRICE", "SALE DATE"
	FROM public."staten_2018-2003"
	WHERE "SALE PRICE" > 3000;
```
	

	
