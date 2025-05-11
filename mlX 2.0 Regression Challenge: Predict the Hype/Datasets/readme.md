
Dataset Description
Files Provided
train.csv - The training set containing historical music track data with known popularity scores
test.csv - The test set containing music track data without popularity scores (for prediction)
sample_submission.csv - A sample submission file demonstrating the required format
Prediction Target
Your goal is to predict the popularity score of music tracks/albums based on their audio characteristics and metadata. The target variable is:

target: Continuous popularity score (higher values indicate more popular tracks/albums)
Data Columns
Each row represents a single music release with its audio features and derived characteristics.

Track Identification
track_identifier: Official title of the primary track or album
creator_collective: List of credited artists
publication_timestamp: Release date (YYYY-MM-DD format)
album_component_count: Total tracks in the release
Core Audio Features (Tracks 0-2)
For the first three tracks on the release:

composition_label_[0-2]: Track titles
duration_ms_[0-2]: Duration in milliseconds
rhythmic_cohesion_[0-2]: Danceability (0-1)
intensity_index_[0-2]: Energy level (0-1)
harmonic_scale_[0-2]: Musical key (0-11)
tonal_mode_[0-2]: Modality (0=minor, 1=major)
organic_texture_[0-2]: Acousticness (0-1)
beat_frequency_[0-2]: Tempo in BPM
time_signature_[0-2]: Meter (e.g., 3=3/4, 4=4/4)
Derived Audio Metrics
emotional_charge_[0-2]: Valence × Energy product
groove_efficiency_[0-2]: Energy/Danceability ratio
organic_immersion_[0-2]: Acousticness × Duration
duration_consistency: Std dev of track durations
tempo_volatility: BPM range across tracks
key_variety: Unique keys among first 3 tracks
Contextual Features
album_name_length: Character length of track title
artist_count: Number of credited artists
weekday_of_release: Day of week (Monday-Sunday)
season_of_release: Seasonal quarter
lunar_phase: Moon phase at release
Data Format
CSV format with header row
Missing values represented as empty cells or NaN
Continuous features scaled 0-1 unless otherwise noted
Temporal features in ISO 8601 format (YYYY-MM-DD)
Categorical features as strings
Important Notes
Data represents diverse music releases across genres and eras
All audio features are extracted from signal processing algorithms
The target column is only present in training data
Evaluation Metric
Submissions will be evaluated using Root Mean Squared Error (RMSE):
