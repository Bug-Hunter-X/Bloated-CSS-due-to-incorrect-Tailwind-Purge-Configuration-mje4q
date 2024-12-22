# Bloated CSS in Tailwind CSS Project

This repository demonstrates a common issue in Tailwind CSS projects where the CSS output is significantly larger than expected. The problem stems from an incorrect configuration of the `purge` option in the `tailwind.config.js` file.  This leads to all potential Tailwind CSS classes being included in the final CSS bundle, even if they aren't actually used in the project.

## Problem

The `tailwind.config.js` file has an improperly configured or missing `purge` option. This results in a bloated `styles.css` file, impacting website performance.

## Solution

The solution is to correctly configure the `purge` option in `tailwind.config.js` to specify the locations of your templates or components. Tailwind will then only include the CSS classes used in these files.

## How to Reproduce

1. Clone this repository.
2. Build the project (instructions will vary depending on your project setup).
3. Observe the size of the generated CSS file. It will be much larger than necessary.
4. Examine `tailwind.config.js` to see the problem configuration.
5. Examine `tailwind.config.fixed.js` to see the corrected configuration.
6. Rebuild the project with the corrected configuration.  The size of the CSS file will significantly decrease.