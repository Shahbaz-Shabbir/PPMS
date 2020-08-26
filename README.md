# PPMS
Petrol Pump Management System By Shahbaz Shabbir

##UPDATES

  27-July-2020
    Add Collem 'DDShahbazPPMS' in product table with nchar 255
    
##Views
###Replace ProductViewForSales (if error occured on product add button in sale invoice) with following.


                              SELECT        dbo.Products.ProductId, RTRIM(dbo.Products.ProductName) AS ProductName, dbo.Stock.Stock, dbo.Stock.SalePrice, dbo.Stock.PurchasesPrice , dbo.Stock.SaleDiscount, CASE WHEN dbo.Products.Service IS NULL THEN 0 ELSE dbo.Products.Service END AS Service
FROM            dbo.Products INNER JOIN
                         dbo.Stock ON dbo.Products.ProductId = dbo.Stock.ProductId
WHERE        (dbo.Products.Active = 1)



                               Shahbaz Shabbir (Computer Software Engineer)
