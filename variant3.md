# Variant 3. Stitching:

1. __Create the main form using Visual Designer__
---------------------------------------------

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/pic_variant3.png)


2. __Add click event listener to "Open folder" button__
-------------------------------

This button should open [FolderBrowserDialog](https://docs.microsoft.com/en-us/dotnet/framework/winforms/controls/how-to-choose-folders-with-the-windows-forms-folderbrowserdialog-component)

And display number of found images (png, bmp, jpeg) from selected folder


3. __Create class that implement following interfaces__
-------------------------------

```c#

interface IStitchingJob{
  bool Direction  { get; } // false - column, true - row
  int Margin { get; }
}

interface IStitchingManager{
  Bitmap Stitch(Bitmap input, IStitchingJob job);
}

```
`IStitchingJob` - holds parameters of processing

`IStitchingManager` - does all job of processing

Create new image and use [DrawImage](https://docs.microsoft.com/en-us/dotnet/api/system.drawing.graphics.drawimage?view=netframework-4.8)

For column:

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/cols_stitch.png)

For row:

![Form](https://raw.githubusercontent.com/Nordth/istu-en-oop-course-work-2019/master/images/rows_stitch.png)

4. __Add click event listener to "Save stitched" button__
---------------------------------------------

It should read data from controls, create object of class that implements `IStitchingJob` and then call `Stitch` method. 

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

