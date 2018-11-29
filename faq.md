---
title: FAQs
---

# FAQs
## General
### Why is the project named “AgileReview”?
The project was named “AgileReview” as reviews can be done in a fast, flexible way which was summarized in the word “agile”. This has nothing to do with Agile Software Developement.

### Is AgileReview compatible to other RCPs?
Currently this is not tested and not guaranteed as the focus of our work is the compatibility to the normal eclipse environment. Especially one issue can be mentioned so far: AgileReview seems not to be compatible to Zend Studio 8.0.1

## Standard Review Functionality
### Why is my source code spammed with strange tags after reviewing and how do I get rid of all these tags?
In order to achieve refactoring stable comments, the location of comments have to be anchored in your source code – this is done by these comment tags.
After your review was finished at all, you can clean all comment tags out of a project by right-clicking on a project in the package-explorer and start the AgileReview cleanup.

## Advanced Review Functionality
### What are Smart Suggestions?
Smart Suggestions provide you with previously entered values for common data fields such as comment recipient.

### Which template should I use for the review export?
The template should be an instanziation of the provided raw templates in the download section. You can implement some more analytical functionalities for your export template. The only constraint is, that the first four excel sheets should not be changed to guaranty a successful export with AgileReview.

## Review Data
### What is a AgileReview Source Project? Do I need more than one?
All your review data are saved as XML files in a project in your workspace. We call this type of project an AgileReview Source Project. AgileReview saves the review data in this way, so you can do reviews ranging over multiple projects and use your version management tools in eclipse to share your reviews.
You can create (or have) multiple of these AgileReview Source Projects in order to share different review data with different teams and/or tools. To switch between AgileReview Source Projects select the projects you want to use in the preferences are activate a Source Project by right-clicking on it and selecting Activate AgileReview Source Folder.

### Where is the review data saved?
The review data is saved as a project in your Eclipse workspace. It contains all reviews and comments.

### How can I share my review data?
You can share your review data by any means, but we recommend using a version control system for easy sharing (the review data are stored in a way to minimize conflict).

### How do I add a project/file/… to a review?
Resources like projects or files are automatically added to a review. Just add a comment to a file. The complete tree structure of project and folders that contains the file is displayed in the Review Explorer.

## Coding Language Support
### How do I adapt AgileReview to specific languages?   (e.g.: C#, .Net, etc.)
This adaption is done within the Eclipse-preferences. (They can be found in “Window > Preferences”.) There you have to navigate to the Language Support of AgileReview and specify your own language support by inserting a new row in the table (press the plus button). A valid row contains the fileendings of the files you want to review, the comment begin identifier (begin tag) for your language and the comment end identifier (end tag).

### My target language does not support block comments. Can I still use AgileReview?
AgileReview does not really depend on block comments. Just fill in the line comment identifier in the begin tag column and some arbitrary character (e.g. the same character as the begin tag) in the end tag column. The end tag column must not be empty!
Example: Perl
fileendings: pl
begin tag: #
end tag: #

The drawback of this alternative is, that no productive code can be written behind the comment tags (as the whole line behind the comment tags is a comment then).

### I added my own language support. Is AgileReview still stable against refactorings?
To be honest, we do not know. It can be, but if your target language plugin uses it’s own refactoring mechanisms AgileReview might not be notified of the refactorings. We can only guarantee refactoring stability for the JDT (Java Development Tools).

## Limitations
### Why can’t I review files using specific editors?
At the moment only single-page text editors (such as Java editor or plain text editor) are supported. Support for other (also multi-page) editors will be included in future releases.

### Does AgileReview also work on Mac OS?
To be honest, we do not know. We received some mails stating problems with AgileReview on Mac OS, but since nobody of us owns a Mac we can not test on Mac OS or verify these problems.

Is it possible to define different statuses and priorities?
It was an initial idea of us to make status and priority customizable but it has not been implemented yet. So at the moment the answer is No but we plan on improving that.