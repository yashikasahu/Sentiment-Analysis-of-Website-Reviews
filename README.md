<h1>1. Data Collection</h1>

I collected a dataset of website reviews (Flipkart product reviews in this demo).
Below is the screenshot of raw extracted reviews:

<img width="1329" height="630" alt="Screenshot 2025-11-30 142712" src="https://github.com/user-attachments/assets/e9561d32-0009-4ec6-bc47-38c58ea58c8c" />


<h1>2. Sentiment Analysis Using VADER</h1>

The reviews were processed using NLTK’s VADER sentiment analyzer.
The model is especially good at understanding:

Emoji

Slang

Social media language

Exclamation emphasis

Punctuation-based sentiment

Code Screenshot
<img width="1392" height="697" alt="Screenshot 2025-11-30 142809" src="https://github.com/user-attachments/assets/5581171a-0181-4bef-91a1-45c44cba6eb7" />


<h1>Code Logic Summary</h1>
*1. Load dataset*

Import reviews from CSV

2. Apply VADER sentiment model

*Polarity scores*

Compound score thresholding

compound ≥ 0.05 → POSITIVE

compound ≤ –0.05 → NEGATIVE

otherwise → NEUTRAL

*3. Save output*

A new CSV with predicted sentiment for each review

<h1>3. Crux (Overall Review Summary)</h1>

To generate a human-readable summary, I used TextBlob polarity and keyword extraction.

Crux Code Screenshot
<img width="1355" height="667" alt="Screenshot 2025-11-30 142756" src="https://github.com/user-attachments/assets/011f4af8-6d46-4e87-8be1-70196add61f6" />


<h1>Output</h1>
Most users praise the iPhone 16 Pro for its awesome, great, overall performance.  
A few reviews were neutral or mixed in sentiment.

<h1>4. Final Sentiment Output (Excel)</h1>

After processing, the final dataset includes:

Original review

Predicted sentiment label

Preview
<img width="1421" height="669" alt="Screenshot 2025-11-30 143231" src="https://github.com/user-attachments/assets/1a6a1be6-a434-487b-9fca-e94fb6276de7" />



Project Files
Sentiment-Analysis-of-Website-Reviews/
│── data/
│   ├── flipkart_review.csv
│   ├── flipkart_reviews_with_sentiment.csv
│
│── visuals/
│   ├── raw_reviews.png
│   ├── vader_code.png
│   ├── crux_code.png
│   ├── final_output.png
│
│── src/
│   ├── vader_sentiment.py
│   ├── crux_generator.py
│
│── README.md

<h1>Installation & Usage</h1>
*1. Clone the Repository*
git clone https://github.com/your-username/Sentiment-Analysis-of-Website-Reviews.git
cd Sentiment-Analysis-of-Website-Reviews

*2. Install Dependencies*
pip install nltk pandas textblob

*3. Run VADER Sentiment Script*
python src/vader_sentiment.py

4*. Generate Crux Summary*
python src/crux_generator.py

<h1>Results</h1>
Sentiment Ratio (Approx.)

Positive: 80–90%

Neutral: 5–10%

Negative: 2–5%

<h1>Summary</h1>

Most customers express high satisfaction, especially around performance, camera, colors, and overall experience.
Only a small percentage of reviews mention minor concerns.

Future Enhancements

Include ML models (SVM, Logistic Regression)

Add word clouds

Build a Streamlit UI for real-time sentiment checking

Deploy via Flask API

*License*

MIT License
