A Github Pages template for academic websites. This was forked (then detached) by [Stuart Geiger](https://github.com/staeiou) from the [Minimal Mistakes Jekyll Theme](https://mmistakes.github.io/minimal-mistakes/), which is © 2016 Michael Rose and released under the MIT License. See LICENSE.md.

I think I've got things running smoothly and fixed some major bugs, but feel free to file issues or make pull requests if you want to improve the generic template / theme.

### Note: if you are using this repo and now get a notification about a security vulnerability, delete the Gemfile.lock file. 

# Instructions
## not Change this template
1. Register a GitHub account if you don't have one and confirm your e-mail (required!)
1. Fork [this repository](https://github.com/academicpages/academicpages.github.io) by clicking the "fork" button in the top right. 
1. Go to the repository's settings (rightmost item in the tabs that start with "Code", should be below "Unwatch"). Rename the repository "[your GitHub username].github.io", which will also be your website's URL.
2. Upload any files (like PDFs, .zip files, etc.) to the files/ directory. They will appear at https://[your GitHub username].github.io/files/example.pdf.  
3. Check status by going to the repository settings, in the "GitHub pages" section
4. Update variables in _config.yml to match your site， url is especially important
5. (Optional) Use the Jupyter notebooks or python scripts in the `markdown_generator` folder to generate markdown files for publications and talks from a TSV file.

See more info at https://academicpages.github.io/

## Custom made
- Update top menu bar (to add/remove items) by editing _data/navigation.yml
- Update files in _pages directory to set top-level (connect with top menu bar (navigation.yml) by variable **permalink**)
- Update files in corresponding folders (_publications, _posts, and so on) to set lower levels (top-level connects with lower levels by corresponding files, such as publications.md && _publications folder)
## To run locally (not on GitHub Pages, to serve on your own computer)

Guided by [office document](https://jekyllrb.com/docs/installation/) (Here, I only record instructions for Ubuntu plateform)

### Ubuntu 18.04
```bash
sudo apt-get install ruby-full build-essential zlib1g-dev

echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc

gem install jekyll bundler

cd YOURPATH
bundle clean --force
bundle install

# Generate the HTML and we can access the site from localhost:4000 by the local browser 
bundle exec jekyll liveserve 

# when above command is useless for the local browser
jekyll serve --incremental

```
