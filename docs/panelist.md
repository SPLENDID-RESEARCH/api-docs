# Explanation

In order to be able to send invite request you need to have access to our panelbase.<br />
This is being achieved by implementing a panelist transfer to you.<br />
After an initial import of our panels, this method will continue to transmit new panelist to you, as well as inform you about changes in profile and deleted panelist.<br />
We offer a lot of profiling information for you to choose from which can also be mapped to already existing categories you have in place.<br />

*Please note: Variable names and value labels will depend on what your system accepts.*


# Profile Information

The following profile information is mandatory and has to be shared with you:<br />

* Member ID
* Country ISO
* Language ISO
* Birthday
* Gender
* Postcode

We would suggest to use at least the following profile information for better targeting:<br />

* Occupation 
* Accommodation
* Household Size
* Number of Children
* Personal Income
* Household Income
* Industry of Organization
* Decision Maker
* IT Position
* Access to Car(s)
* Primary Grocery Shopper 
* Education
* Marital Status

Additionally to that we offer more than 100 more specific profiling points within the following categories:<br />

* **DEMOGRAPHICS**
* **HOUSEHOLD**
* **JOB**
* **CAR**
* **ELECTRONICS**
* **SMOKING**
* **DEMOGRAPHICS**
* **HEALTH**
* **TRAVEL**
* **MEDIA**
* **MOTHER/BABY**
* **HOBBIES**
* **EDUCATION**
* **DRINKS/FOOD**
* **GAMING**

Just [contact us](mailto:api@splendid-research.com) if you want more information on our extended profiling.<br />


# Transmission

The transmission of panelist can be done via API or FTP file upload. However the API approach is way more superior.<br />
Next to any profiling information, each call also contains the information whether the panelist is a new one to be added, an already existing one who adjusted their profile or a panelist who should be deleted:<br />

Value | Explanation
--- | ---
new | This panelist has to be added by you yet
change | This panelists profile should be updated
delete | This panelist should be deleted

# Example

*Please note: Variable names and value labels will depend on what your system accepts.*

```
{
		"member_id": "349-1-123456789",
		"status" : "new"
		"country_iso_code": "US",
		"language": "en",
		"birthday": "1992-08-22",
		"gender": 1,
		"postcode": 13661,
		"occupation": 7,
		"marital_status" : 3,
		"education" : 5,
		"p_income" : 2,
}
```