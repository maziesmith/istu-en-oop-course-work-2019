# Variant 5. Postcard creator:

1. __Create the main form using Visual Designer__
---------------------------------------------

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/pic_variant5.png)


2. __Add click event listener to "Open file" button__
-------------------------------

This button should open [OpenFileDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-open-files-using-the-openfiledialog-component) which should accept images (bmp, png, jpeg)

And display image in "Input" block


3. __Create class that implement following interfaces__
-------------------------------

```c#

interface IPostcardJob{
  int Border { get; }
  string Heading { get; }
  string Text { get; }
}

interface IPostcardManager{
  Bitmap MakePostcard(Bitmap input, IPostcardJob job);
}

```
`IPostcardJob` - holds parameters of processing

`IPostcardManager` - does all job of processing

Create new image and use [DrawImage](https://docs.microsoft.com/en-us/dotnet/api/system.drawing.graphics.drawimage?view=netframework-4.8)

Example of result:

![Result](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/postcard.png)

4. __Add click event listener to "Resize image" button__
---------------------------------------------

It should read data from controls, create object of class that implements `IPostcardJob` and then call `MakePostcard` method. 

After that, it should open [SaveFileDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-save-files-using-the-savefiledialog-component) and write resulting picture to file

5. __Add click event listener to "About" button which creates new "About" form using code__
---------------------------------------------

Use code to create and display new form:

![About form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/about_form.png)

[Example of creating form using code](https://docs.microsoft.com/en-us/dotnet/api/system.windows.forms.form?redirectedfrom=MSDN&view=netframework-4.8)

6. __Add click event listener to "Close" button in "About" form__
---------------------------------------------

This button should close About form

[Example of attaching event listeners using code](https://docs.microsoft.com/en-us/dotnet/framework/winforms/how-to-create-event-handlers-at-run-time-for-windows-forms)

7. __Create UML class diagram for business-logic classes__
-----------------------------------------------
[Wiki](https://en.wikipedia.org/wiki/Class_diagram)

8. __Create a report/paper for course work__
-----------------------------------------------
Report should consist of:
- Table of contents
- Description of your task
- Description how you solve your task
- UML class diagram
- Code
- Screenshot of the program
