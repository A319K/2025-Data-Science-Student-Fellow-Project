Bucknell Soccer Prediction System
A machine learning-based prediction model for NCAA soccer match outcomes and tournament qualification. This project implements and compares Random Forest, Gradient Boosting, and Logistic Regression models to forecast game results with 70% cross-validated accuracy. Features include comprehensive data pipeline with PDF match report extraction, advanced feature engineering with 30+ performance metrics, and Excel-exportable formulas for practical team use.
Overview
This project aims to predict the outcomes of Bucknell University Women's Soccer Team matches and their tournament qualification potential using historical data and advanced analytics. The system extracts data from match reports, processes it, and uses machine learning algorithms to generate predictions with probability distributions.
Features

Data extraction from PDF match reports
Advanced feature engineering (30+ performance metrics)
Time-series cross-validation to ensure chronological prediction integrity
Multiple ML models (Random Forest, Gradient Boosting, Logistic Regression)
Excel-exportable predictive formulas
Detailed probability distributions for match outcomes
Head-to-head team analysis
Formulas for calculating win, draw, and loss probabilities

Setup

Create a virtual environment:
python -m venv sklearn-env

Activate the environment:

Windows: sklearn-env\Scripts\activate
Mac/Linux: source sklearn-env/bin/activate


Install dependencies:
pip install -r requirements.txt

Ensure you have the appropriate data files (PDFs of match reports) in the project directory

Usage

Run the PDF extraction script to process match reports:
python pdfExtractor.py

Run the main prediction notebook:
jupyter notebook PatriotLeaguePredictor12.ipynb

For generating Excel formulas and predictions, execute all cells in the notebook

File Descriptions
Core Files

PatriotLeaguePredictor12.ipynb: Main Jupyter notebook containing all the modeling, prediction logic, feature engineering, and Excel formula generation. This is the primary file where the machine learning models are trained and evaluated.
pdfExtractor.py: Script that extracts match statistics from PDF format match reports. Processes data like shots, goals, saves, and other metrics for each game.
2023_2024patriot_league_match_data.xlsx: Excel file containing all processed match data from the Patriot League. Serves as the primary dataset for model training.
patriotleage_stats.xlsx: Generated output file containing team statistics including wins, losses, goals, and various derived metrics.
patriot_league_h2h_statistics.xlsx: Generated output file containing head-to-head statistics between teams, used for advanced feature engineering.
requirements.txt: Lists all Python dependencies required to run the project.
.gitignore: Specifies intentionally untracked files that Git should ignore.

Support Files

match_data2023.xlsx: Historical match data from the 2023 season used for training and validation.
2023.pdf: Example PDF match report file that's processed by the pdfExtractor.py script.
patriot_league_match_reports.py: Helper module for identifying and categorizing match reports.

Results
The models achieve approximately 70% cross-validated accuracy in predicting match outcomes. The Gradient Boosting model slightly outperforms Random Forest (70.0% vs 69.3%).
Key features that influence predictions include:

Head-to-head points per game (H2H Home PPG)
Head-to-head win rate (H2H Home Win Rate)
Attack vs. Defense ratios
Recent team form

Contributing
Contributions are welcome. Please feel free to submit a Pull Request.
License
This project is licensed under the MIT License - see the LICENSE file for details.
