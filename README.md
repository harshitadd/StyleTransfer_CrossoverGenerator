# Nested-Style-Transfer-
This project uses style transfer NLP to create a crossover between 2 core plots and then uses Open AI GPT-2  (117M ) to predict the extension plot of the given crossover data.  

The given Network has 12 layers in comparison to the more diverse 48 layer 1.5MB dataset which has not been made public as yet. 


What we are doing ? 

Give us a concatenated string of any 2 subplots (no matter how unrelated they are) and on the basis of the following parameters 1. top_k : Regulates the repetition (Until 'n' words, the context of the sentence will be the same, after which it will repeat)
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

