# xcodeTemplates
Specta test case template files for Xcode

Useage
======

Xcode (6) keeps its file templates in the app bundle which are of course liable to being overwritten by updates etc.
Just for reference this path is (at time of writing) 

    /Applications/Xcode.app/Contents/Developer/Library/Xcode/Templates/File Templates/
  
Xcode will also check the following directory

    ~/Library/Developer/Xcode/Templates/
  
So create that directory it does not exist. Clone the repository in the Templates directory and you should see the following structure.

    ~/Library/Developer/Xcode/Templates/File Templates/SpectaTestCase.xctemplate

An actual Template consists of a Directory named `xxx.xctemplate` which contains a `.plist` file an `.icns` file and `.h` and `.m` files.

For detailed information on these files and variations please read the excellent post by Bob McCune found
[here](http://www.bobmccune.com/2012/03/04/creating-custom-xcode-4-file-templates)

There is also more information on Project Templates etc [here](http://blog.boreal-kiss.net/2011/03/11/a-minimal-project-template-for-xcode-4/)
and [here](http://ericasadun.com/2014/06/30/building-custom-extension-templates/)

**NOTE** The template paths may well change at the whim of Apple. So far the local directory
  ~/Library/Developer/Xcode/Templates/
seems a pretty reliable place for custom templates.

