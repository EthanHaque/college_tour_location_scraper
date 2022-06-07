# College Tour Location Scraper

Scrapes the website [https://www.youvisit.com/collegesearch/](https://www.youvisit.com/collegesearch/) for the images 
and locations colleges bring people on in their virtual tours.

## Description

The following pieces of information are gathered:

- Ids of the Universities.
- Names of the Universities.
- Ids of the tours for each University (each university can have more than one tour).
- Title of the stops on the tours.
- Ids of the stops on the tours.
- Names of the media files for each stop
- A description of the media files for each stop (if a description exists)
- Type of media for each stop
- Downloads the media for each stop.

Out of the four main types of media that the website provides (photos, panoramas, videos, and audio) the scraper gathers
photos and panoramas. This makes up the majority of the media the website serves on its tours.

The tours often have descriptions for the locations on the tours that are associated with a group of images for the stop
on the tour. These descriptions are useful because they give context to the images on the tours. Additionally, the 
descriptions are often the transcribed text of an accompanying video/audio for the tour.

## Usage Information

The notebook named "api_endpoint_scraper" contains the code to scrape all the desired information from the website. 
The notebook is divided into several parts that each perform an intermediate step to download the content from the 
website. Open the notebook, install the dependencies, and run all the cells to download the content. 

## Why Data is Needed

The data is for a study for Princeton's Stigma and Social Perception Lab. The goal of the study is to analyze how 
colleges signal diversity and inclusion matters to them by the places they take people on their tours. 

## Implementation Details

Two approaches were used to gather the relevant data. First, selenium was used to gather the content of different tours
from the content served in the browser. This approach was not how the final data was gathered, but the code for this 
implementation was left in the repo. Second, requests was used to manipulate open api endpoints to gather the content
from the website. This second approach was how the final data was gathered.