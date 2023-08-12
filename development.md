# setup

following https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll

install ruby Wait I have ruby `ruby -v` I'm on 2.6.10

install bundler wait I have bundle /usr/bin/bundle


but jekll recommends not using that verison of ruby, so I won't.
https://jekyllrb.com/docs/installation/macos/

it wants

brew install chruby ruby-install xz
ruby-install ruby 3.1.3

echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc # run 'chruby' to see actual version

check version with ruby -v
then
gem install jekyll


but instead I'll put it in a project

bundle init
bundle add jekyll
no, github-pages instead?? according to generated gemfile comments

bundle exec


## okay time for pelican in python

## Initial setup

```
poetry new .
poetry add pelican
poetry add "pelican[markdown]"
poetry install
poetry run pelican-quickstart # interactive setup
```

## setup themes

```
cd ~/code/
mkdir getpelican
cd getpelican
git clone --recursive https://github.com/getpelican/pelican-themes.git
poetry run pelican-themes --install ../../../getpelican/pelican-themes/pelican-mockingbird 
poetry run pelican-themes --list # confirm install
```

## development

generate static content:

```bash
poetry run pelican content
```

then serve it locally:

```bash
poetry run pelican --listen
```

publish it:

```bash
poetry run pelican content -o output/ -s publishconf.py
```