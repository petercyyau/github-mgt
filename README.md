## github-mgt

# install gh
brew install gh

# lgin gh
gh auth login

# Retriev all repos
gh repo list drpeteryau-uofg --limit 10 | while read -r repo _; do
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
