# Google-Scholar-API

# I. Introduction:
The API should be able to obtain authors information, bibliography, publications from a Google Scholar search query. The API will use web crawler to grasp the aforementioned information from Google Scholar and transform them into a machine and human readable format. It is able to search by title-only,  publication date timeframes and return publication title, most relevant web link, PDF link, number of citations, number of online versions, link to Google Scholar's article cluster for the work, total number of hits. It also includes other functions like inclusion/exclusion of patents and citations, retrieval of citation details in standard external formats as provided by Google Scholar, including BibTeX and EndNote, Cookie, higher query volume, ability to persist cookies to disk across invocations.

# II. Methods of the Under Developing API: 

## A, scholar_search: allows users to search an author by name.

### 1, Returns an entry or multiple entries which authors may have a same name, including:

A unique ID for the author, in order to distinguish homonymous authors. √

The author’s name √

The author’s  affiliation √

The author’s email * (Not fullfilled. No author’s email available)

The author’s total number of being cites √

The author’s publications with Doi * (Not fullfilled. No Doi available. Also it will be too redundancy if the program show author’s publications)

### 2, Parameters: 

Name: a string (ignore capitalization), for instance:

	A string: ‘Jian Chen’ 
  
Number of the results showed: an integer, the default is all found results.

Publications: a integer decides the maximum number of each author’s publications showed, the default is 0, for instance:

	Show at most 1 publications for each author: publication = ‘1’
	Not show any publication: publication = ‘0’
	Show at most 3 publications for each author:  publication = ‘3’
  
Exact match: a boolean decides whether the result should exactly match the input, the default is no.	

## B, keyword_search: allows users to search a publication by key word or exact mach by title:

### 1, Returns an entry or multiple entries including:

The number of results found  √

The title √

Doi * (Not fullfilled. Google Scholar does not contain Doi)

Author(s) with a unique ID √

The number of being cited √

The number of versions √

Keywords √

Journal √

Url √

Abstract √

### 2, Parameter:

Key word(s) in title or abstract: a string search for title and abstract, for instance: 

  A string: input = ‘nonprofits’ or input = ‘strategic collaboration between nonprofits and businesses’
  
Year of publication until: an integer.

Year of publication since: an integer.

Exact match: a boolean decides whether the return publications’ title should exactly match the input, the default is no.

## C Export: allows users to export result into a CSV file.  √

### 1, Returns: 

A CSV file which contains results exported by a user.

### 2, Parameter:

Data produced by the previous two functions

## D, Proxy and Tor: * (Not fullfilled. Google can identify robots even if I use proxy and Tor)
