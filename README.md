## EEG MOTOR IMAGERY SIGNALS CLASSIFICATION VIA SCOUT ESI & CNN

**Overall Framework**:

<div>
    <div style="text-align:center">
    <img width=100%device-width src="https://user-images.githubusercontent.com/31528604/200832194-ea4198f4-e732-436c-bdec-6e454341c442.png" alt="Project1">
</div>

**Proposed CNNs Architecture**:

<div>
    <div style="text-align:center">
    <img width=60%device-width src="https://user-images.githubusercontent.com/31528604/200834151-647319e6-9f6c-428b-b763-36d8859acab9.png" alt="Project1">
</div>

---

### Installation and Usage

1. Python file: PhysioNet_MI_Dataset/MIND_Get_EDF.py

    --- download all the EEG Motor Movement/Imagery Dataset .edf files from [here](https://archive.physionet.org/pn4/eegmmidb/)!

    ```
    (Under Any Python Environment) $ python MIND_Get_EDF.py
    ```

2. Python file: Read_Raw_Data_Save_Into_Matlab_Files.py

    --- Read the edf Raw data of different channels and save them into matlab .m files

    --- At this stage, the Python file must be processed under a Python 2 environment (I recommend to use Python 2.7 version).

    ```
    (Under Python 2.7 Environment) $ python Read_Raw_Data_Save_Into_Matlab_Files.py
    ```

3. Matlab file: Saved_Matlab_Data/Preprocessing_Raw_Data.m

    --- Pre-process the dataset (Data Normalization mainly) and save matlab .m files into Excel .xlsx Files

4. Python file: MI_Proposed_CNNs_Architecture.py

    --- the proposed CNNs architecture 

    --- based on TensorFlow 1.12.0 with CUDA 9.0 or TensorFlow 1.13.1 with CUDA 10.0

    --- The trained results are saved in the Tensorboard

    --- Open the Tensorboard and save the results into Excel .csv files

    --- Draw the graphs using Matlab or Origin

    ```
    (Under Python 3.6 Environment) $ python MI_Proposed_CNNs_Architecture.py
    ```

### Structure of the code
At the root of the project, you will see:

```text
├── PhysioNet_MI_Dataset
|  └── MIND_Get_EDF.py
├── Read_Raw_Data_Save_Into_Matlab_Files.py
├── Saved_Matlab_Data
|  └── Preprocessing_Raw_Data.m
├── MI_Proposed_CNNs_Architecture.py
├── electrode_positions.txt
```