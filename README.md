# Farris Family Recipe Book

A personal project that involves adding all the recipes that I can get my hands
on and make it available to everyone's phone.

## Features

- **Digital & Convenient!** No more physical recipe books taking up counter
space. Mount your phone on a stand and access all your recipes instantly.

- **No Ads!** I'm committed to running this ad-free, because who wants to see
ads relating to deodorant when you're trying to cook up some family recipes?

- **Easy to follow!** All the recipes I use follow the same template:
Ingredients, then instructions! Notes are included either as footnotes or it's
own section. No ranting to make someone scroll all the way down to get to the
good stuff.

## Roadmap

I'm still learning so I don't know how this project will go. But if it does
start taking off, I want to start tracking progress of features.

## Contributing

So I use [Material for MKDocs](https://squidfunk.github.io/mkdocs-material/) as
the framework for this site, basically taking a simple document structure
(Markdown) and turning it into a static webpage with features like search.

To contribute to the recipes, use the [Recipe Template](docs/recipes/.templates/Recipe%20Template.md)
and save with title name under `docs/recipes`. You can leave out
unnecessary descriptors ("the", "at", "in") so it's shortened. See file names
for examples.

### Prerequisites

Before you start, make sure you have `git` and `python` installed on your
machine. Check your versions, as python 3.11+ is needed to run MkDocs:

```bash
git --version
python3 --version
```

### Building the project

Then you create a new folder and clone the repo (example for Linux nerds):

```bash
mkdir -p ~/projects/recipebook/
git clone https://github.com/Flabbyaxe272/recipebook.git
cd recipebook
```

Next, set up the virtual environment in the root directory:

```bash
# in ~/projects/recipebook/
python3 -m venv .venv
```

Then activate it:

| macOS / Linux             | Windows                | Windoes (PowerShell)       |
| ------------------------- | -----------------------| ---------------------------|
| ```bash                   | ```                    | ```                        |
| source .venv/bin/activate | .venv\Scripts\activate | .venv\Scripts\Activate.ps1 |
| ```                       | ```                    | ```                        |

You'll see (.venv) in your prompt when it's active. Verify using `which pip`,
which should have `~/projects/recipebook/.venv/bin/pip` or corresponding
directory.

Then come the python3 dependencies:

```bash
pip install mkdocs mkdocs-material
```

OR

```bash
pip install -r requirements.txt
```

After the requirements are installed, then run a local preview by using:

```bash
source .venv/bin/activate
mkdocs serve
```

Take note where it's generating the website. Often it's `http://127.0.0.1:8000`
From there, it should allow you to build it live, with live reload as you make
edits.

And that's how you build it.
