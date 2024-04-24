## 0x14. JavaScript - Web scraping

This project focuses on utilizing JavaScript to perform web scraping tasks, covering various objectives related to manipulating JSON data, working with APIs, and reading/writing files using the `fs` module.

### Learning Objectives

- Understand why JavaScript programming is powerful.
- Learn how to manipulate JSON data.
- Master the use of request and fetch API.
- Gain proficiency in reading and writing files using the fs module.

### Requirements

- Allowed editors: vi, vim, emacs
- Interpreted on Ubuntu 20.04 LTS using Node.js (version 14.x)
- All files should end with a new line
- First line of all files should be `#!/usr/bin/node`
- A `README.md` file at the root of the project folder is mandatory
- Code should be semistandard compliant, using Standard rules with semicolons
- All files must be executable

### How to Install Node 14

```bash
$ curl -sL https://deb.nodesource.com/setup_14.x | sudo -E bash -
$ sudo apt-get install -y nodejs
```

### How to Install semi-standard

```bash
$ sudo npm install semistandard --global
```

### How to Install request module

```bash
$ sudo npm install request --global
$ export NODE_PATH=/usr/lib/node_modules
```

### Tasks Overview

1. **Readme**
   - Write a script that reads and prints the content of a file.

2. **Write me**
   - Write a script that writes a string to a file.

3. **Status code**
   - Write a script that displays the status code of a GET request.

4. **Star wars movie title**
   - Write a script that prints the title of a Star Wars movie based on the episode number provided.

5. **Star wars Wedge Antilles**
   - Write a script that prints the number of movies where the character "Wedge Antilles" is present.

6. **Loripsum**
   - Write a script that retrieves the contents of a webpage and stores it in a file.

7. **How many completed?**
   - Write a script that computes the number of tasks completed by user id.

8. **Who was playing in this movie?** (Advanced)
   - Write a script that prints all characters of a Star Wars movie.

9. **Right order** (Advanced)
   - Write a script that prints all characters of a Star Wars movie in the same order as the list "characters" in the response.
