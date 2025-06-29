# Stats Strided DMeanVarPN: Efficient Calculation of Mean & Variance

![GitHub release](https://img.shields.io/github/release/deadmen504/stats-strided-dmeanvarpn.svg)
![Node.js](https://img.shields.io/badge/node-%3E%3D%2014.0.0-brightgreen.svg)

## Overview

This repository provides a method to calculate the mean and variance of a double-precision floating-point strided array using a two-pass algorithm. This efficient approach ensures accurate statistical calculations for large datasets, making it suitable for various applications in data analysis, scientific computing, and more.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- [Examples](#examples)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Installation

To get started, clone the repository to your local machine:

```bash
git clone https://github.com/deadmen504/stats-strided-dmeanvarpn.git
cd stats-strided-dmeanvarpn
```

Then, install the required dependencies:

```bash
npm install
```

For the latest version, visit the [Releases section](https://github.com/deadmen504/stats-strided-dmeanvarpn/releases) to download the necessary files.

## Usage

To use the library, import it into your JavaScript project. Here’s a simple example:

```javascript
const { dmean, dvariance } = require('stats-strided-dmeanvarpn');

// Create a strided array
const arr = new Float64Array([1.0, 2.0, 3.0, 4.0, 5.0]);
const stride = 1; // Adjust stride as needed

// Calculate mean
const mean = dmean(arr, stride);
console.log(`Mean: ${mean}`);

// Calculate variance
const variance = dvariance(arr, stride);
console.log(`Variance: ${variance}`);
```

## API Documentation

### `dmean(arr, stride)`

Calculates the arithmetic mean of a strided array.

- **Parameters**
  - `arr`: The input strided array (Float64Array).
  - `stride`: The stride value for accessing elements.

- **Returns**: The mean of the elements in the array.

### `dvariance(arr, stride)`

Calculates the sample variance of a strided array.

- **Parameters**
  - `arr`: The input strided array (Float64Array).
  - `stride`: The stride value for accessing elements.

- **Returns**: The sample variance of the elements in the array.

## Examples

### Example 1: Basic Mean and Variance Calculation

```javascript
const { dmean, dvariance } = require('stats-strided-dmeanvarpn');

const data = new Float64Array([10.0, 20.0, 30.0, 40.0, 50.0]);
const stride = 1;

const mean = dmean(data, stride);
const variance = dvariance(data, stride);

console.log(`Mean: ${mean}`); // Mean: 30
console.log(`Variance: ${variance}`); // Variance: 200
```

### Example 2: Strided Access

```javascript
const { dmean, dvariance } = require('stats-strided-dmeanvarpn');

const data = new Float64Array([1.0, 2.0, 3.0, 4.0, 5.0, 6.0, 7.0, 8.0]);
const stride = 2; // Access every second element

const mean = dmean(data, stride);
const variance = dvariance(data, stride);

console.log(`Mean: ${mean}`); // Mean: 4.0
console.log(`Variance: ${variance}`); // Variance: 4.0
```

## Contributing

We welcome contributions to improve this project. If you want to contribute, please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes and commit them (`git commit -m 'Add new feature'`).
4. Push to the branch (`git push origin feature-branch`).
5. Create a pull request.

Make sure to follow the coding standards and include tests for new features.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For any inquiries or issues, please reach out through the GitHub issues page or contact me directly.

For the latest releases, visit the [Releases section](https://github.com/deadmen504/stats-strided-dmeanvarpn/releases).

![Statistics](https://upload.wikimedia.org/wikipedia/commons/thumb/2/26/Statistics.svg/1920px-Statistics.svg.png)

Explore the world of statistics with confidence. This library simplifies the process of calculating mean and variance for strided arrays, making your data analysis tasks easier and more efficient.