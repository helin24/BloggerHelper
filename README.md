## Overview

Writing long-form pieces can be a good way to keep large audiences informed, but the work and time required to collect cohesive thoughts prevents many from embarking on this endeavor. This app aims to collect disparate pieces of content we create/consider regularly (e.g. emails we write to friends or articles we've read) and organize them by topics to ultimately provide us with "nearly-bloggable" content. "Nearly-bloggable" content has many potential forms - snippets we've written to different people that share a common theme, question prompts arising from articles on a topic that we've read, etc.


## MVP Components

### User Authentication
- Implement OAuth from google?

### Gmail scraping

#### Functionality needed
- Connect to gmail
- Filter relevant emails - e.g. only those written to others
- Store relevant emails and metadata

#### Implementation notes
- [Overview](https://developers.google.com/gmail/api/guides/overview#key_resource_types)
- [Messages](https://developers.google.com/gmail/api/v1/reference/users/messages#methods)
- We probably just need to put the client library in our Django project
- Mainly need to implement messages that were sent by the user


### Browser tracking

#### Functionality needed
- Track content read in browser
- Filter for relevant activity - e.g. only articles read completely
- Store relevant content and metadata

#### Implementation notes
- [Overview](https://developer.chrome.com/extensions/getstarted)
- [More details](https://developer.chrome.com/extensions/overview)
- It may be better to use chrome API since we don't need to modify anything in the browser? Not sure what the API is like
- If using an extension, may need content scripts to grab relevant portions of web pages

### Storage of relevant information
- Table of users
- Table for each source of data
- Table of topics-sources

### Models to extract topics
- Use nltk to tag content by topic
- Gather multiple content together by topic
- Make snippets of single topics

### Interface to display topics and snippets
- Django web application?
- Display all saved content
- Generate snippets by topic


## Things to research
- The concept of HTTP requests
- MIME type and how emails are sent
- Base64 encoding for emails
