# Generate a new SSH key
ssh-keygen

# Add the public key to authorized keys
cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys

# Print the public key
cat ~/.ssh/id_rsa.pub

# Create a directory for repositories
mkdir repos
cd repos

# Clone the forked repository (replace 'YourGitHubUsername' with your GitHub username)
git clone git@github.com:YourGitHubUsername/CSCE1015.git
cd CSCE1015

# Append EUID section to README.md (replace YOUR_EUID with your actual EUID)
echo '## EUID' >> README.md
echo YOUR_EUID >> README.md

# Append Favorite Professor section to README.md (replace YOUR_FAVORITE_PROFESSOR with the professor's name)
echo '## Favorite Professor' >> README.md
echo 'YOUR_FAVORITE_PROFESSOR' >> README.md

# Check the status to see changes not staged for commit
git status

# Stage the README.md file
git add README.md

# Check the status to see changes staged for commit
git status

# Commit the changes
git commit -m "Updated readme file"

# Push the changes to the remote repository
git push

# Show the commit log
git log
