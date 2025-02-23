# Pen Colors

Repository of pen colors for plotting.

## What it is

This repository is a catalogue of pen colors in computer-readable formats.

Although the tooling is in Node.js, it is intended to be generic and usable by any system.

## How it works

Each pen color is represented by a token, defined in JSON files using the [DTCG format](https://www.w3.org/community/design-tokens/).

These files are transformed using Style Dictionary to a multitude of formats,
with the goal of being compatible with most languages and frameworks.

# Add colors

Colors are defined as tokens in JSON files in the `src` folder. 

Each file represent a brand. The structure of the files should follow the brand naming and categorization.

## FAQ

### What's it for?

Creative coders who want to plot their artworks need to approximate their
pen colors on the computer during preview. This project aims to standardize and simplify the process 
by having a single source of truth available to everyone in a wide range of formats.

### I don't use Node.js, NPM or Javascript. Is this project not for me?

You can download or link to the colors in JSON format on different CDN: https://unpkg.com/pen-colors@1.0.2/lib/json/pen-colors.json
