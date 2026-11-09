# github-lab
Labs 
mkdir github-lab
cd github-lab
git init -b main

echo "# My First GitHub Lab" > README.md
git add README.md
git commit -m "Initial commit: add README"

echo "This lab teaches basic Git commands and GitHub usage." >> README.md
git add README.md
git commit -m "Updated README with project description"

git checkout -b feature-update
echo "This change was made on the feature-update branch." >> README.md
git add README.md
git commit -m "Added branch-specific update to README"

git checkout main
git merge --no-ff feature-update -m "Merge branch feature-update"
git branch -d feature-update

echo "Learning Git via command line is an essential developer skill." >> README.md
git add README.md
git commit -m "Added note about Git command line importance"

git log --oneline --graph
