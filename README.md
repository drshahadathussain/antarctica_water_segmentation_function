# Antarctic Ice Shelf Water Segmentation Project 

A MATLAB-based image processing project to analyze climate change effects by quantifying melt water in Antarctic ice shelf satellite images from 2018 and 2020.

# 📋 Overview

This project compares two satellite images of the same Antarctic region taken two years apart (January 2018 and January 2020). Using MATLAB's Image Processing Toolbox, we segment water areas in both images to calculate the change in visible water, providing quantitative evidence of ice shelf melting over time.

# 🎯 Learning Objectives

- Segment images using MATLAB's Color Thresholder app
- Experiment with different color spaces (HSV, RGB, Lab, YCbCr) for optimal segmentation
- Generate and refine segmentation functions for robust performance
- Apply morphological operations to clean binary masks
- Quantify and visualize changes between images
  
# 📁 Repository Structure

```
text
antarctic-ice-shelf-analysis/
│
├── README.md                 # Project documentation
├── images/                   # Satellite images directory
│   ├── iceshelf_2018.jpg    # January 2018 image
│   └── iceshelf_2020.jpg    # January 2020 image
├── results/                  # Output directory for masks and figures
└── docs/                     # Additional documentation
```

# 🛠 Requirements

- MATLAB R2019b or later
- Image Processing Toolbox
- Color Thresholder app (included with Image Processing Toolbox)

# 🚀 Getting Started

1. Clone the repository
```
bash
git clone https://github.com/yourusername/antarctic-ice-shelf-analysis.git
```

2. **Add your images** to the `images/` folder
3. **Open MATLAB** and navigate to the project directory
4. **Launch Color Thresholder** to begin segmentation

```
matlab
img = imread('images/iceshelf_2018.jpg');
colorThresholder(img);
```

# 📊 Methodology

**Color Space Exploration**

- Color Space	Application for Water Detection
- **HSV**	Water has distinct Hue range (blue: ~180-240°)
- **RGB**	Water shows higher blue channel values
- **Lab**	Water has negative a* and b* values
- **YCbCr**	Water has specific Cb (blue-difference) values

## Workflow

1. Load satellite image in Color Thresholder
2. Experiment with different color spaces
3. Adjust thresholds to select water regions
4. Export segmentation function
5. Test function on both 2018 and 2020 images
6. Refine thresholds for robust performance
7. Calculate water area in both images
8. Generate change map and statistics

# 🔍 Key Considerations

## Segmentation Challenges

- Water and ice can have similar visual characteristics
- Lighting conditions may differ between images
- Shadows can be mistaken for water
- Glare on water surfaces affects detection

## Tips for Success

- Start with HSV color space (most effective for water/ice separation)
- Test your function on both images throughout development
- Use morphological operations to clean up masks:
  - Remove small noise objects
  - Close small gaps in water regions
  - Fill holes within identified water areas
- Document threshold values that work well

# 📈 Expected Outcomes

The analysis will yield:

- Binary masks showing water vs. ice for both years
- Water coverage percentage for each image
- Absolute and relative change in water area
- Change map visualizing:
  - Water lost (present only in 2018)
  - Water gained (present only in 2020)
  - Persistent water (present in both years)

# 🌍 Scientific Context

In Antarctic climate research:

- Increased melt water indicates rising temperatures
- Melt pond formation precedes ice shelf collapse
- Surface melting contributes to sea level rise
- Multi-year comparisons help establish climate trends

# 🤝 Contributing

Contributions to improve segmentation methods or documentation are welcome. Please:

- Fork the repository
- Create a feature branch
- Submit a pull request

# 📚 References

- [Introduction to Image Processing](https://www.coursera.org/learn/introduction-image-processing/)
- [MATLAB Color Thresholder Documentation](https://www.mathworks.com/help/images/color-thresholder-app.html)
- [NASA Climate Change Research](https://science.nasa.gov/climate-change/)
- [National Snow and Ice Data Center](https://nsidc.org/home)

# 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

# ✏️ Citation

If you use this project in your research, please cite:
```
text

Antarctic Ice Shelf Water Segmentation Project, MATLAB Image Processing,
https://github.com/drshahadathussain/antarctic-ice-shelf-analysis
```
## About the Author

**Dr. Shahadat Hussain**

Researcher in 3D Printing & Materials Science. I use Image Processing to analyze material structures and 3D printing failure modes.

🌐 [www.shahadathussain.com](https://www.shahadathussain.com) | ✍️ [Substack](https://drshahadathussain.substack.com)

# 📧 Contact

For questions or feedback, please open an issue in the GitHub repository.
