# Mini-Conf - Data Description

All data for Mini-Conf can be provided either as CSV, JSON, or YAML. 
So it does not matter if you provide a `papers.csv` or a `papers.yml` as long as
the required data fields are provided.

## Global Configuration (config.yml)

- name: `<short name>`
- tagline: `<long name>`
- date: `<Date of conference>`
- proceedings_title: `<proceedings name for citation>`
- citation_date: `<date for citation export (no HTML)>`
- analytics: `<Google analytics ID starting with UA... >`
- logo: 
    - image: `<link to logo>`
    - width: `<width of the image> or "auto"`
    - height: `<height of the image> or "auto"`
- site_title: `<name of the site>`
- page_title:
    - prefix: `<text to include in title of every page>`
    - separator: `<characters between prefix and name of the current page>`
- background_image: `<link to background image>`
- organization: `<conference committee name>`
- chat_server: `<url of rocket chat server, if used>`
- default_presentation_id: `<default slideslive id, if used>`
- default_poster_pdf: `<default poster pdf, if used>`

## Detail Pages

### committee [.csv | .json | .yml]
The list of members of the orga team visible on the landing page

  - role: `<Chair name>` 
  - name: `<Name>`
  - aff: `<Affiliation>`
  - im: `<Image URL>`
  - tw: `<Twitter name>`


<hr>

### papers [.csv | .json | .yml]
The list of papers.

- UID: `<Unique ID>`
- title: `<paper title>`
- authors: `<list of authors>` -- (seperated by `|` in CSV)
- abstract: `<abstract text>`
- keywords: `<list of keywords>` -- (seperated by `|` in CSV)  
- sessions: `<list of session IDs>` --  (seperated by `|` in CSV) 

<hr>

### speakers [.csv | .json | .yml]
The list of keynote talks.

- UID: `<Unique ID>`
- title: `<talk title>`
- institution: `<affiliation>`
- speaker: `<speaker name>`
- abstract: `<talk abstract>`
- bio: `<short bio>`
- session: `<session ID>`

<hr>

### workshops [.csv | .json | .yml]
The list of workshops or socials.

- UID: `<Unique ID>`
- title: `<workshop title>`
- authors: `<organizer names>`
- abstract: `<abstract text>`
- [TBD] url: `<external link>`

<hr>

### faq [.json | .yml]
The list of FAQ questions partitioned into sections.

 - Section: `<Section Name>`
 - QA:
      - Question: `<Question>`
      - Answer: `<Answer>`

Example (.yml):
```yaml
FAQ:
  - Section: Test Section
    QA:
      - Question: What is a good question?
        Answer: "Here are the answers"
```

