---
layout: note
title: HTML File Paths
parent: HTML
grand_parent: Home
---

# HTML File Paths

To get files to talk to one another you have to create a path between them, **a route between files**. For example `<img src="assets/images/awesome-picture.png" alt="My awesome image">` provides the html with directions to the image file to display on the site.

- To link to a target file in the same directory as the invoking HTML file, just use the filename, e.g. `my-image.jpg`.
- To reference a file in a subdirectory, write the directory name in front of the path, plus a forward slash, e.g. `subdirectory/my-image.jpg`.
- To link to a target file in the directory above the invoking HTML file, write two dots. So for example, if `index.html` was inside a subfolder of _test-site_ and `my-image.jpg` was inside `test-site`, you could reference my-image.jpg from index.html using `../my-image.jpg`.
- You can combine these as much as you like, for example `../subdirectory/another-subdirectory/my-image.jpg`.

Remember to follow the conventions in [[Dealing With Files and Folders]]

---
## Backlinks
* [[HTML]]
	* [[HTML File Paths]]

