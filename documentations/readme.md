# Project Reflections and Review

## Personal Reflection

Working on the Spam Classifier Analysis Project has been a valuable learning experience that deepened my understanding of machine learning, natural language processing, and cybersecurity. Starting from a simple concept — teaching a computer to distinguish between ham and spam messages — I gained hands-on experience with the full machine learning pipeline: data preparation, feature extraction, model training, and evaluation.

One of the most important lessons I learned is that machine learning is not just about writing code. It requires careful consideration of how data is structured, how models are evaluated, and how results are interpreted. For example, achieving 100% accuracy on a small test set does not necessarily mean the model is perfect — it may simply mean the test was too limited to reveal weaknesses. This taught me to think critically about metrics and not to rely on a single number when assessing model performance.

## What I Learned

- **Data Preparation Matters:** The quality and balance of the dataset directly affect model performance. Using stratified sampling ensured that both ham and spam classes were evenly represented in training and testing sets.
- **Vectorisation is Key:** Converting raw text into numerical features using CountVectorizer was a critical step. Without proper vectorisation, the algorithm cannot process language data.
- **Naive Bayes is Effective for Text:** The MultinomialNB algorithm proved to be a simple yet powerful tool for text classification, even with a small dataset.
- **Test Split Size Affects Results:** Testing with different split sizes (0.1, 0.2, 0.3, 0.4) showed that larger test sets provide more reliable accuracy estimates, while very small splits can give misleadingly perfect scores.

## Project Review

### Strengths

- The project follows a clear and logical pipeline from data loading to model evaluation
- The notebook is well-commented and easy to follow, making it accessible to beginners
- Multiple test split sizes were explored, providing a more complete picture of model behaviour
- The CIA Triad analysis added a cybersecurity perspective that goes beyond typical machine learning projects

### Areas for Improvement

- **Larger Dataset:** The current dataset contains only 30 messages. Using a real-world dataset (e.g., the SMS Spam Collection from UCI or Kaggle) would significantly improve model reliability and generalisation.
- **Advanced Vectorisation:** TF-IDF vectorisation could be explored as an alternative to simple word counting to better weight important terms.
- **Additional Models:** Comparing Naive Bayes with other algorithms such as Logistic Regression, SVM, or Random Forest would provide deeper insights into which approach works best for spam detection.
- **Real-Time Deployment:** Deploying the model as a web service or API would make it practically useful beyond a notebook environment.
- **Confusion Matrix:** Adding a confusion matrix visualisation would make it easier to see exactly where the model makes errors.

## Conclusion

This project has given me a solid foundation in building and evaluating a text classifier. It demonstrated that even a simple model can achieve meaningful results when the pipeline is well-structured. Moving forward, I plan to expand the dataset, experiment with more advanced techniques, and explore deployment options to turn this learning exercise into a functional application.
