# Slotted Pages 

* storage structure used in database systems to efficiently manage records within a page. They are designed to handle variable-length records and to support dynamic operations such as insertion, deletion, and updates
* (store tuple in page)
* Each Slot corresponds tuple 
* slot start to the top 
* slot start and add from end 


 
# Structure of a Slotted Page
* A slotted page typically consists of the following components:

* Header: The page header contains metadata about the page, such as the number of slots, the offset of the free space, and a pointer to the first free slot.
* Slots: Each slot in the page corresponds to a record. Slots contain pointers to the actual records stored in the data area of the page.
* Data Area: This area stores the actual records. Records can be of variable length and are stored compactly to minimize wasted space

* **Why Use** 
* improved Performance:-

* Access Speed: Slots provide direct pointers to the records, enabling quick access to records by simply following the pointer from the slot.
* Reduced Fragmentation: Slots help manage free space and reduce fragmentation since records can be moved and slots can be updated without shifting all records in the data area.

* Support for Dynamic Operations
* Metadata Management
* Simplified Record Management
* Efficient Management of Variable-Length Records
 ![1618490094733](https://github.com/ebrahimabdallah/FUNDAMENTALS-OF-Database-Systems/assets/119238955/acbb1058-36a8-4d51-99a8-8091937d6ef6)# Slotted Pages 


# Before Use Slotted
![1618490094733](https://github.com/ebrahimabdallah/FUNDAMENTALS-OF-Database-Systems/assets/119238955/211941ca-1533-4d8f-8648-fab3efca1ace)
)# Slotted Pages 

# After

![1618490094733](https://github.com/ebrahimabdallah/FUNDAMENTALS-OF-Database-Systems/assets/119238955/a5af471e-e17f-4207-b91f-83819b9076cc)

# Challenge
* Too Much Disk I/O
* Random Disk I/O
* Fragmentation

# Record ID

* Unique 
* Represents physical location  
* usually not stored with tuple

* Structure of Record IDs
* Page Number: This is an integer value that uniquely identifies a page in the database file. It allows the system to navigate to the correct page directly.
* Slot Number: This is an integer value that identifies the slot within the page. Slots are used to store pointers to the actual records in the data area of the page.
