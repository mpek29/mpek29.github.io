---
layout: page
title: MailSpreader
description: 📧 Automate LinkedIn-based mailings
full_name: mpek29/MailSpreader
img: assets/img/projects/MailSpreader/main.png
importance: 1
git: https://github.com/mpek29/MailSpreader
github: https://github.com/mpek29/MailSpreader
category: Computer Science
subcategory: DevOps & Automation
---



**MailSpreader** is a Python command-line tool to automate LinkedIn-based mailings.
It collects company profiles, extracts metadata, finds emails, generates summaries, and exports data into a spreadsheet-ready format.

## Installation


Clone and install directly from GitHub:

```bash
pip install git+https://github.com/mpek29/MailSpreader
```

## Usage


```bash
mail-spreader [OPTIONS] COMMAND [ARGS]...
```

### Global Options



* `--install-completion` → Install shell completion for the current shell  
* `--show-completion` → Show shell completion script  
* `--help` → Show this message and exit  
 

## Available Commands


| Command                                  | Description                                                                |
| ---------------------------------------- | -------------------------------------------------------------------------- |
| `list-industries-to-linkedin-url`        | Convert a list of industries into LinkedIn URLs                            |
| `linkedin-url-to-profil-json`            | Convert LinkedIn URLs into a JSON list of company profile URLs             |
| `profil-url-to-metadata-json`            | Convert company profile URLs into JSON metadata                            |
| `metadata-json-to-email-json-auto`       | Generate a JSON of emails from metadata JSON (automatic mode)              |
| `metadata-json-to-email-json-manual`     | Generate a JSON of emails from metadata JSON (manual/operator-assisted)    |
| `metadata-json-to-summaries-json`        | Generate a JSON of business summaries from metadata and config             |
| `summaries-json-en-to-fr`                | Translate summaries JSON from English to French                            |
| `metadata-email-json-to-spreadsheet`     | Merge metadata, email, and summaries JSON into a CSV spreadsheet           |

## Example Workflows


### Convert industries YAML into LinkedIn URLs



This repository includes a collection of `.yaml` files that contain various industries available as filters on LinkedIn. These files, referred to as "list of industries files," enable users to target specific industries for job applications. You can find these files in the following directory: `src/mail_spreader/templates/job/`.

To customize your experience, you have the option to create your own "list of industries" `.yaml` file to better suit your needs.

The following command converts a specified industries `.yaml` file into a corresponding LinkedIn search URL. The generated URL will be saved in a file named `urls.yaml`.

```bash
mail-spreader list-industries-to-linkedin-url .	emplates\joblectronics_industries.yaml -o urls.yaml
```

> This command processes the electronics_industries.yaml file and creates a LinkedIn search URL that targets the specified industries.

### Change the URL to your desired location



The URL generated previously does not include a location filter. To customize it, simply open the URL and add your desired location.

Next, you can add the updated URL along with your LinkedIn credentials to the `config.yaml` file, located in the following directory: `src/mail_spreader/templates`. For security reasons, consider creating a separate LinkedIn account to avoid potential bans.

**Important**: Ensure that the total number of pages in your LinkedIn search does not exceed 100 pages. If your search generates more than 100 pages, you will need to split the LinkedIn search URL into multiple URLs. One effective approach is to create separate URLs for each industry, location if possible, available job etc...

Once you have your URLs ready, you can add them to the `config.yaml` file in a YAML list format.

### Convert LinkedIn URLs into JSON



```bash
mail-spreader linkedin-url-to-profil-json .	emplates