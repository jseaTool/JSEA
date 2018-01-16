1. Please configure following “Configuration.txt”;
2. Run JSEA;
3. Upload the directory of source code that need to process.
4. Select preprocessing steps as your demands, and we recommend do all steps;
5. Click “Start Preprocessing”;
6. Open bash and enter “MALLET” directory;
7. Run “mallet-2.0.8/topic-modeling.sh”: 
bash topic-modeling.sh -input_file -topic_number;
#-input_file: the project name, like JHotDraw;
#-topic_number: the number of topics
8. You can use the system via “show” page (The project overview page) and “search” page (JSEA-Search).
9. If you want to adjust the value of parameters during topic modeling, please open "mallet-2.0.8/topic-modeling.sh" and then change the following value:
(1) --num-top-words [NUMBER]:The number of the most trusted words for each topic output after the model is estimated.
(2) --num-iterations [NUMBER]: The number of sampling iterations should be a trade off between the time taken to complete sampling and the quality of the topic model.
(3) --optimize-interval [NUMBER] This option turns on hyperparameter optimization, which allows the model to better fit the data by allowing some topics to be more prominent than others. Optimization every 10 iterations is reasonable.

or add new options:
(1)--optimize-burn-in [NUMBER] The number of iterations before hyperparameter optimization begins. Default is twice the optimize interval.