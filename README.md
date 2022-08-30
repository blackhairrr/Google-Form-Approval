# Google-Form-Approval
<img width="651" alt="PNG image" src="https://user-images.githubusercontent.com/37354986/186953736-0b830d66-5e1b-4dff-95f7-0a9eaa12526c.png">


User submit form > Approver get email to approve > User get email approved status > Data recorded in Google Sheet

## 1. Create questions in Google Form
### Create form. Create some questions. After that, test submit some response.
![form 1](https://user-images.githubusercontent.com/37354986/187424177-e65a8c01-39af-4783-a9c4-322ac21cfcf7.PNG)


### Open setting tab. Enable collect email addresses
![Enable collect email address](https://user-images.githubusercontent.com/37354986/186952887-779063b2-7f4d-4cdf-8c38-79976501883c.png)

### Open response tab and click on sheet icon to link with Google Sheet automatically
![Click on sheet to link with Google Sheet Automatically](https://user-images.githubusercontent.com/37354986/186953337-05b8e394-886d-4d78-8e06-cdaf8af464a0.png)

### Create new sheet
![Create sheet](https://user-images.githubusercontent.com/37354986/186953432-d7e0af23-259b-436a-bd35-66afd7ff4246.png)

### Open sheet to see the data.
![sheet 1](https://user-images.githubusercontent.com/37354986/187425437-95d767bf-dd00-4387-befe-61f4f58dc2e2.PNG)
## 2. Create form for approval section.
![form 2](https://user-images.githubusercontent.com/37354986/187426097-7c5684c0-53d6-43e2-be9c-d0b7ebd993f7.PNG)
### Open setting tab, set all same as the previous form. Enable collect email addresses.
![form 3](https://user-images.githubusercontent.com/37354986/187429454-5fac9b49-3878-4817-94be-35f8cd856879.PNG)

## 3. Create approval using Form Mule and Copy Down extension from google spreadsheets marketplace.
### Rename the sheet for requestor workbook and approver workbook.
![sheet 2](https://user-images.githubusercontent.com/37354986/187430226-077d6220-5c47-4314-b465-d1906d908058.PNG)
![sheet 3](https://user-images.githubusercontent.com/37354986/187430384-56bf53d3-f52a-4c88-9a1e-8e5aa27f0309.PNG)

### Configure Form Mule
Select cell, I use cell G1. Open extensions tab, select Form Mule and Launch.
![sheet 4](https://user-images.githubusercontent.com/37354986/187431031-7d09e1cd-90a1-4d4f-aa9e-9b9ff1db3254.PNG)

1-Select sheet
2-turn on to enable
3-tick on case no
4-go next
![sheet 5](https://user-images.githubusercontent.com/37354986/187431521-7d66a84e-7bf8-4f42-80a3-3eaf2dfff127.PNG)

Just click okay if this dialogs appear
![sheet 6](https://user-images.githubusercontent.com/37354986/187431593-940b68dd-e71c-4ef1-b110-f93437c27ff4.PNG)

Rename the email template and select one condition.
![sheet 7](https://user-images.githubusercontent.com/37354986/187431963-52f19dba-e8d6-49ca-937c-7d090657c30c.PNG)

This dialog is used to set up the email that will forward to the approval. Fill out all the details.
![sheet 8](https://user-images.githubusercontent.com/37354986/187432222-6fdcb057-b4a9-418b-9e37-9f06f04b2bf6.PNG)

You can put some HTML code in the body. I use the button code for approval to click and approve. Insert the approval form link.
![sheet 9](https://user-images.githubusercontent.com/37354986/187433019-117ae64a-1db7-4276-947d-d898bd6b55d3.PNG)

Click on save and preview. Your email will look like this. Done for requestor part.
![sheet 10](https://user-images.githubusercontent.com/37354986/187433178-ebee10dc-d884-42a9-8838-5b7717842c0c.PNG)

Open the extension, select Form Mule, and generate the case number.

![sheet 11](https://user-images.githubusercontent.com/37354986/187433634-6215b817-dc49-4d2d-98b5-cec69f64dad6.PNG)

### Lets test submit a respone. I got an emel from my submission. And a set of data. Test the submit button also.

![emel 1](https://user-images.githubusercontent.com/37354986/187436896-fa1b7366-3575-4aa4-82fb-1034a212948a.PNG)

From my google sheet.
![sheet 12](https://user-images.githubusercontent.com/37354986/187436914-d7527572-b33b-474c-aac5-920bc28be881.PNG)

### Now lets configure the approver workbook spreadsheet.

![sheet 13](https://user-images.githubusercontent.com/37354986/187437674-d19441a1-6a25-452a-9140-27959b760286.PNG)

Configure same as before.

![sheet 14](https://user-images.githubusercontent.com/37354986/187438104-f7eaaf21-b8c1-45ed-9e1c-28ed57239f2a.PNG)

Lets test the approval submission.

![emel 2](https://user-images.githubusercontent.com/37354986/187438499-16f397fd-d1d9-489e-a4da-4038aeb357c4.PNG)
Everything goes well. And my case number automatically generated.
![sheet 15](https://user-images.githubusercontent.com/37354986/187438748-b1974812-408c-4a54-a143-9c6723677947.PNG)

Add some formula. We want to make this approval sending the email depends on the requestor email.
this is the formula =VLOOKUP(D3,IMPORTRANGE("https://docs.google.com/spreadsheets/d/1rRQm8hqTX9jw527SXyIZY9PjvTGBWgA9hOILk3ZOIg0/edit?resourcekey#gid=310135806","Requestor!B:C"),2,0)

use importrange if you use the different workbook. Put the sheet name and cell that we want to look up.

![formula](https://user-images.githubusercontent.com/37354986/187439983-e437b558-4e0a-4430-b248-93649529e130.PNG)

Allow the access.
![sheet 17](https://user-images.githubusercontent.com/37354986/187440088-2b083adb-5e1b-4e47-92dd-9c6382deb214.PNG)

The data will appear.
![sheet 18](https://user-images.githubusercontent.com/37354986/187440763-3b448dca-4066-4f36-84bd-fc2c5636a37f.PNG)

Now, open the Form Mule, select setup and select build/preview template to change the email to requestor email.
![sheet 19](https://user-images.githubusercontent.com/37354986/187441651-2cff89c4-cb5b-4ff8-9150-74d1064fc53e.PNG)

Click on cell that has formula, then click on extension tab, select copy down, and enable.
![sheet 20](https://user-images.githubusercontent.com/37354986/187443179-d8e6b5dc-689f-4df9-8c38-01ef97985d04.PNG)

Save the setting
![sheet 21](https://user-images.githubusercontent.com/37354986/187443448-e3a54853-04d7-4ae8-a5b7-862b4b4f8982.PNG)

Automatic email after approval will received.
![sheet 22](https://user-images.githubusercontent.com/37354986/187443960-845f3d51-8e4b-4d16-9059-c49d52d5dbe7.PNG)

## Done.
