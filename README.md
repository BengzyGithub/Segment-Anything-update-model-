# Grounding Dino, SAM, and Speech-to-Text Integration

This repository combines three powerful functionalities: Grounding Dino for image grounding, SAM for segmentation, and Speech-to-Text for audio transcription. This integration allows for a comprehensive analysis of images based on natural language descriptions and audio inputs.The main goal is to optimize SAM to use speech and text box for segmenting.

## Setup

Before running the code, ensure you have the required dependencies installed. You can install them using the following command:

```bash
pip install torch opencv-python numpy matplotlib transformers google-cloud-speech
```

Additionally, make sure to set up the necessary API credentials for Speech-to-Text by providing the path to your JSON file:

```python
# Import API credentials for Speech-to-Text
os.environ["GOOGLE_APPLICATION_CREDENTIALS"] = r"C:\Users\someone\Downloads\GroundingDINO-main\GroundingDINO-main\API_Key_for_speech_to_text.json" //this is an example
```

## Grounding Dino Model

The Grounding Dino model is used for image grounding. Pretrained weights and configuration files for the model are specified as follows:

- Grounding Dino Model Weights: `C:\Users\someone\Downloads\GroundingDINO-main\GroundingDINO-main\groundingdino_swint_ogc.pth`
- Grounding Dino Model Config: `C:\Users\someone\Downloads\GroundingDINO-main\GroundingDINO-main\config\GroundingDINO_SwinT_OGC.py`

## SAM Model

The SAM model is used for image segmentation. Pretrained weights and configuration files for SAM are specified as follows:

- SAM Model Weights: `C:\Users\someone\Downloads\segment-anything-main\segment-anything-main\sam_vit_h_4b8939.pth`
- SAM Model Config: `C:\Users\someone\Downloads\segment-anything-main\segment-anything-main\demo\configs\webpack\prod.js`

## Speech-to-Text

The Speech-to-Text functionality uses the Google Cloud Speech API. Make sure to set up your API credentials as mentioned in the setup section.

## Usage

1. Set the paths for Grounding Dino and SAM model weights and configuration files.
2. Specify the image path for processing.
3. Provide a list of trained datasets or an empty string for Speech-to-Text input.
4. Run the code to transcribe audio, perform image grounding, and visualize the results.

**Example Usage:**

```python
python grounding_dino_sam_speech.py
```

The code will transcribe audio, use Grounding Dino to associate descriptions with regions in the image, and then use SAM for segmentation. The annotated images will be displayed with bounding boxes and segmentation masks.

## Contributors

- Alphonse <alphonselemnsernyuy@gmail.com>
- Jichao <fangdxc@gmail.com>
- Matt Kiesel <mkaisel01@gmail.com>

Feel free to contribute, report issues, or reach out for any questions related to this integrated project.
