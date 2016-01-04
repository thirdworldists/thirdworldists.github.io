require 'rake'
require 'date'
require 'yaml'

SOURCE_BRANCH = "develop"
DESTINATION_BRANCH = "master"

desc "Generate the site and push changes to remote origin"
task :travis do
    # Detect pull request
    if ENV['TRAVIS_PULL_REQUEST'].to_s.to_i > 0
      puts 'Pull request detected. Not proceeding with deploy.'
      exit
    end
    
    # Generate the site
    sh "bundle exec jekyll build"
    
    # Commit and push to github
    sha = `git log`.match(/[a-z0-9]{40}/)[0]
    Dir.chdir("_site") do
      sh "echo '**This branch contains the generated website. To make changes, see the [develop](https://github.com/thirdworldists/thirdworldists.github.io/tree/develop) branch.**' > README.md"
      sh "git remote add origin https://github.com/thirdworldists/thirdworldists.github.io.git"
      sh "git add -A"
      sh "git commit -m 'Updating to develop@#{sha}.'"
      sh "git push -u --force origin #{DESTINATION_BRANCH}"
      puts "Pushed updated branch #{DESTINATION_BRANCH} to GitHub Pages"
    end
  end
