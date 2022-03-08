import sqlite3
conn = sqlite3.connect("product.db")
# conn.execute('''CREATE TABLE PRODUCT(
# PRODUCTCODE INTEGER,
# PRODUCTNAME TEXT,
# PRICE INTEGER,
# DISTRIBUTORNAME TEXT,
# MANUFACTURERNAME TEXT);''')
# print("table created sucessfully")
getProductcode = input("enter productcode:")
getproductname = input("enter productname:")
getprice = input("enter price:")
getdistributorname = input("enter distributorname:")
getManufacturername = input("enter manufacturername:")

conn.execute("INSERT INTO PRODUCT (PRODUCTCODE,PRODUCTNAME,PRICE,DISTRIBUTORNAME,MANUFACTURERNAME)\
                   VALUES("+getProductcode+",'"+getproductname+"',"+getprice+",'"+getdistributorname+"','"+getManufacturername+"')")
conn.commit()
conn.close()
print("inserted sucessfully")
