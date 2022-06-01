---
description: >-
  These features can be found in the scorecard section of the admin dashboard
  and allow for uploaded data to be compiled and presented on the Municipal
  Money scorecard page
---

# Geographies and profile compilation

## Geographies <a href="#compiling-municipal-profiles" id="compiling-municipal-profiles"></a>

This is used to set the general information and contact details at the top of each scorecard page.\


![](<../.gitbook/assets/image (24).png>)

### Updating contact details

Geography data uses an import/export approach to allow for updating geographies individually or in bulk.  The options shown below can be used to select the file and format to import or export.

![](<../.gitbook/assets/image (20).png>)

{% hint style="info" %}
The columns needed to update municipality contact details are

`geo_code, postal_address_1, postal_address_2, postal_address_3, street_address_1, street_address_2, street_address_3, street_address_4, phone_number, fax_number, url`
{% endhint %}

### Geography data format

The geo\_code column is required to identify the geography to be updated by a given row. All other columns and rows are optional.

{% hint style="info" %}
**Only include the columns you intend to update.** Including blank columns will overwrite that data.
{% endhint %}

The import tool shows a list of valid column headers, and offers a selection of import formats.&#x20;

{% hint style="info" %}
**xlsx** is probably the easiest to avoid encoding issues.
{% endhint %}

![](../.gitbook/assets/Screenshot\_2022-06-01\_17-27-48.png)

#### Example CSV containing all data fields

```
geo_level,geo_code,name,long_name,square_kms,parent_level,parent_code,province_name,province_code,category,miif_category,population,postal_address_1,postal_address_2,postal_address_3,street_address_1,street_address_2,street_address_3,street_address_4,phone_number,fax_number,url
municipality,BUF,Buffalo City,"Buffalo City, Eastern Cape",2751.69154949282,province,EC,Eastern Cape,EC,A,A,781026,P O BOX 134,EAST LONDON,5200,Trust Bank Centre,C/O Oxford & North Street,East London,5200,043 705 2000,043 743 8568,http://www.buffalocity.gov.za
municipality,TSH,City of Tshwane,"City of Tshwane, Gauteng",6310.21760217517,province,GT,Gauteng,GT,A,A,2921488,P O BOX 6338,PRETORIA,0001,Isivuno House,Cnr Lilian Ngoiyi & Madiba Street,Pretoria,0002,012 358 7911,012 358 1112,http://www.tshwane.gov.za
```

#### Example CSV with just an optional fields for phone number

```
geo_code,phone_number
BUF,043 705 2000
```

The import tool will show a preview of changes to be confirmed before applying them:

![](../.gitbook/assets/Screenshot\_2022-06-01\_17-10-40.png)

## Compiling municipal profiles <a href="#compiling-municipal-profiles" id="compiling-municipal-profiles"></a>

In order for the data made available by the Municipal Money platform to be displayed on the Municipal Profiles displayed on the site, a 'Municipal Profile Compilation' has to be initiated.

To see a list of previous compilations that were initiated, we can click on the appropriate item in on the home page.

![](<../.gitbook/assets/Screenshot 2021-02-22 at 05.58.44.png>)

Once we've clicked on the 'Municipality Profile Compilations' item, we will be presented with a page where we can see previous compilations and create new ones.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 07.56.26.png>)

Here we have a list of previous compilations, ordered by date, and an indication to the users that initiated the compilation and the periods that were targeted as the focus of the compilation. From this page we can make use of the 'ADD MUNICIPALITY PROFILE COMPILATION' button to initiate a new compilation.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 08.00.50.png>)

At this point we can indicate the years that we would like to target during the compilation, with defaults provided from the system configurations discussed in the 'System configurations' chapter. Once we're happy with the years that we'd like to target we can initiate the compilation by clicking the 'SAVE' button.

![](<../.gitbook/assets/Screenshot 2020-12-22 at 08.07.23.png>)

We should now be redirected back to the page listing all the previous compilations, and our newly created compilation should now be included on the list.

Creating a new 'Municipality Profile Compilation' will start a task on the backend that processes the compilation. Refer to the 'Checking task status' chapter of this guide to find out more about tasks.

##
