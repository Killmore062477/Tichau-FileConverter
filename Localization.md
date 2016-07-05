In the next version of File Converter (v1.1) there will be a localization system that will automatically translate the application depending on the language set in Windows. This language will be overridable in the application options.

You can help File Converter adding new supported languages to the application. Here is the steps to follow:

- Fork the File Converter repository in GitHub.
- Switch to the "development" branch to have the latest version of File Converter project.
- Go to project folder FileConverter\Application\FileConverter\Properties\.
- Duplicate the file _Resources.resx_ and rename it _Resources.{language-culture-name}.resx_. 
You can find the list of the language culture names here: [Table of Language Culture Names](https://msdn.microsoft.com/library/ee825488(v=cs.20).aspx).
For example to create the french localization resources file, name the file _Resources.fr-FR.resx_.
- Edit the created file with your prefered text editor and fill all the data values.

Example:
    `<data name="About" xml:space="preserve">
         <value>`**A propos**`</value>
    </data>`

- Finally create a pull request in GitHub so I can integrate your contribution in the project.

If you have visual studio installed, you can directly edit the resx file in a graphical interface.

Thanks a lot for your help :) !
