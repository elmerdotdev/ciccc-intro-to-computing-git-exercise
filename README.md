# Extended Git and GitHub Exercise: Mastering Git Commands

**Objective**: This exercise aims to teach students how to manage a Git repository, including using `git add`, `git commit`, `git restore`, `git mv`, `git rm`, `git clean`, `git revert`, `git log`, and how to work with files in Git.

## Setup

1. Go to a folder where you want to put the repository. Clone the repository from GitHub by running:
   - `git clone https://github.com/yourrepositoryurl`

2. Navigate into the cloned directory:
   - `cd git-github-exercise`

### Part 1: Basic Add and Commit

1. Create a new file called `instructions.txt` and write a simple welcome message:
   - `echo "Welcome to My Git Project" > instructions.txt`

2. Stage and commit the file:
   - `git add instructions.txt`
   - `git commit -m "Add instructions.txt with welcome message"`

3. Push the changes to GitHub:
   - `git push`

### Part 2: Updating and Using Git Restore

1. Modify the `instructions.txt` file by adding a section about the project description:
   - `echo "\n## Description" >> instructions.txt`
   - `echo "This project demonstrates basic Git and GitHub operations." >> instructions.txt`

2. Stage and commit the changes:
   - `git add instructions.txt`
   - `git commit -m "Update instructions.txt with project description"`

3. Accidentally modify another section:
   - `echo "\nAccidental addition" >> instructions.txt`

4. Restore the last accidental addition:
   - `git restore instructions.txt`

### Part 3: Advanced File Handling

1. Rename `instructions.txt` to `guide.txt`:
   - `git mv instructions.txt guide.txt`
   - `git commit -m "Rename instructions.txt to guide.txt"`

2. Accidentally add a temporary file:
   - `touch temp.txt`
   - `git add temp.txt`

3. Remove `temp.txt` from tracking and delete it:
   - `git rm temp.txt`
   - `git commit -m "Remove temporary file"`

4. Clean up any untracked files (like if `temp.txt` was never added):
   - `git clean -f`

### Part 4: Using Git Log and Revert

1. Introduce a new change:
   - `echo "\nThis will be reverted soon." >> guide.txt`
   - `git add guide.txt`
   - `git commit -m "Add line to be reverted"`

2. Use `git log` to view the commit history:
   - `git log`

3. Revert the last commit:
   - `git revert HEAD --no-edit`

### Part 5: Making Additional Changes

1. Make additional changes to `guide.txt`:
   - `echo "\nThis project helps to understand Git basics." >> guide.txt`
   - `git add guide.txt`
   - `git commit -m "Update guide.txt with Git basics info"`

2. Push the changes to GitHub:
   - `git push`
