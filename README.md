Votesmart
=========

NPAT/PCT

This file contains the documentation on how to get the survey responses or the PCT forms filled by candidates using votesmart API.

Now, my code lies in npat.php
It is using the NPAT class method. See this link http://api.votesmart.org/docs/Npat.html
I am saving the responses in a file called original_survey_responses.xls
I have used || as the separator. Save it in xlsx format, then you wont have to use || separator everytime you open the file.


When you open original_survey_responses.xlsx file, you can see that one row is having the headers, and one row below it is having the values.

The reason that I am adding headers for every candidate is because they might have filled different PCT forms.

If you browse more through this file, you may notice that for some candidates their NPAT forms may differ even if their "NPAT Name" is same, thus there is no way you can separate out the common responses through code. This is a defect in votesmart's API.

In simple words, "NPAT Name" shows the name of the lates NPAT/PCT form that the candidates have received, and the form which we get is the latest form which they have "filled". Thus the form may or may not be the "NPAT Name" which is being shown. 

You may also notice few blank rows, these are the candidates who show no information when their ids are fed into NPAT methods.

The only way you can separate out the common survey responses is through manually traversing through the file, until votesmart people clean their APIs.

After manually cleaning the original file, I created the final_survey_responses.xlsx file.

This is the final file. Around 508 candidates.

There are a number of sheets. Each sheet is a particular form, and also contains the responses of the candidates who have filled that form number. All sheets are in the form of number except the first two. the first sheet holds candidates who haven't ever filled the form, and second sheet holds the candidates which have never qualified to receive the NPAT form. 

All the other sheets are having candidates who have common NPAT/PCT forms. I had to manually check all the forms of candidates and then added them to a particular sheet.

Though originally there were around 650 candidates, but in the end around 508 are there in the file. This is because of the empty fields for many candidates.

I have tried to mention all the issues that I got during writing this code.
For any further query, contact me at mittal.anant@gmail.com
I will be more than happy to help.
