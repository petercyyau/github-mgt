## github-mgt
Reference: https://stackoverflow.com/questions/19576742/how-to-clone-all-repos-at-once-from-github

# install gh
brew install gh

# login gh
gh auth login

# Retriev all repos
gh repo list [<owner>] --limit 10 | while read -r repo _; do
  print $repo
done

# download repo to local
gh repo clone "$repo" "$repo"

# Delete a GitHub repository.
gh repo delete
gh repo delete [<repository>] [flags]

Options
--yes
confirm deletion without prompting
