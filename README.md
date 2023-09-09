# Retail GeoPlatform
## About
This repository was created as a part of the AI Talent Hackathon. During this hackathon, the problem of analyzing reviews of X5 retail stores was solving. As a solution, we have proposed the *GeoPlatform* - a tool for analyzing reviews both for one store and for a set of stores in a district/city.

## Data collection
The data was collected from online map services such as Yandex Maps and 2GIS. The result of the data collection was more than 5,000 reviews on 55 stores of 5 different retailers. All the collected data as well as the python scripts for it collection can be find in the `data-parsing` root.

## Model selection and fitting
In the ML part of the project we faced with hierarchical text classification by store parameter and it's sentiment.

The first-level model classifies the key storage parameter. The second one - sentiment of this parameter. Due to the missing markup, the zero-shot text classification approach was chosen.

Two models from Hugging Face were considered:
- zero-shot-classify-SSTuning-XLMR, cause it's fast and easy to integrate;
- multilingual-e5-large-xnli-english, cause it's powerful.



## Results demonstration
- pydeck layers for build map and plot points
- streamlit for deploy app
Try our result here: https://geoplatforma.streamlit.app
