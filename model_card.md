# 🎧 Model Card: Music Recommender Simulation

## 1. Model Name  

Give your model a short, descriptive name.  
Example: **VibeFinder 1.0**  

---

## 2. Intended Use  

Describe what your recommender is designed to do and who it is for. 

Prompts:  

- What kind of recommendations does it generate  
- What assumptions does it make about the user  
- Is this for real users or classroom exploration  

---

## 3. How the Model Works  

Explain your scoring approach in simple language.  

Prompts:  

- What features of each song are used (genre, energy, mood, etc.)  
- What user preferences are considered  
- How does the model turn those into a score  
- What changes did you make from the starter logic  

Avoid code here. Pretend you are explaining the idea to a friend who does not program.

---

## 4. Data  

Describe the dataset the model uses.  

Prompts:  

- How many songs are in the catalog  
- What genres or moods are represented  
- Did you add or remove data  
- Are there parts of musical taste missing in the dataset  

---

## 5. Strengths  

Where does your system seem to work well  

Prompts:  

- User types for which it gives reasonable results  
- Any patterns you think your scoring captures correctly  
- Cases where the recommendations matched your intuition  

---

## 6. Limitations and Bias 

This recommender may create a filter bubble because genre receives the largest weight, so songs outside the user's preferred genre can be overlooked even when their mood and energy are similar. The system also uses a small catalog of only 20 songs, and some genres have more examples than others, which can make recommendations less balanced. Its scoring logic only considers genre, mood, and energy, even though the dataset also includes tempo, valence, danceability, and acousticness. As a result, users with more complex or changing musical tastes may receive overly narrow recommendations.
---

## 7. Evaluation  

I tested the recommender using three different user profiles: High-Energy Pop, Chill Lofi, and Deep Intense Rock. For each profile, I checked whether the top recommendations matched the user's preferred genre, mood, and energy level.

The results generally matched my expectations. The High-Energy Pop profile returned upbeat pop songs, the Chill Lofi profile recommended calmer low-energy tracks, and the Deep Intense Rock profile ranked rock songs with high energy at the top. I also tested changing the scoring weights by increasing the importance of energy and reducing the importance of genre. This caused songs with similar energy levels to move higher in the rankings, showing that the recommender responds appropriately when the scoring logic changes.

One interesting observation was that songs like "Gym Hero" appeared in multiple recommendation lists because their energy level closely matched several user profiles, even when the genre was not a perfect match.

Comparing High-Energy Pop and Chill Lofi, the recommendations changed from upbeat, energetic pop songs to calmer, low-energy tracks. This makes sense because the preferred genre, mood, and target energy were very different.

Comparing High-Energy Pop and Deep Intense Rock, both profiles received high-energy songs, but the rock profile prioritized rock songs while the pop profile prioritized pop songs because genre has the highest weight in the scoring system.

Comparing Chill Lofi and Deep Intense Rock, the recommendations were almost completely different. The Chill Lofi profile favored relaxing, low-energy songs, while the Deep Intense Rock profile favored intense, high-energy rock tracks, showing that the recommender responds appropriately to different user preferences.
---

## 8. Future Work  

Ideas for how you would improve the model next.  

Prompts:  

- Additional features or preferences  
- Better ways to explain recommendations  
- Improving diversity among the top results  
- Handling more complex user tastes  

---

## 9. Personal Reflection  

A few sentences about your experience.  

Prompts:  

- What you learned about recommender systems  
- Something unexpected or interesting you discovered  
- How this changed the way you think about music recommendation apps  
