
## <div align="justify"> Title - Automated Damage Detection and Mapping in Historical Artifacts Using Deep Learning </div>

##  Introduction

<div align="justify">
The preservation of cultural heritage demands precise and scalable methods for monitoring the structural integrity of historical artifacts. Traditional manual inspection techniques are often labor-intensive, subjective, and limited in their ability to detect subtle or early stage damage. This project presents an automated deep learning framework for artifact damage detection and mapping, designed to support conservation efforts with objectivity and efficiency. By leveraging a convolutional autoencoder, the system reconstructs artifact images and localizes anomalies through reconstruction error analysis. Advanced postprocessing methods including heatmap visualization, skeletonization, and bounding box extraction enable the identification of cracks, scratches, and surface deterioration. The framework outputs interpretable results in the form of overlays, binary masks, and quantitative severity scores, offering both visual and analytical insights. Additionally, a Gradio-powered web interface provides an accessible and interactive platform, allowing conservation professionals and researchers to upload artifact images, analyze damage patterns, and prioritize restoration tasks effectively.
</div>

##  Structure 

├── data/ ├── damaged_images/ # Raw input artifact images        

├── image_mapping_code.ipynb  # Main Jupyter Notebook (training + evaluation + UI)

├── samples # Example inputs and outputs for quick reference

├── requirement.txt # Required Python libraries for the project

## Setup Instructions

1. Clone the Repository

    Terminal - Command - Git Clone 

    https://github.com/Praisingh-Codes/Image-Mapping.git

    cd Image-Mapping


2. Create Virtual Environment

   Terminal - Command
   
   python -m venv venv

   (On Linux/Mac: source venv/bin/activate)
   
   (On Windows: venv\Scripts\activate)


3. Install Dependencies
   
   Terminal - Command
    
   pip install -r requirements.txt


4. Prepare Dataset

   Place your artifact images inside the data/damaged_images/ folder.

   dataset/

      ├── damaged_images/
            ├── artifact_1.jpg
            ├── artifact_2.jpg
            ...

   
5. Run the Jupyter Notebook
   
   Launch the notebook environment:
   
   jupyter notebook

   Open and execute all cells in image_mapping_code.ipynb.
   
   - Trains the autoencoder.

   - Saves models in models/.

   - Generates heatmaps, overlays, and CSV summaries in outputs/.


6. Use the Gradio Interface
   
   Run the final cell in the notebook to launch the Gradio app:
   
   - Upload artifact images for analysis.

   - System will return:

     - Original image

     - Autoencoder reconstruction

     - Heatmap of anomalies

     - Damage overlay visualization

     - Binary mask of detected regions

     - Percent damaged area + severity classification


## Conclusion

<div align="justify">
This project establishes a comprehensive pipeline for non-invasive damage monitoring of historical artifacts. By integrating deep learning–based anomaly detection with advanced image postprocessing techniques, the framework delivers precise visual and quantitative assessments of artifact condition. The inclusion of a Gradio-powered web interface enhances accessibility, enabling experts to interactively analyze damage, interpret results, and prioritize conservation efforts. Overall, this system highlights the transformative role of artificial intelligence in cultural heritage preservation, offering a scalable, accurate, and practical solution for artifact condition assessment and restoration planning.
</div>
