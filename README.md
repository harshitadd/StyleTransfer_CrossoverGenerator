# Crossover Generator Nesting Style Transfer

This project uses style transfer NLP to create a crossover between 2 core plots and then uses Open AI GPT-2  (117M ) to predict the extension plot of the given crossover data.  

The given Network has 12 layers in comparison to the more diverse 48 layer 1.5MB dataset which has not been made public as yet. 

What we are doing ? 

# OPTION 1 
Core feature - Use of GPT-2 to create plots based on different features of the seed text. 

Give us a concatenated string of any 2 subplots (no matter how unrelated they are) and on the basis of the following parameters 

1. top_k : Regulates the repetition (Until 'n' words, the context of the sentence will be the same, after which it will repeat)
2. Temperature : regulates randomness - greater the temp, greater the randomness 
3. length 
4. punctuation
5. vocabulary
6. syntactic style 

It will you an extention of the plot 

Consider the following Example - 

Plot 1 - Jack,A poor farmer was walking home one stormy night. 

Plot 2 - Jill,A young girl was swimming in the clear stream in broad daylight.

INPUT - jack a poor farmer was walking home one stormy night and jill a young girl was swimmming in the claer stream in broad daylight.
Features - 
1. Base Character - Jack , Jill
2. Attribute - Poor, Young 
3. Verb - Walking, Swimming 
4. Setting - Stormy night, Broad Daylight


# OUTPUT 
# On the basis of different stress points
we suggest different plot points for the 2 unrelated plots that are given to us.  

Sample Runs - 

![f2](https://user-images.githubusercontent.com/31439716/54006305-c947f180-4182-11e9-96f3-46f646cbfb38.jpeg)
![f1](https://user-images.githubusercontent.com/31439716/54006136-17a8c080-4182-11e9-86b8-3f16ca0ca159.jpeg)
![whatsapp image 2019-03-08 at 09 10 28](https://user-images.githubusercontent.com/31439716/54006228-71a98600-4182-11e9-8a08-ebdc123b9059.jpeg)



# How do we carry out the field extraction - 

As of now : OpenAI GPT-2 construct is such that in the input text depending upon : 

1. Cases (Upper Case ,Lower case)
2. Punctuations (,;:.!)
3. Connectors (and, or, between )

are being used to identify the key element in a seed sentence : Slightly intuitive process - 
![f3](https://user-images.githubusercontent.com/31439716/54007517-39a54180-4188-11e9-8deb-f5b6c4c251f6.jpeg)



So we are modifying the seed text' format each time we wish to give stress on a particular element of a sentence. 
# OPTION 2 
Core Feauture : Use of Style Tranfer to create the seed text and then apply GPT-2 to predict the the extention of the plot 

Give us a concatenated string of any 2 subplots (no matter how unrelated they are) - 

1. We apply content + style tranfer on them to achieve an intermediate text 
2. Then that resultant text is used as the input (seed) for the GPT-2 analysis. 


# Scalability : 
1. Can be applied to any Image Model as well : Style Transfer has been originally applied to images as well.
# style tranfered seed image - and then have it predict an extention to even that plot. 

2. Movies subtitles files can be fed into the script and on that basis -- extention plot. 
Live Example - Tortiose and Hare story part 2 
