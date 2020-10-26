# WebCore Kit Sketch Library
### Overview
This is a test for hosting a Sketch library which can be updated and maintained as part of a GitHub repository. Changes to the library can be pushed to the repo and reviewed in the GEL team before merging. Then, users with the RSS feed linked to their personal Sketch application should then get any new updates.

> This test has been largely successful when trialled in the GEL team. But, has raised a few thoughts around maintenance, version control, and what happens if Dave get hit by a bus.

## Linking the library to your Sketch application
To link the library to your Sketch application, you simply need the URL which points to the XML file in this repo.

`sketch://add-library?url=https%3A%2F%2Fgithub.com%2Fdave-morris%2FWebCore-kit-test%2Fraw%2Fmain%2FWebCore-UI-kit-DRAFT.xml`

The first part of this url `sketch://add-library?url=` simply tells the browser to open the link using Sketch, and tells Sketch to open as a library.

If you're creating a new file or updating the file name, a new URL needs to be formatted using a Meyer Web URL encoder.

## Updating the Library
So far, it's only been one user creating, maintaining and updating the library. In the future, we may need to have multiple designers working on one Sketch library.

This presents new challenges to keeping the library up to date.

Designers can have a local repo of the library cloned to their laptops. They have the potential to create any changes to the library using a separate branch which can be merged when the changes are complete. This kind of workflow could be a steep learning curve for a designer and their knowledge of git.

For now, I would say just one designer keeps the library up to date and stored locally on their machine until we've trialled merging changes from multiple machines at once.

To do this, simply make the changes to a cloned repo. Some parts of the XML file need to be updated too, such as the published date and sparkle-version. Then, sdd, commit and push the changes to the master branch.

Updates should then be dished out to all users who have the RSS/XML feed added to their Sketch application. Sketch _apparently_ checks for updates to 3rd party libraries hourly. So changes may take a little while to come through.

## The future
As this is just a test, the next steps for project are:

- Finish the WebCore UI Kit Sketch library
- Weigh up the pros and cons of a GitHub Repo for hosting and maintaining a Sketch library. Are we making our lives more difficult for the sake a smaller barrier to entry?
- Figure out an approach that works for the whole GEL team to keep a file like this up to date.
- Trial the update of a Sketch Library when multiple people have made changes.
