# Variant 4. Cutting:

1. __Create the main form using Visual Designer__
---------------------------------------------

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/pic_variant4.png)


2. __Add click event listener to "Open file" button__
-------------------------------

This button should open [OpenFileDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-open-files-using-the-openfiledialog-component) which should accept images (bmp, png, jpeg)

3. __Create class that implement following interfaces__
-------------------------------

```c#

interface ICuttingJob{
  int X { get; }
  int Y { get; }
  int Width { get; }
  int Height { get; }
}

interface ICuttingManager{
  Bitmap Cut(Bitmap input, IResizerJob job);
  Bitmap GetPreview(Bitmap input, IResizerJob job); // Should draw rectangle of cutting zone
}

```
`ICuttingJob` - holds parameters of processing

`ICuttingManager` - does all job of processing

[How to crop and scale images](https://docs.microsoft.com/en-us/dotnet/framework/winforms/advanced/how-to-crop-and-scale-images)

4. __Add event listener for clicking of "Cut image" button and for changing of input controls__
---------------------------------------------
Each time user changes parameters of cutting you should create object of class that implements `ICuttingJob`, call `GetPreview` method and then display result into "Preview" block

When user clicks "Cut image" button you should create object of class that implements `ICuttingJob`, call `Cut` method and then open [SaveFileDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-save-files-using-the-savefiledialog-component) and write resulting picture to file

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
