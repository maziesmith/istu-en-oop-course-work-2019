# Variant 1. Resizing:

1. __Create the main form using Visual Designer__
---------------------------------------------

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/pic_variant1.png)


2. __Add click event listener to "Open file" button__
-------------------------------

This button should open [OpenFileDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-open-files-using-the-openfiledialog-component) which should accept images (bmp, png, jpeg)

And display image in "Input" block


3. __Create class that implement following interfaces__
-------------------------------

```c#

interface IResizerJob{
  int Width { get; }
  int Height { get; }
  bool PreserveRatio { get; }
}

interface IResizerManager{
  Bitmap Resize(Bitmap input, IResizerJob job);
}

```
`IResizerJob` - holds parameters of processing

`IResizerManager` - does all job of processing

[How to crop and scale images](https://docs.microsoft.com/en-us/dotnet/framework/winforms/advanced/how-to-crop-and-scale-images)

4. __Add click event listener to "Resize image" button__
---------------------------------------------

It should read data from controls, create object of class that implements `IResizerJob` and then call `Resize` method. 

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

