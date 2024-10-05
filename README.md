![CINEsage (1)](https://github.com/user-attachments/assets/46d9b08b-44e9-46a1-aa25-9c8de75aa09a)
________________________________________________________________________________________________
# Personalized Movie Recommendation System

## Description
CineSage is a personalized movie recommendation system designed to help users discover films tailored to their preferences. By leveraging machine learning techniques, this project analyzes user data and movie features to provide accurate recommendations, enhancing the movie-watching experience.

## Installation Instructions
1. Clone the repository:
```bash
git clone https://github.com/yourusername/CineSage.git  
cd CineSage
```
2. Install the required libraries:
```bash
pip install numpy pandas scikit-learn
```
## Usage Examples
Here are some examples of how to use the CineSage recommendation system: call the function `recommend_10_similar_movies`
```python
def recommend_10_similar_movies(movie_name):
    '''
    This function recommends 10 similar movies to the given movie_name.
    movie_name (str): name of the movie for which similar movies are to be recommended
    Returns:
    list_: list of 10 similar movies to the given movie_name
    '''
    # finding index of given movie_name
    index = df[df['title'] == movie_name].index[0]
    # finding top 10 similar movies
    distances = sorted(list(enumerate(similarity_scores[index])), key = lambda x: x[1], reverse = True)[1:11]
    for i,_ in distances:
        print(df['title'][i]) # printing the top 10 similar movies
```

## Project Structure

1.Data Preprocessing & Cleaning 

```python
def extract_name(array):
    '''
    This function extracts the name of genres and keywords from the array. Created for genres and keywords.
    Returns:
    list_: list of genres in the array
    '''
    list_ = [value['name'] for value in ast.literal_eval(array)]
    return list_
```

2. Vectorization

```python
from sklearn.feature_extraction.text import CountVectorizer

# creating object of CountVectorizer
count_vectorizer = CountVectorizer(max_features = 5000, # only keeping top 5000 vectors
                                   stop_words = 'english') #  removing stop words
```

## Contribution Guidelines
Contributions are welcome! If you have suggestions for improvements or new features, please fork the repository and submit a pull request.

## License Information
This project does not have a specific license.

## Future Work

Future enhancements for CineSage may include:

1. Implementing a more sophisticated recommendation algorithm (e.g., collaborative filtering).
2. Adding a user interface for easier interaction.
3. Deploying the model as a web application for real-time recommendations.

## Contact:
For any questions or feedback, feel free to contact me at akashambure123@gmail.com

Happy Coding! 🚀











