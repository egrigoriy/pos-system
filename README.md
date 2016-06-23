Point of Sale (POS) system

This project was inspired by Isaiah Perumalla's article in MSDN Magazine in June 2009 entitled "Using Mocks and Tests to Design Role-Based Objects". In that paper a POS system was developped in TDD style, so the design was "guided" by unit tests.
The system is not very complex, so in this case such appoach is probably justified.
However, my target is to develop a POS system appliyng Responsibility-driven design (RDD) methodology proposed by Rebecca Wirfs-Brock.

The specifications as declared Isaiah Perumalla's article (https://msdn.microsoft.com/magazine/dd882516.aspx):

Reading Barcodes
I am building a point-of-sale system for a large supermarket chain. The product catalog systems are in the head office and accessed by a RESTful service. The main focus for the first feature is for the system to use barcode information, either manually entered or read from a barcode scanner, to identify an item, retrieve its price, and calculate the total receipt for the sale.
The system is triggered when the cashier enters commands using a touch screen or a barcode scanner. Commands from input devices are sent as a string in the following format:
Command: NewSale; 
Command: EndSale; 
Input: Barcode=100008888559, Quantity =1; 
All barcodes follow the UPC scheme; the first six characters of the barcode identify the manufacturer code, and the next five characters identify a product code. The product information system requires the manufacturer code and product code to be able to retrieve product description for an item. 
The system first needs to receive and interpret commands from input devices (keyboard and scanners). When the sale is finished, the system should calculate and print a receipt using the product catalog from the head office to retrieve product description and price.


Sidebar: An interesting feature is to extend the system for different types of barcodes (EAN,....)  
