# Create your own install guide

## How do I do it?
1. Just make a copy of this install_template directory. Name the directory after your install guide and put a `_mac`, `_windows` or `_whateverOS` at the end if the guide is platform specific.
2. Open the `README.md` file in the new directory.
3. Add your installation instructions to the file in markdown.
4. Open the README.md file in the top level of the repo and add a link to the index.html file inside the new install guide directory you created in step 1. Use a relative path and make sure you link to the index.html file **not** the README.md file. 
5. Push the new file to the `gh_pages` branch of the [https://github.com/treehouse/installation-guides](https://github.com/treehouse/installation-guides) repo.

Your new installation guide will appear at http://treehouse.github.io/installation-guides/[your-new-guide]/

Example: [http://treehouse.github.io/installation-guides/node_mac/](http://treehouse.github.io/installation-guides/node_mac/)


