# RQ1: Taxonomy Generation
This folder contains the files for RQ1. It has the source code and the repository extraction files which are used for taxonomy generation. Below is a description of all the files:

1. get_repositories.py extracts repositories with keywords: 'deep neural network' and 'deep learning' and star count > 50. With that we get 6655 repositories.

2. Then the downloaded csv files have information about these repositories with number of releases > 1. These files are in the folder github_repositories.

3. We combine these files to get 696 repositories. These are in 'Repositories - Owner and repo'.

4. We then mine issues with keywords: feature request and enhancement using get_issues.py. We get issues.csv containing 3997 issues.

5. We only consider issues with comments > 0 to only get issues that are relevant and have been interacted with. We use get_issues_comments.ipynb to do this. We get filtered_issues.csv with 1860 issues.

6. We manually label to get model related changes by answering the question: Does the issue deal with requirement change in pre-trained model? We get 168 issues in 42 repositories.
   
7. Repositories.xlsx contains a comprehensive sheet of all the steps mentioned above as well as the final filtered repositories which are in the sheet named "final".

8. We have also attached a pdf file named "Examples of Change Types" which gives one example each of the identified changes.
