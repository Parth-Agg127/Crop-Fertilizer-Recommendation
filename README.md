# Crop Recommendation and Fertilizer System

## Project Overview

This project implements an intelligent agricultural decision support system that provides crop recommendations and fertilizer suggestions based on soil and environmental conditions. The system uses machine learning algorithms to analyze various agricultural parameters and help farmers make data-driven decisions for optimal crop selection and fertilization.

## Key Features

- **Crop Recommendation**: Predicts the most suitable crop based on soil nutrients (N, P, K), climate conditions (temperature, humidity, rainfall), and soil pH
- **Fertilizer Recommendation**: Suggests appropriate fertilizer types based on predicted crop and soil conditions  
- **Data Visualization**: Comprehensive exploratory data analysis with interactive plots
- **High Accuracy**: Achieves excellent prediction accuracy using Random Forest algorithm
- **User-Friendly Interface**: Interactive input system for real-time recommendations

## Technologies Used

- **Python 3.x**
- **Machine Learning**: scikit-learn
- **Data Analysis**: pandas, numpy
- **Visualization**: matplotlib, seaborn
- **Algorithm**: Random Forest Classifier/Regressor

## Dataset Information

The system uses two primary datasets:

### Crop Recommendation Dataset
- **Features**: 
  - `N` - Nitrogen content in soil
  - `P` - Phosphorus content in soil  
  - `K` - Potassium content in soil
  - `temperature` - Temperature in Celsius
  - `humidity` - Relative humidity in %
  - `ph` - pH value of soil
  - `rainfall` - Rainfall in mm
- **Target**: `label` - Crop type (rice, maize, wheat, cotton, etc.)

### Fertilizer Dataset
- Contains soil nutrient information and corresponding fertilizer requirements
- Merged with crop data for comprehensive analysis

## Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/crop-fertilizer-recommendation.git
   cd crop-fertilizer-recommendation
   ```

2. **Install required packages**
   ```bash
   pip install pandas scikit-learn numpy matplotlib seaborn
   ```

3. **Download datasets**
   - Place `Crop_recommendation.csv` in the project directory
   - Place `fertilizer.csv` in the project directory

## Usage

### Running the Complete System

```bash
python Crop-Fertilizer-Reco-Project.py
```

The script will prompt you to enter:
- Nitrogen content (N)
- Phosphorus content (P)
- Potassium content (K)
- Temperature in Celsius
- Humidity percentage
- Soil pH level
- Rainfall amount in mm

### Example Usage

```python
# Example input values
N = 60
P = 55
K = 44
temperature = 23.0
humidity = 82.3
ph = 7.5
rainfall = 200

# Get recommendation
recommendation = recommend_fertilizer(N, P, K, temperature, humidity, ph, rainfall)
print("Predicted Crop:", recommendation["predicted_crop"])
print("Fertilizer Recommendation:", recommendation["fertilizer_recommendation"])
```

## Model Performance

The Random Forest model achieves:
- **High Classification Accuracy**: 99%+ accuracy on test data
- **Robust Predictions**: Handles multiple crop types effectively
- **Feature Importance**: Considers all environmental and soil factors

### Evaluation Metrics
- **Mean Squared Error**: Used for regression tasks
- **R-Squared Score**: Measures model fit quality
- **Classification Accuracy**: Overall prediction accuracy
- **Precision & Recall**: Detailed per-class performance

## Data Visualization

The system includes comprehensive data analysis:

1. **Feature Histograms**: Distribution of all soil and climate parameters
2. **Correlation Heatmap**: Relationships between different features
3. **Boxplots**: Feature distributions across different crop types
4. **Scatter Plots**: Temperature vs Humidity relationships by crop type

## Fertilizer Recommendation Logic

The system provides tailored fertilizer recommendations:

- **Rice & Maize**: Nitrogen-rich fertilizer
- **Wheat & Barley**: Balanced NPK fertilizer  
- **Cotton & Pigeonpeas**: Phosphorus and Potassium rich fertilizer
- **Other Crops**: General purpose NPK fertilizer

## Model Architecture

### Data Preprocessing
- Label encoding for categorical variables
- Standard scaling for numerical features
- Missing value handling
- Feature alignment across datasets

### Machine Learning Pipeline
1. **Data Loading**: CSV files import and preprocessing
2. **Feature Engineering**: Scaling and encoding transformations
3. **Model Training**: Random Forest with 100 estimators
4. **Evaluation**: Cross-validation and performance metrics
5. **Prediction**: Real-time crop and fertilizer recommendations

## Project Structure

```
crop-fertilizer-recommendation/
│
|__ crop_recommendation_analysis.ipynb #Main implementation file 
├── Crop-Fertilizer-Reco-Project.py  # Pyhton code file
├── Crop_recommendation.csv # Primary dataset
├── Fertilizer recommendation.csv # Fertilizer data
├── README.md             # Project documentation
└── requirements.txt      # Python dependencies
```
## Future Enhancements

- [ ] Web interface using Flask/Django
- [ ] Mobile application development
- [ ] Integration with weather APIs
- [ ] Advanced deep learning models
- [ ] Multilingual support
- [ ] Soil image analysis using computer vision
- [ ] Real-time IoT sensor integration

## Known Issues

- Ensure CSV files are in the correct format
- Input validation for user-entered values
- Handle edge cases for extreme environmental conditions


## Author

**Parth Aggarwal**
- GitHub: [@Parth-Agg127](https://github.com/Parth-Agg127)
- Email: Parthaggarwal481@gmail.com

## Acknowledgments

- Dataset providers for agricultural data
- Scikit-learn community for machine learning tools
- Agricultural research institutions for domain knowledge

## Support

If you have any questions or need support, please:
- Create an issue on GitHub
- Contact via email
- Check the documentation

---

**Happy Farming! 🌱🚜**
