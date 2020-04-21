---
layout: lesson
title: "Session 14"
output: markdown_document
---

## Topics
*




str_detect / regular expresssions

I'd like to understand the gender and racial/ethnic representation of graduates at different stages of their training. I'm going to start the analysis with "Microbiology". To do this analysis, I need to develop a sense of how the data are reported. A "microbiologist" is a very diverse concept! They can study organisms in any of the three domains of life, viruses, interactions with animals or plants or the natural environment. They can be engineered ecosystems. They can be studied at the gene, protein, organismal, or community level. Depending on the campus, the people that study microbes at these various levels can be one person in a Biology department or 20 in a Microbiology department or 200 across 20 different departments. How we organize data into a framework is critical to the interpretation of our data. We could be the best R programmer in the world, but if we can't get the definitions right, we're toast.

Inspecting the CIP codes, I see that there's some organization to them - the first two numbers correspond to a broad dicipline (e.g. 26 - Biology or 27 - Math). Of course, I immediately noticed that "26.1102 - Biostatistics" is listed under Biology and not under Math and "27.0306 - Mathematical Biology" is listed under Math rather than Biology. For the microbiology-affiliated fields I listed above, I notice that their CIP codes all start with "26.05". Among those CIP codes, there are

* 26.0502	Microbiology, General
* 26.0503	Medical Microbiology and Bacteriology
* 26.0504	Virology
* 26.0505	Parasitology
* 26.0507	Immunology
* 26.0508	Microbiology and Immunology
* 26.0599	Microbiological Sciences and Immunology, Other

Of course, there are Immunologists that don't think much about microbes and there are card carrying microbiologists in general Biology departments and *even* Engineering. This overlap between subdisciplines is why it is a bad idea to aggregate all institutions blindly and to rather pick peer institutions where one has a better understanding of where a microbiologist would most likely be trained within that institution. In other words, take this analysis with a small grain of salt...

I'd like to see whether the