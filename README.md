### Welcome to the Text Style Transfer project!

This project, which was implemented in Google Colab, uses two fine-tuned MLM BERT models to transfer the style of text from negative to positive. The first model is fine-tuned on positive reviews, and the second model is fine-tuned on negative reviews.

The project also includes a function called get_replacements() that can find the most "negative" words in a sentence and replace them with their positive equivalents. The negativeness of a word is determined by the ratio of its likelihood of appearing in negative reviews to its likelihood of appearing in positive reviews `P(negative) / P(positive)`.

You can fine-tune the BERT models on your own dataset of positive and negative reviews. Then, you can use the `get_replacements()` function to perform the text style transfer on any sentence.

Please note that this project is for educational and research purposes only, and the results may not always be accurate or applicable to every use case. It's recommended to thoroughly evaluate and test the model on your specific dataset before using it in production.

### Examples:

    "This place is weird and I do not like it at all!" becomes "This place is great and i do really like it after all!"
    "The prices are high and the staff were terrible." becomes "Their prices are great and the staff is great!"
    "Never buy this product this is really bullshit!" becomes "I like this and it is really great!"
    "Very delicious coffee and pancakes!" (already positive) doesn't change.

To use this project, you can run the code in Google Colab notebook by following this link:  
[Colab link](https://colab.research.google.com/github/konductor000/Style-transfer-BERT/blob/main/style_transfer.ipynb)
