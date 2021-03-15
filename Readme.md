# Bigram Model Language Identifier
#### By: Benjamin Kulis (bkulis2)
### Problem Solved
My program solves the problem of idenitfying what language that a sentence is written in. There are 3 programs that idenitfy the language in different ways. The first is the `letterLangId.ipynb` program, which uses a letter bigram model for English, French, and Italian and determines which language the sentence is in. The second is the `wordLangId.ipynb` program, which uses a word bigram model for the 3 langauges and decides the the most probable language the sentence is written in. The last is the `wordLangId2.ipynb` program which is implemented the same way as the latter program, except it uses the Good-Turing smoothing algorithm, instead of Laplace (or add-one) smoothing (like the previous two models), to account for Out of Vocabulary words, and predict the language of an inputted sentences.

### Program Structure
Each program follows the same strucutre. The first cell parses the training data for said language and the following cell creates the bigram for the respective language. This occurs for all 3 languages. After these 6 cells, the program parses the testing data, to check the accuracy of our bigram model. Now the following cells, apply either Laplace or Good-Turing smoothng and update the bigram probabilites for their respective languages. Then, the program writes its predictions into the respective output file after deciding which language is most probable for a given line. Lastly, the program compares the predictions to the actual languages for each line and calculates the accuracy.

### How To Run the Code
Make sure to use an IDE that can run `.ipynb` files. Choose the type of n-gram language model you want to run by clicking on the respective `.ipynb` file. Click to run all of the cells. Then, you can see the last cell print the prediction accuracy percentage. Additionally, you can see the predictions the model made for each line in the `../Data/Output/` folder, in the respectively named file.
