# Fork of Card Sorting for LimeSurvey 3.x

**A custom question theme for "card sorting" in LimeSurvey 3.x**

**original: https://github.com/tpartner/LimeSurvey-Card-Sorting-3.x**

![Image Card Sorting](/cardSort/survey/questions/answer/multipleshorttext/assets/images/screen2.png)
![Image Card Sorting](/cardSort/survey/questions/answer/multipleshorttext/assets/images/screen1.png)

**Improved UI for longer sentences**

**Add Placeholders options (see below)**


**Implementation:**

1) Extract the download and upload the **cardSort** folder to */pathToLimeSurvey/upload/themes/question/*.

2) Create a multiple-short-text question, click Save.

3) Set the question setting "Question theme" to "cardSort", click Save.  
![Image Select cardSort](/cardSort/survey/questions/answer/multipleshorttext/assets/images/card_sort_3.x_1.png)

4) In the question setting "Sorting area names" field, enter a comma-separated list of the names for the sorting "buckets", click Save.  
![Image Enter Bucket names](/cardSort/survey/questions/answer/multipleshorttext/assets/images/card_sort_3.x_2.png)

5) Create subquestions as required.

**Placeholder options**

- You can create placeholders to force the user to fill at least a set number of groups
- First you need to make the answers mandatory (this will make them mandatory for each group)
- Then create a number of Placeholder options. To be identified as placeholder this options should have a code starting with "Def" such as: Def1, Def2, Def3 and so on.

For example:
- I have 10 options and 5 groups. I want users to group the options in AT LEAST 2 groups.
- First, I set the answers as mandatory. Then I create 3 placeholder options.
- The user will only be able to submit if every group contains at least 1 answer (because we made it mandatory). Assuming the user wants to only have 2 groups, he/she will then be able to use the placeholders (one for each empty group) and submit the form.

**Notes:**

1) The styles for the theme can be modified in */pathToLimeSurvey/upload/themes/question/cardSort/survey/questions/answer/multipleshorttext/assets/css/cardsort.css*.

2) Array filter and array filter exclusion will only work if the filtering question is on a previous page.

3) Demo survey in */cardSort/survey/questions/answer/multiplenumeric/assets/demo/*.
    
    
*Custom themes are given without any warranty, implied or otherwise.*
