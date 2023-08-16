# Updating the IND 100 repository

Once you fork the repository, you will be working on your own repository (with its own history, branches, commits, issues, pull requests, etc...).
Occasionally, we will update the IND 100 course as new features are implemented and added to the OPBs and to PrairieLearn.
The easiest way to update your fork, is to use GitHub's "Sync Fork" feature:

<img src="pl_images/ind100_sync_fork.png">

## Update `problem_bank_helpers`

Though the "Sync Fork" feature will address most things, it's also useful to know how to update custom python packages on PrairieLearn, such as the `problem_bank_helpers` package.
Each course that uses an OPB requires the `problem_bank_helpers` to be installed within the `serverFilesCourse` directory.
More details about this are in the [PrairieLearn documentation](https://prairielearn.readthedocs.io/en/latest/questionRuntime/#installing-libraries-in-your-course)

Here's how we can use pip to install the package (and its dependencies that are not already on PrairieLearn):

```
pip install --target serverFilesCourse/ problem_bank_helpers sigfig sortedcontainers --no-deps
```

To update this package, we just need to add the `--upgrade` flag:

```
pip install --target serverFilesCourse/ problem_bank_helpers --no-deps --upgrade
```

That should be it!

```{tip}
Remember to add, commit, and push the changes so the repository is updated correctly.
```