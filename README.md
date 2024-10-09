<p align="center">
  <img src="https://raw.githubusercontent.com/p-society/artwork/master/gifs/typeracer.gif" />
</p>

> Practice touch typing and compete with your friends all from the comfort of your shell and become a typing ninja :boom:.

[![Build Status](https://travis-ci.org/p-society/typeracer-cli.svg?branch=master)](https://travis-ci.org/p-society/typeracer-cli)
[![Codacy Badge](https://api.codacy.com/project/badge/Grade/baa51166cb03438488dd285d331fdad8)](https://www.codacy.com/app/knrt10/typeracer-cli?utm_source=github.com&amp;utm_medium=referral&amp;utm_content=knrt10/typeracer-cli&amp;utm_campaign=Badge_Grade)

*But this has already been done. Why should I use this client?*

Because most other shell clients don't offer the features that we do

---

# Sections
- [Features](#features)
- [Installation](#installation)
  - [Possible Errors](#possible-errors)
  - [How to update](#how-to-update)
  - [Errors while update](#errors-while-update)
- [Usage](#usage)
- [Help menu](#help-menu)
- [Modes overview](#modes-overview)
  - [Practice mode](#practice-mode)
    - [To start practice mode](#to-start-practice-mode)
    - [Preview of practice mode](#preview-of-practice-mode)
  - [Online mode](#online-mode)
    - [To start online mode](#to-start-online-mode)
    - [To view the Highscores](#to-view-the-highscorestop-10-in-online-mode)
    - [Prevew of online mode](#preview-of-online-mode)
- [Contributing](#contributing)
- [Support Us](#support-us)
- [Contributors](#contributors)

---

# Features

- Practice mode (offline mode)
- User stats (words per minute, time taken)
- Online mode (have a type-race by spawning up a server and sharing it with your friends)
- Ask for a rematch after the race ends (online mode)
- Can view the top 10 Highscores in online mode
- Dockerized image

---

# Installation

1. **Docker:** (default option `practice`)
```bash
sudo docker image pull p-society/typeracer-cli:latest
```

2. **Direct installation**, run from your command line
```bash
npm i --global typeracer-cli
```

<br />

## Possible Errors

When you have installed this tool some times later you could find some error when you start **typerace**.

This may be because new update might have been rolled out and you have to update to latest version.

<br />

## How to update

1. **Docker:**
```bash
sudo docker image pull p-society/typeracer-cli:latest
```

2. **Binary:**
```bash
npm i --global typeracer-cli`
```

<br />

## Errors while update
1. find **.nvm** folder in your home directory.
```bash
ls -ld ~/.nvm
```

2. cd to `.nvm/versions/node/${your node version}/bin` and delete **typerace** file
```bash
cd ~/.nvm/versions/node/${node --version | awk -F 'v' '{print $2}'}/bin
rm typerace
``` 

3. cd to `.nvm/versions/node/${your node version}/lib/node_modules` and delete **typeracer-cli** directory
```bash
cd ~/.nvm/versions/node/${node --version | awk -F 'v' '{print $2}'}/lib/node_modules
rm -r typeracer-cli
```

4. Try to install again:
```bash
npm i --global typeracer-cli
```

**These steps should resolve the isssue. If it does not please open an isssue.**

---

# Usage

1. **Docker:** (Default option `practice`)
```bash
sudo docker container run -it --rm p-society/typeracer-cli [-h/--help] [options]
```

2. **Binary:**
```bash
typerace [-h/--help] [options]
```

---

# Help menu

```
Usage: typerace [options] [command]

  Options:

    -h, --help          output usage information

  Commands:

    practice|p          Start typeracer
    online|o [options]  Start game in online mode
```

---

# Modes overview

## Practice mode

### To start practice mode
```bash
sudo docker container run -it --rm p-society/typeracer-cli
```

**OR**

```bash
typerace p
```

<br />
  
### Preview of practice mode

![practice](https://user-images.githubusercontent.com/24803604/39970250-e3d22eca-5705-11e8-9c89-472ff4d982ea.gif)

<br />

## Online mode

### To start online mode
```bash
sudo docker container run -it --rm p-society/typeracer-cli o -f
```

**OR**

```bash
typerace o -f
```

You will be prompt by a question:

**Are you starting server for race (y/N) ?**

Now 2 cases are there:

- If **yes**
  - You will share **Room to join for race**, **Number of racers**, **Number(sort of password)**
  - All the above will be prompted if you select yes and all of your friends should fill them out same.

- If **no**  
  - Ask for **Room to join for race**, **Number of racers**, **Number(sort of password)** from your friend who created a private room to race.

<br />

### To view the Highscores:(Top 10 in online mode)
```bash
sudo docker container run -it --rm p-society/typeracer-cli o -s
```

**OR**

```bash
typerace o -s
```
<br />

### Preview of online mode

![online](https://user-images.githubusercontent.com/24803604/39970260-f63d6bc4-5705-11e8-8d94-b2f984f8c998.gif)

**Enjoy** :fire:

---

# Contributing

If you think of a feature enhancement or find a bug kindly raise an issue. We also welcome you to work on your issues by just commenting down on them with *"I would like to work on this"*. All contributions are appreciated.

**General Setup**

- fork the repository

- clone your forked repository

- set the upstream remote

- cd to folder and run `npm install`

- create a `.env` file in root directory and put following in it

```
DATABASE=your mongoDB url
```

- run `npm start`

*But I don't know how to code, is there any other way I can contribute?*

Yes, ofcourse you can we need lots of paragraphs so that our users don't get bored by typing out the same text over and over  again. To add a paragraph follow these steps:

- Add paragraphs in `paragraphs/para.json`
- run `npm test`
- **Important:** all tests should pass as you would get a test failure for duplicate paragraphs.
- Find same paragraphs then run `npm test`
- If all tests pass locally then **Open a PR**

---

# Support Us

We are a bunch of undergrads passionate about software development looking to make cool stuff. A little motivation and support helps us a lot. If you like this nifty hack you can support us by doing any (or all :wink: ) of the following:
- :arrow_up: Upvote on producthunt [producthunt](https://www.producthunt.com/posts/typeracer-cli)
- :star: Star us on [Github](https://github.com/p-society/typeracer-cli) and make us trend so that other people can know about our project.
- :clap: Clap for us on [Medium](https://medium.com/programming-society-gazette/shellracer-bbce3efbe888)
- Tweet about us
- Share this on Facebook
- Install it and increase our download count on npm
- Donation (Coming Soon)

---

# Contributors

- *Conceived by:*  :thought_balloon: <a href="https://github.com/shibasisp">Shibasis Patel</a>
- *Developed by:*  :computer: <a href="https://github.com/knrt10">Kautilya Tripathi</a>
- *Documentation by:*  :pencil: <a href="https://github.com/palash25">Palash Nigam</a> & <a href="https://github.com/IamRaviTejaG">Ravi Teja Gannavarapu</a>
