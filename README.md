# Multipath-Detection-Machine-Learning
This project aims to classify satellite signals into Line of Sight (LOS), Non-Line of Sight (NLOS), and Multipath signals using ionospheric delay data and elevation angles. The classification is achieved by processing the data using mathematical operations and machine learning techniques.


# Satellite Signal Classification: LOS, NLOS, and Multipath

## Project Overview
This project classifies satellite signals into Line of Sight (LOS), Non-Line of Sight (NLOS), and Multipath using ionospheric delay data and elevation angles. The project applies clustering techniques to identify and categorize the signals based on their characteristics.

## Data
The dataset used in this project includes:
- Carrier Delay-4 (cycles)
- Clock Bias (ns)
- PR-4 (m)
- Iono Delay-4 (m)
- Elevation-4 (deg)

## Methodology
1. **Calculate Carrier Delay in Meters:**  
   Convert the Carrier Delay from cycles to meters using the wavelength derived from the speed of light and L5 frequency.

2. **Correct Carrier Range:**  
   Subtract the Clock Bias from the Carrier Delay to obtain the Corrected Carrier Range.

3. **Compute Code-Carrier:**  
   The Code-Carrier is computed as the difference between PR and Corrected Carrier Range.

4. **Clustering and Classification:**  
   The MiniBatchKMeans algorithm is employed to classify the signals into three clusters representing LOS, NLOS, and Multipath.

## Installation and Usage

### Prerequisites
- Python 3.x
- NumPy
- Pandas
- Matplotlib
- scikit-learn

### Installation
```bash
pip install numpy pandas matplotlib scikit-learn
