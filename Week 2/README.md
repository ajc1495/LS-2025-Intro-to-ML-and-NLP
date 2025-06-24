# Comparison of word scores between manual TF-IDF, CountVectorizer, and TfidfVectorizer:

- Manual TF-IDF: Calculates scores based on word importance across documents. Rare words (like "satellite", "celestial") get higher scores; common words get lower scores.

- CountVectorizer: Simply counts word frequency. Common words like "the" get high scores even if they’re uninformative.

- TfidfVectorizer: Similar to manual TF-IDF, but includes normalization. It penalizes common words and highlights rare, informative ones.

# Why do scores for common words (like "the") differ significantly between the methods?

-In CountVectorizer, "the" has a high score because it appears frequently.

-In TF-IDF methods (both manual and sklearn), "the" appears in every document, so its IDF is low, reducing its overall importance.

-TF-IDF is designed to highlight unique, distinguishing terms, not just frequent ones.
