# Robust KMeans using L1 Lightweight Coresets

This repository contains the implementation of various coreset construction techniques for clustering large-scale datasets. The main goal is to reduce computational complexity while maintaining the quality of clustering results. The methods implemented include:

- **L1 Lightweight Coresets (Lightweight Coresets Median)**: A novel approach that uses the median of distances between data points for coreset construction, designed to provide a compact and informative subset of the dataset. It significantly outperforms other techniques in terms of error reduction and processing speed in most datasets.
  
- **Weighted Volume Sampling**: A weighted variant of volumetric sampling that incorporates weights into the sampling process to better capture the data distribution, enhancing the clustering quality of the resulting coresets.

- **Weighted Statistical Leverage**: Extends the traditional statistical leverage approach by introducing weights, aiming to improve the representativeness of coresets for clustering large datasets.

- **Existing Models Implemented for Comparison**:
  - **Lightweight Coresets** (Bachem et al., 2018)
  - **Statistical Leverage** (Ismail et al., 2012)
  - **Volumetric Sampling** (Deshpande et al., 2006)

## Datasets

The methods were evaluated on the following datasets:

1. **KDD Dataset**: A subset of the KDD Cup 99 dataset, commonly used for anomaly detection tasks, containing both categorical and continuous features.
   
2. **Face Dataset**: Consists of facial images used primarily for testing clustering algorithms in facial recognition applications.

3. **Synthetic Dataset**: A generated dataset designed to simulate specific statistical distributions, allowing for controlled validation of clustering algorithms.

4. **Worms Dataset**: Contains morphological data of various worm species, utilized in biological and ecological research.

## Results

The methods were tested with data reductions of 30%, 50%, 80%, and 95%. Key results include:

- **L1 Lightweight Coresets** consistently provided the lowest error rates and fastest processing times across all datasets and reduction levels, demonstrating robustness and efficiency.
  
- **Weighted Volume Sampling** and **Weighted Statistical Leverage** did not show significant performance gains over traditional sampling methods, indicating that while theoretically promising, their practical advantages were limited in the tested scenarios.

- The simplicity of uniform and norm-based sampling occasionally outperformed more complex methods, suggesting that elaborate sampling techniques may not always yield superior results.

## Contributions

Contributions to improve the implementations or extend the study are welcome. Please feel free to fork the repository, submit issues, or make pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
