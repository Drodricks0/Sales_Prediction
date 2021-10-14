## Sales Prediction
As an amateur Data Scientist, I was tasked with 'cleaning' this data set that contains errors and typos. Once the data is cleaned and prepared, I created various visualizations to understand what the data tells us.' Having a baseline understanding of what the data is telling me, I used some machine learning techniques to identify models that best represent this data set.

# Important Visualizations: Where do we Begin?

![heat](https://user-images.githubusercontent.com/84295634/133169098-fde073df-1224-4085-9422-27072cd39f2a.png)

This heat map is used to identify any correlations within our data set. The darker colors resemble so kind of correlation with numbers ranging from -1 to 1. Item_MRP and Item_Outlet_Sales (our focus) have a moderate correlation.

# Item MRP Compared to Sales
![mrp](https://user-images.githubusercontent.com/84295634/133170245-cf8d3999-47c8-4915-b213-16b0fccea18a.png)

As the Item MRP increases, so does the possibility of generating more sales.

# Which Outlet is Selling More?

![bar graph](https://user-images.githubusercontent.com/84295634/133170695-f0e5c5f1-f512-464b-bb4b-009f5fa73c1b.png)

Supermarket Type 3 is generating the most sales compared to the other 'Outlet Types.'

# Which Features are Important?

![importance_0_1](https://user-images.githubusercontent.com/84295634/133174021-ed4933fd-b704-4efa-bc71-69de37b10ad2.png)
![importance_27](https://user-images.githubusercontent.com/84295634/133174024-d20ee875-3dac-4c86-93d5-de2789cf5ebd.png)
![importance_30](https://user-images.githubusercontent.com/84295634/133174028-1cb5a07c-d6e4-4428-8148-cce7f86e9189.png)

![importance](https://user-images.githubusercontent.com/84295634/133171576-0266a01a-16e0-4e8b-878f-77d758b1e110.png)

Just like what a heat map produces, for correlation, this bar chart shows us how 'important' the features is to producing the best outcome for our target: Item Outlet Sales. We have four features that stand out, and Item MRP contains the most influence on Sales. After that, the type of store which will equal the Type 3 supermarket.

## Machine Learning: Which model do we use?

I ran multiple models to identify which would be most accurate in predicting sales, and two models stood apart from the rest: Linear Regression and Random Forests.

Linear Regression  |  Random Forests
-------------------|----------------
R2 score           | R2 score       
Train: 0.561       | Train: 0.914
Test: 0.567        | Test: 0.486

Linear Regression | Random Forests
------------------|---------------
RMSE              | RMSE
Train: 1139.32    | Train: 1074.67
Test: 1092.52     | Test: 1092.52

Linear Regression and Random Forests capture the smallest error ($), which is essential since that dollar amount is trying to predict and minimize uncertainty. 

## Conclusion

Recommendations for capturing sales are:

Item MRP and the type of Outlet, precisely Supermarket Type 3: These two groups will aid in capturing more sales. Stakeholders should focus on sustaining higher MRP items in stock and order them more frequently as sales spikes appear.

As for which outlet style is gathering the most sales, Supermarket Type 3 is selling very well. Either build more Supermarket Type 3s or convert the other outlet types into modeling Type 3 (as in copying: Interior/Exterior Design, location of the product, carrying similar products, etc.)
