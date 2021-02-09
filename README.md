# WebCore Kit Sketch Library
### Overview
This is a Sketch library which can be _delivered_ or added to a designer's Sketch application via RSS. A Sketch library remotely hosted like this has the added benefit of version control in Github, a lower barrier to entry for the designer to start using the library and better conflict management (it cannot be edited or changed locally).

> This test has been largely successful when trialled in the GEL team. But a few thoughts has been raised around maintenance, version control, and governance.

## Linking the library to your Sketch application
To link the library to your Sketch application, you simply need the URL which points to the XML file in this repo.

`sketch://add-library?url=https%3A%2F%2Fgithub.com%2Fbbc%2FWebCore-UI-Kit%2Fraw%2Fmain%2FWebCore-UI-kit-DRAFT.xml`

The first part of this url `sketch://add-library?url=` simply tells the browser to open the link using Sketch, and tells Sketch to open as a library.

If you find this broken in the future, follow the documentation for Libraries on the Sketch website.

## Updating the Library
So far, it's only been one user creating, maintaining and updating the library. In the future, we may need to have multiple designers working on one Sketch library.

This presents new challenges to keeping the library up to date.

Designers working to improve the library can have a local repo cloned to their laptops. They have the potential to create any changes to the library using a separate branch which can be merged when the changes are complete. This kind of workflow could be a steep learning curve for a designer and their knowledge of git.

For now, I would say just one designer keeps the library up to date at a time and stored locally on their machine until we've trialled merging changes from multiple machines at once.

To do this, simply make the changes to a cloned repo. Some parts of the XML file need to be updated too, such as the published date and sparkle-version. Then, add, commit and push the changes to the master branch.

Updates should then be dished out to all users who have the RSS/XML feed added to their Sketch application. Sketch _apparently_ checks for updates to 3rd party libraries hourly. So changes may take a wee while to come through.

## The future
We're now at the stage where we can trial this with UX designers, the next steps for project are:

- To continue adding more features to the kit where there is a requirement to do so
- Weigh up the pros and cons of a GitHub Repo for hosting and maintaining a Sketch library. Are we making our lives more difficult for the sake a smaller barrier to entry?
- Figure out an approach that works for the whole GEL team to keep a file like this up to date
- Include the licensing before sharing outside a core group of trial WebCore Designers
- Find a solution for storing binary files on Git that still allows the library to be installed as a 3rd Party Library

## License
These assets are available for download on the following licence terms:

> You can:
> - Download the assets and use them free of charge;
> - Use the assets without attribution (but we’d appreciate it if you could let us know); and
> - Modify or alter the assets and edit them as you like.

> You can’t:
> - Use the assets in a way that would bring the BBC into disrepute;
> - Make available the assets so that they can be downloaded by others;
> - Sell the assets to other people or package the assets with others that are for sale;
> - Take payment from others to access the assets (including putting them behind a paywall);
> - Use the assets as part of a service that you are charging money for; or
> - Imply association with or endorsement from the BBC by using the assets.

> _Disclaimer: The assets are offered as is and the BBC is not responsible for anything that happens if you use them._
