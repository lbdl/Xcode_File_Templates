# xcodeTemplates
Specta test case template files for Xcode

Useage
======

Xcode (6) keeps its file templates in the app bundle which are of course liable to being overwritten by updates etc.
Just for reference this path is (at time of writing) 

    /Applications/Xcode.app/Contents/Developer/Library/Xcode/Templates/File Templates/
  
Xcode will also check the following directory

    ~/Library/Developer/Xcode/Templates/
  
Clone the repository and move the contents into your local Templates directory,` ~/Library/Developer/Xcode/Templates/` create this directory if it does not exist.

You should now have the following structure.

    ~/Library/Developer/Xcode/Templates/File Templates/SpectaTestCase.xctemplate

An actual Template consists of a Directory named `xxx.xctemplate` which contains a `.plist` file an `.icns` file and `.h` and `.m` files.

For more information on these files and variations please read the excellent post by Bob McCune found
[here](http://www.bobmccune.com/2012/03/04/creating-custom-xcode-4-file-templates).

There is also more information on Project Templates etc [here](http://blog.boreal-kiss.net/2011/03/11/a-minimal-project-template-for-xcode-4/)
and [here](http://ericasadun.com/2014/06/30/building-custom-extension-templates/)

Considerations
--------------

The name of the template file is important, Bob McCune uses `___FILEBASENAME___.m` in the case of his custom GHUnit tests. This did not work for me, examination of Apples templates files led me to use the `___VARIABLE_xxx___Spec.m` as the base template file (in this case `xxx` is `productName` in the  `<key>Options</key>` array and to remove the `MainTemplateFile` key. I assume this key is redundant if there is only one template file to be considered.

I could not find a way of creating an autocomplete field that populates with the classes in the project.

**NOTE** The template paths may well change at the whim of Apple. So far the local directory
  ~/Library/Developer/Xcode/Templates/
seems a pretty reliable place for custom templates.

**Further** If you need to change licenses etc then there is a good project that deals with this by [royclarkson](https://github.com/royclarkson/xcode-templates)

