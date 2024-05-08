# Initialize a new Git repository
git init

# Add a remote repository named 'origin'
git remote add origin https://github.com/neehargadam/git_assignment_HeroVired

# Create and switch to a new branch named 'dev'
git checkout -b dev

# Add all files to the staging area
git add .

# Commit changes with a message
git commit -m "Add Calculator class with basic arithmetic operations and square root method"

# Push changes to the 'dev' branch on the remote 'origin' repository
git push -u origin dev

# Switch to the 'main' branch
git checkout -b main

# Merge the 'dev' branch into the 'main' branch
git merge dev -m "Merge dev branch into main"

# Create a new tag named 'v1.0' with a message
git tag -a v1.0 -m "Version 1.0 release"

# Push 'main' branch changes and tags to the remote repository, overwriting existing tags
git push origin main --tags --force

# Create and switch to a new branch named 'feature/sqrt'
git checkout -b feature/sqrt

# Commit changes with a message
git commit -m "Implement square root feature"

# Push changes to the remote 'feature/sqrt' branch
git push origin feature/sqrt

# Add specific file(s) to the staging area
git add calculator.py

# Commit changes with a message
git commit -m "Fix divide function to handle division by zero"

# Switch to the 'feature/sqrt' branch
git checkout feature/sqrt

# List all branches
git branch

# Switch to the 'dev' branch
git checkout dev

# Switch to the 'main' branch
git checkout main

# Merge the 'dev' branch into the 'main' branch
git merge dev

# Create a new tag named 'v2.0' with a message
git tag -a v2.0 -m "Version 2.0 release"

# Pull changes from the remote 'main' branch
git pull origin main

# Push 'main' branch changes and tags to the remote repository
git push origin main --tags

# Install Git LFS (Large File Storage)
git lfs install

# Create and switch to a new branch named 'lfs'
git checkout -b lfs

# Create a large binary file
fsutil file createnew Neehar_large_file.large 209715200

# Track large binary files using Git LFS
git lfs track "*.large"

# Add all files to the staging area
git add .

# Commit changes with a message
git commit -m "Add large binary file(s) tracked by Git LFS"

# Push changes to the remote 'lfs' branch
git push origin lfs

# Create and switch to a new branch named 'geometry-calculator'
git checkout -b geometry-calculator

# Add GeometryCalculator.py file with GeometryCalculator class
git add GeometryCalculator.py
git commit -m "Add GeometryCalculator.py file with GeometryCalculator class"

# Create and switch to a new branch named 'feature/circle-area', stashing changes for later
git stash push -m "Circle Changes"

# Check the status of the working directory and staging area
git status

# Create and switch to a new branch named 'feature/rectangle-area', stashing changes for later
git checkout -b feature/rectangle-area
git stash push -m "Rectangle Changes"

# Switch to the 'feature/circle-area' branch and apply the stash
git checkout feature/circle-area
git stash apply stash@{0}

# Commit changes with a message
git commit -m "Implemented circle area feature"

# Push changes to the remote 'feature/circle-area' branch
git push origin feature/circle-area

# Switch to the 'feature/rectangle-area' branch and apply the stash
git checkout feature/rectangle-area
git stash apply stash@{1}

# Commit changes with a message
git commit -m "Implemented rectangle area feature"

# Push changes to the remote 'feature/rectangle-area' branch
git push origin feature/rectangle-area
