
## Style transfer

This implementation of text style transfer uses two fine-tuned MLM BERTs. The first one is fine-tuned on positive reviews, the second - on negative reviews. 

Next define a function that will find most "negative" words in sentence and replace it with positive. The negativeness means 

```bash
               P_negative_model(word=sentence[i], context=sentence)
negativeness = ----------------------------------------------------
               P_possitive_mode(word=sentence[i], context=sentence)
```

To choose which words to replace I used beam search.

### Results

This place is weird and I do not like it at all!  
This place is great and i do really like it after all!

The prices are high and the staff were terrible.  
Their prices are great and the staff is great!

Never buy this product this is really bullshit!  
I like this and it is really great!

Very delicious coffee and pancakes! (already positive)  
Very delicious coffee and pancakes! (Didn't change at all)

[Colab link](https://colab.research.google.com/github/konductor000/Style-transfer-BERT/blob/main/style_transfer.ipynb)