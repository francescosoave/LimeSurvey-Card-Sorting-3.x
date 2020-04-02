# Card Sorting for LimeSurvey 3.x

**A custom question theme for "card sorting" in LimeSurvey 3.x**

**fork of: https://github.com/tpartner/LimeSurvey-Card-Sorting-3.x**

![Image Card Sorting](/cardSort/survey/questions/answer/multipleshorttext/assets/images/screen2.png)
![Image Card Sorting](/cardSort/survey/questions/answer/multipleshorttext/assets/images/screen1.png)


**Changes:**

**- Improved UI for longer sentences**

**- Options now follow mouse scroll**



**Implementation:**

1) Extract the download and upload the **cardSort** folder to */pathToLimeSurvey/upload/themes/question/*.

2) Create a multiple-short-text question, click Save.

3) Set the question setting "Question theme" to "cardSort", click Save.  
![Image Select cardSort](/cardSort/survey/questions/answer/multipleshorttext/assets/images/card_sort_3.x_1.png)

4) In the question setting "Sorting area names" field, enter a comma-separated list of the names for the sorting "buckets", click Save.  
![Image Enter Bucket names](/cardSort/survey/questions/answer/multipleshorttext/assets/images/card_sort_3.x_2.png)

5) Create subquestions as required.


**About mandatory options**

Assuming you need:
- all the options to be categorized in your groups
- at least a certain number of groups must have at least 1 option

You can to do this:
- set the question as mandatory under *General Options* menu (this will force the user to move all the options in the groups)
- Add a validation expression to set how many groups must be filled (at least).
This can be done under *Edit question -> Logic -> Question validation equation*.

The equation is: `countifop("==","1",self.NAOK)>0` for 1 group, `countifop("==","1",self.NAOK)>0 AND countifop("==","2",self.NAOK)>0` for 2 groups and so on..


**Notes:**

1) The styles for the theme can be modified in */pathToLimeSurvey/upload/themes/question/cardSort/survey/questions/answer/multipleshorttext/assets/css/cardsort.css*.

2) Array filter and array filter exclusion will only work if the filtering question is on a previous page.

3) Demo survey in */cardSort/survey/questions/answer/multiplenumeric/assets/demo/*.
    
    
*Custom themes are given without any warranty, implied or otherwise.*
