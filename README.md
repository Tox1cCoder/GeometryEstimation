# GeometryEstimation

### Prerequisite

- Clone this repository. 

    ```bash
    git clone https://github.com/microsoft/MoGe.git
    cd MoGe
    ```

- Make sure that `pytorch` and `torchvision` are installed. Then install the rest of the requirements. 
    
    ```bash
    pip install -r requirements.txt
    ```
    
    It should be very easy to install these requirements. Please check the `requirements.txt` for more details if you have concerns.

### Pretrained model

The ViT-Large model has been uploaded to Hugging Face hub at [Ruicheng/moge-vitl](https://huggingface.co/Ruicheng/moge-vitl). 
You may load the model via `MoGeModel.from_pretrained("Ruicheng/moge-vitl")` without manually downloading.
