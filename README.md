# Markdown Writing Advise
## Introduction

The goal of this article is to provide some tips for write clear and consistent articles. The focus is on explaining various of the GitHub/MarkDown syntax posibilities.

Include a small introduction. Try to explain in a line or 3 what the article it's goal is. Ensure the reader doesn't have to scroll through the article to guesstimate what the content/result will be.

## Table Of Content

Include a TOC at the top of the article. This allows for easy navigation and also provides the reader a clear overview of what to expect.
The MarkDown for a TOC can simply look like this:

```
* [Abstract](#abstract)
* [Learning objectives](#learning-objectives)
```

These are basically hyperlinks to the headers in your article. You can reference any level of header by specifying the header and replacing spaces with dashes ("-"). Here's an example:

* [Header 1](#information)
* [Header 2](#more-details)
* [Header 3](#explanation)

# Information

Foo bar

## More Details

Some more foo bar

### Explanation

And more of the same.

## Lists

GitHub doesn't mind if you use +, - or *. All of them wil result in a list like this:

```
+ first item
- second item
* third item
```


+ first item
- second item
* item


* first item
* second item
* item

But it makes more sense to use * accross all articles. 




Try to use headers where it makes sense instead of trying to use multiple levels of bullets. The headers can also easily be linked in a TOC.

When using numbered lists make sure to restart them after each header. 


Try to avoid using bullets where possible
Using headers for providing structure / context switches
Use double spaces at the end of a line (or bullet) to have the image following appear inline without a bullet
Be consistent. Some people split words like Azure Web App vs Azure WebApp. Imho it's not a real issue as long as each article is consistent on it its own.
Don't use capitals where it's not needed.

https://docs.microsoft.com/en-us/azure/virtual-network/virtual-networks-create-nsg-arm-pportal


image in bullet:
white line before image
then 4 spaces (tab)

inline lists of properties can be in an intended bullet. But don't include returns/enters with images as that will add a lot of whitespace between the bullet items

scaling of images

restart numbered lists after a new header/logical segment

indent screenshots



Why me on the v-team for pptless
* I'm really into content development
-> became an MVP for FIM after writing technet wiki's in collaboration with a MS Doc Writer
-> As a PFE I worked on managed intellectual property: I'm very responsible/have an eye for detail
-> As a PFE I contributed/wrote articles for the official AD FS docs

-> I'm familiar with the GitHub and Docs.com processes/tooling

-> I've got some ideas how we can make this work
