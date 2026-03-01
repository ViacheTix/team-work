**Repository Description**
This repository is dedicated to storing our machine learning and deep learning theory and course materials. It serves as our shared workspace for notes, practice, and collaborative study.

**Working as a Team with Jupyter Notebooks (.ipynb)**
*   Before starting any work on an `.ipynb` file, communicate with the team to ensure no one else is currently modifying it to prevent merge conflicts, which are difficult to resolve in notebooks. OR you can use .py files with jupyter notebook extension in VS code that allows to execute lines of code as if they were in jupyter's cell!
*   Consider creating a personal copy of a notebook or working in a separate branch if you plan to make extensive experimental changes.
*   Always clear the output of your cells before committing and pushing the `.ipynb` file to keep the repository size manageable and diffs cleaner.
*   Don't forget to save model's weights somewhere in the working directory so we could compare our results without executing the whole file again.

**General GitHub Workflow**
1.  First, pull the latest changes from the repository to ensure your local version is up to date: `git pull origin main`
2.  Make your changes to the files locally.
3.  Check the status of your changes: `git status`
4.  Add the files you want to include in your update: `git add <filename>` or use `git add .` to add everything.
5.  Commit your changes with a descriptive message so everyone knows what you did: `git commit -m "Your descriptive message here"` . It should be in imperative mood, for example:
* Updates README for punctuation
* Fix the broken toilet
* Add unit tests for user authentication 
6.  Finally, upload your changes to the shared repository: `git push origin main`

**Using Mamba for Environment Management**
Mamba is same as conda but faster and doesn't take up that much space on the machine!
*   Mamba is a fast, drop-in replacement for Conda, used to manage our project's packages and environments.
*   To create a new environment based on a configuration file, use: `mamba env create -f environment.yml`
*   To activate the environment before working, use: `mamba activate <environment_name>`
*   To deactivate the environment when you are done, use: `mamba deactivate`

**Creating and Updating environment.yml Files**
*   The `environment.yml` file ensures that everyone on the team has the exact same libraries and versions to run the code successfully.
*   If you install a new package that the team needs, you should update the shared environment file.
*   *Note:* It is often better to manually curate the `environment.yml` by adding only the specific packages you installed (e.g., `pandas`, `scikit-learn`, `torch`) rather than exporting the full list, to keep the file clean and cross-platform compatible.