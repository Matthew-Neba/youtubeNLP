# YouTube Comments Sentiment Analysis Application

This Django web app analyzes YouTube comments to track how viewers feel about a video. It uses both traditional machine learning and modern NLP models to show sentiment trends over time, helping understand audience reactions.

## Features

- **YouTube Video Selection**: Users can select a YouTube video URL to analze its comments.
- **Sentiment Analysis Methods**: Offers two methods for sentiment analysis: VADER (a lexicon-based sentiment analysis tool) and a machine learning approach using Hugging Face's Transformers library.
- **Visualization**: Generates charts displaying the percentages of positive,negative and neutral comments for each month/year pair that returned by the youtube api
- **Environment Variables**: Utilizes environment variables for configuration, including the YouTube API key and other settings.

## Setup

To run this application locally, follow these steps:

1. **Clone the Repository**:
   ```
   git clone https://github.com/MastrMatt/youtubeNLP.git
   cd youtubeNLP
   ```

2. **Install Dependencies**:
   Ensure Python 3.x is installed. Then, install the required packages listed in `requirements.txt`:
   ```
   pip install -r requirements.txt
   ```

3. **Configure Environment Variables**:
   Copy `.env.example` to `.env` and fill in the missing values, such as your YouTube API key.

4. **Run Migrations**:
   Apply database migrations to set up the database schema:
   ```
   python manage.py migrate
   ```

5. **Start the Development Server**:
   Run the development server:
   ```
   python manage.py runserver
   ```

6. **Access the Application**:
   Open your web browser and navigate to `http://127.0.0.1:8000`.

## Usage

Upon accessing the application, users will see a form where they can enter a YouTube video URL. After submitting the form, the application will display the sentiment analysis results, including charts showing the distribution of sentiments across the selected video's comments. NOTE: the amount of comments fetched for each year/month pair is not constant, there may be some months with more comments retrieved than others.

## Future Considerations

1. Incorporate the likes of each comment into the overall sentiment analysis

2. Provide a graphical interface to view the maximum and minimum comments

3. Implement batch processing for the Hugging face analysis to attempt to speed up

## Author
Matthew Neba / [@MastrMatt](https://github.com/MastrMatt)

## License
This project is licensed under the [MIT License](LICENSE).

## Contributing

Contributions to this project are welcome Please submit pull requests or open issues to discuss potential improvements or report bugs.



---



