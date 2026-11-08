# Public release plan — Bachelor's thesis

**Permissions:** Muhammad Nouman confirms that the university, co-author and supervisors have approved sharing the bachelor's thesis and poster. This public repository is for **documentation, selected results and hardware design files only**. **No project source code, model checkpoints or datasets will be uploaded.**

## Uploading to a GitHub folder

GitHub folders can be opened by clicking their name. Navigate to `docs/`, `Hardware-Images/`, or `Hardware_Files/`. Inside that folder, select **Add file → Upload files**, select or drag in the files, then click **Commit changes**. Files will go into the folder you opened.

Do not create an empty folder by typing its name into the “Create new file” field. This creates a file with that name; GitHub needs a file *inside* the folder. These three folders already contain a `README.md` and are ready to receive uploads.

## 1. Approved thesis and poster: `docs/`

- Upload the updated final report named `bachelors_thesis.pdf`.
- Upload the university-approved poster named `thesis_poster.pdf`.
- Important quality check: the newly supplied thesis PDF is titled “Final Year Project Report”, but its certificate of originality still contains the literal placeholder **“Project Title”** on page 3 and its title page contains **“Year”** on page 2. The approval page also uses the alternate project title. Consider correcting these inconsistencies in the source document *if your university allows an amended public copy*; otherwise preserve the official copy and do not misrepresent it.
- After upload, update the main README links from “upload pending” to `[Download bachelor's thesis](docs/bachelors_thesis.pdf)` and `[View project poster](docs/thesis_poster.pdf)`. GitHub file URLs can be copied into admissions forms.

## 2. Hardware images: `Hardware-Images/`

Choose several clear photos of the insole, sensor wiring, assembly and enclosure, plus relevant result plots such as `accuracy_plot.png`, `confusion_matrix.png`, and `sensor_input_radar.png` from your local FYP results folder. Prefer descriptive filenames. Upload only images you can distribute; obtain consent from identifiable people and exclude sensitive participant details.

## 3. CAD and 3D-printing files: `Hardware_Files/`

Upload **STL exports** first, since admissions reviewers can preview or download these easily. Optional: upload selected `.SLDPRT` and `.SLDASM` SolidWorks files that you are authorized to share. If the set is large, organize it under `Hardware_Files/stl/` and `Hardware_Files/cad/`, with a README describing part names and print/assembly requirements.

## What will stay private

- Python, MATLAB, Arduino or microcontroller source code
- LSTM model files, checkpoints, `.h5`, `.pkl` and intermediate training artifacts
- All datasets, raw participant CSV files, and records with health or identifying details

The published IEEE paper remains linked through its [official DOI](https://doi.org/10.1109/INMIC65900.2025.11348422), rather than redistributing the publisher PDF.

## Final check for applications

After uploading, open the thesis file from GitHub in a private/incognito browser window. Check that it renders without requiring sign-in. Use its file URL in admission fields specifically asking for the thesis. Use the repository home page for research/portfolio fields.
