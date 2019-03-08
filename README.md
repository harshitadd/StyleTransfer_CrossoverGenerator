# Nested-Style-Transfer-
This project uses style transfer NLP to create a crossover between 2 core plots and then uses Open AI GPT-2  (117M ) to predict the extension plot of the given crossover data.  

The given Network has 12 layers in comparison to the more diverse 48 layer 1.5MB dataset which has not been made public as yet. 


What we are doing ? 

#OPTION 1 - Core feature - Use of GPT-2 to create plots based on different features of the seed video. 

Give us a concatenated string of any 2 subplots (no matter how unrelated they are) and on the basis of the following parameters 
1. top_k : Regulates the repetition (Until 'n' words, the context of the sentence will be the same, after which it will repeat)
2. Temperature : regulates randomness - greater the temp, greater the randomness 
3. length 
4. punctuation
5. vocabulary
6. syntactic style 


Consider the following Example - 
Plot 1 - Jack,A poor farmer was walking home one stormy night. 

Plot 2 - Jill,A young girl was swimming in the clear stream in broad daylight.

Input to Script - jack a poor farmer was walking home one stormy night and jill a young girl was swimmming in the claer stream in broad daylight. 

Features - 
1. Hero - Jack , Jill
2. Attribute - Poor, Young 
3. Verb - Walking, Swimming 
4. Setting - Stormy night, Broad Daylight

Sample Runs - 

![f2](https://user-images.githubusercontent.com/31439716/54006305-c947f180-4182-11e9-96f3-46f646cbfb38.jpeg)
![f1](https://user-images.githubusercontent.com/31439716/54006136-17a8c080-4182-11e9-86b8-3f16ca0ca159.jpeg)
![whatsapp image 2019-03-08 at 09 10 28](https://user-images.githubusercontent.com/31439716/54006228-71a98600-4182-11e9-8a08-ebdc123b9059.jpeg)



















#OPTION 2 - Core Feauture : Use of Style Tranfer to create the seed text and then apply GPT-2 to predict the the extention of the plot 

Give us a concatenated string of any 2 subplots (no matter how unrelated they are) - 

1. We apply content + style tranfer on them to achieve an intermediate text 
2. Then that resultant text is used as the input (seed) for the GPT-2 analysis. 


Sample Runs - 

