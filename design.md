# Intro

This app will:
- provide a centralised place to store links to useful resources on the web. 
- allow the user (me) to create new resources
- get a list of resources that match given criteria
- edit a given resource
- delete one or more given resources

# Data model

A *resource* is a pointer to some useful item of information on the web (an article, webpage, video etc). It consists of:
- A URL that points to the resource
- A description that gives a brief summary as to the content.
- One or more tags that associate the resource with particular topics

In addition to the standard Django models, we will need:

_Resource model_
- id (int, pk)
- description (varchar)
- url (varchar)

_Tag model_
- id (int, pk)
- tag (varchar)

_ResourceTag model (many to many link table)_
- Resource.id
- Tag.id

# Front end

The UI will be a simple HTML / Bootstrap page that provides the following:
- A search field. This should return any resources where i) the search appears in the resource description field, or ii) the search string matches one of the tags associated with the resource.
- A list of resources which match the search criteria.
- A means to add new resources to the list.
- A means to add new tags to the list.

At least at first, I'm happy to use the built-in admin facility to manage content.
