require 'jekyll'

# Usage: bundle exec rake deploy
desc 'Deploy to gh-pages'
task :deploy do
  system 'bundle exec jekyll build'
  origin = `git config --get remote.origin.url`

  # Make a temporary directory for the build before production release.
  # This will be torn down once the task is complete.
  Dir.mktmpdir do |tmp|
    cp_r '_site/.', tmp
    Dir.chdir tmp
    system 'touch .nojekyll'
    system 'git init'
    system 'git add --all && git commit -m "Site updated at #{Time.now.utc}"'
    system "git remote add origin #{origin}"
    system 'git push origin master:refs/heads/gh-pages --force'
  end
end
