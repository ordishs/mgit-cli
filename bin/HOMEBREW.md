To publish on Homebrew:

git tag v1.0.0

git push --tags

cd bin

git archive --format=tar.gz --output=../mgit-cli-1.0.0.tar.gz v1.0.0 mgit-cli 

cd ..

gh release create v1.0.0 mgit-cli-1.0.0.tar.gz --title "mgit-cli 1.0.0" --notes "Latest release of mgit-cli."

# Get the SHA256 hash of the release
curl -L https://github.com/ordishs/mgit-cli/releases/download/v1.0.0/mgit-cli-1.0.0.tar.gz | shasum -a 256


Edit mgit-cli.rb in github.com/ordishs/homebrew-mgit-cli to update tar name and sha

brew tap ordishs/mgit-cli
brew install mgit-cli


