# Heroku buildpack

This is a buildpack that you can use if you can't change your Gemfile from git@github.com to https://github.com/ paths, but would like to use <https://github.com/timshadel/heroku-buildpack-github-netrc> to access private gems when deploying to heroku.

## This works around this bundler feature:

If you have code to detect the environment and dynamically change paths in `Gemfile`, bundler will say:

E.g. `You are trying to install in deployment mode after changing your Gemfile. Run bundle install elsewhere and add the updated Gemfile.lock to version control.`

## Installing

    heroku buildpacks:add -i 1 https://github.com/barsoom/change-ssh-to-https-in-gemfile-buildpack.git
