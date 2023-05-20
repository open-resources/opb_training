# Prairie Learn System workflow

The markdown files that are created to author questions are then parsed by a function in [problem_bank_scripts](https://github.com/open-resources/problem_bank_scripts). The function creates the correct format in which the question should be uploaded to PrairieLearn to be able to correctly be randomised and displayed.

Your markdown files are sent to PrairieLearn when you add the `syntax check` label to it in your pull request. This triggers a Github action which makes `problem_bank_scripts` parse your question and pushes your files to be available on PrairieLearn.

[PrairieLearn](https://ca.prairielearn.org/pl) has an impressive randomisation system where the answer choices can get shuffled and new variants of the question can be created using the different randomisation ranges and files that you provide in the Python code section while creating the markdown file.

![Image for files created by pbs for PL](https://user-images.githubusercontent.com/2507459/128770962-2a8b1cf7-500a-4968-ab8d-94b50cd019fc.png)

These files can also be found on PrairieLearn once your question is available there.
You might want to change the values in the `question.html` or the `server.py` file to try and debug your question if there is an issue, but make sure to make the same changes in the file locally and push it to the Github repository.