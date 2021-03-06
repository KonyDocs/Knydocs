Skip to content
 
Search or jump to…

Pull requests
Issues
Marketplace
Explore
 
@KDocz 
1
0 0 KDocz/Knydocs
 Code  Issues 0  Pull requests 0  Projects 0  Wiki  Security  Insights  Settings
Knydocs/Responsive Web
@premgvg premgvg Create Responsive Web
a876b43 7 days ago
114 lines (71 sloc)  11.8 KB
    

# Overview
Kony Visualizer SP2 version enhances the existing Responsive design feature. Prior to Kony Visualizer SP2 Responsive Web design was done through code. From Kony Visualizer SP2, you can build Responsive Web desktop applications using Visualizer.


For a more hands-on approach on the Responsive design feature provided by Kony AppPlatform, import and preview the [Resort Feature sample app](https://marketplace.kony.com/items/resort-feature-app) by using Kony Visualizer.

**Note**: The Responsive Web design feature is currently available only for the Desktop Web platform.

**Important**: Ensure to enable Responsive Web in the Desktop Web Properties section here.

When your app is open in a browser, if the browser window resizes, content which is in a bigger layout does not resize according to the smaller layout automatically. Responsive web enables you to design your desktop web applications to fit various layouts and create a glitch free browsing experience.

There are three pre-existing breakpoints, Mobile, Tablet, and Desktop They help you resize your web application to pre-set scales. You can either use them or you can create your own custom breakpoint and use it. The ruler in the form assists you in viewing these breakpoints. When you hover on the breakpoint section, the breakpoint area is highlighted in the ruler indicating the screen size.

You can switch between various breakpoints set on the canvas. When you click a break point, the canvas resizes to the width specified on that breakpoint and all the content in the canvas adjusts according to the specified canvas width. You cannot hide the ruler when breakpoints are set for a form.

![Responsive Design Break point](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/responsive_designbp.gif)

You can resize the breakpoints using the resize handle icon on the right side of the canvas. This provides a quick review so that you can determine the exact width where the content design breaks during the resize. You can also use a key (Command + D key in Mac and Ctrl + D key in Windows) when you reach the required width to insert a breakpoint of a specified width when you are resizing a breakpoint. You can drag a breakpoint in a ruler.

![Responsive Design Resize](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/reswebcanvasresize.gif)

For New projects, you can use the three default values or create a new one by using the Add New button.

* Desktop - 1200 PX
* Tablet - 1024 PX
* Mobile - 640 PX
* Add New - Button

![Responsive Design Break point](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/breakpointintro.gif)

For existing projects, you do not have any default breakpoints. You can add a breakpoint by using the Add New button.

Breakpoints are always sorted from largest to smallest. If you add a new breakpoint which is larger than the existing large breakpoint, the newly added largest one goes to the top.

Important: A new event onBreakpointChange is added to the Actions list in the Properties pane. You can define what happens to the form when the breakpoint changes.

## Breakpoint Forking
You can choose the layout for each of the breakpoints separately by using the Breakpoint Forking feature. When this feature is turned on, you can rearrange your layout in the form, specific to each breakpoint. This helps you in defining how you want to display the form in each layout. You can choose the changes at the breakpoint level or a global level for all breakpoints.

![Breakpoint Forking](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/responsivebreakpointforking.gif)


Important: When you turn Breakpoint Forking on, you can fork your widgets separately for each breakpoint. If you do not fork your widgets for each breakpoint, the canvas will resize only a few widgets and not all of them.

## Working with Skins, Widgets, and Components
You can also fork skins for different breakpoints. For Video and Image widgets, the source of images and videos can be forked based on the breakpoint. For Labels, whenever you change a breakpoint in the canvas, the width of the label changes and the content wrapping is adjusted for the breakpoint.

When you drag and drop a widget to the form and make changes, unless you have selected the Breakpoint Forking feature, all changes reflect across breakpoints. If a breakpoint is forked, changes will not reflect in that breakpoint.

When you drag and drop a widget on any breakpoint, the widget is added to all breakpoints. When you delete or rename a widget on a breakpoint, the widget is deleted or renamed on all breakpoints. You can change properties of a widget specific to each breakpoint.

You can use components across breakpoints. You cannot create components with forked responsive properties. You can use Desktop web templates for the Responsive Web application. You can also create different templates for different breakpoints. Once you publish your responsive web app, you can preview the app in the kdw (desktop web output) mode.

## Responsive Web APIs
The following are the APIs, keys, and constants associated with Responsive Web.

* [kony.application.setApplicationBehaviors (Breakpoint key)](https://docs.kony.com/konylibrary/visualizer/viz_api_dev_guide/Default.htm#kony.application_functions.htm%23kony.app)
* [kony.application.getCurrentBreakpoint();](https://docs.kony.com/konylibrary/visualizer/viz_api_dev_guide/Default.htm#kony.application_functions.htm%23kony.application.getCurrentBreakpoint)
* [constants.BREAKPOINT_MAX_VALUE](https://docs.kony.com/konylibrary/visualizer/viz_api_dev_guide/Default.htm#kony.application_functions.htm%23top)

## Create a Breakpoint
To create a Responsive Design application, do the following:

1. On the File menu (the Project menu in Kony Quantum Visualizer), click New Project to open the Start a New Project screen of the New Project wizard.
1. Select Create Custom App, and then click Choose. Kony Visualizer opens the Project Type screen of the New Project wizard.
1. In the Project Name text box, enter a name for your project. <br>A project name should contain fewer than 14 characters.<br>A project name can be alphanumeric. However, the first character of a project should always be a letter. <br>Do not use any of the following reserved keywords as a project name: authService, workspace, mfconsole, kpns, middleware, accounts, syncservice, syncconsole, services, admin, middleware, and appdownload.
1. Select Kony Reference Architecture, and then click Create. As this is a new project, in the Project Explorer, you will see Responsive Web / Desktop. <br>
![Responsive Design Project Explorer](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/responsive_design_projectexplorer.png)

1. Right-click Form > New Form. This results in creating a new form with a default name assigned to it.
1. You will have three different breakpoints by default. <br>You can view these breakpoints in the Properties pane. <br>![Responsive Design Project Explorer](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/responsive_design_bp_properties.png)

1. To add a new breakpoint, click Add New. A new row appears. <br>![Responsive Design Add New Breakpoint](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/responsive_design_bp_addnew.png)

1. Enter the breakpoint details. You will see that the new breakpoint is added.  <br>![Responsive Design Add New Breakpoint](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/responsive_design_bp_addnew2.png)<br>The breakpoint is added and it reflects in the Properties pane and the Canvas. 
## Create a form with Breakpoint Forking Off
To create a form with Responsive Web with Breakpoint Forking Off, do the following:

1. In your Visualizer Project, on the form that you want to use Responsive Web design, in Visualizer Canvas, select Responsive Web. <br> ![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/reswebselect.png)<br>The Responsive web layout appears on Visualizer Canvas. <br>Tip: You may want to set the view of Canvas to 75%. Setting the canvas to 75% view makes it easier to navigate through three different breakpoints.
1. Drag and drop a FlexContainer to the form. 
1. Ensure that this FlexContainer is spread across all three default breakpoints. <br>Tip: For better visibility on how the canvas changes the FlexContainer in different breakpoints, you may want to change the background color of the FlexContainer.
1. Add a few TextBox widgets to the FlexContainer. <br>Tip: Add three TextBox widgets spread across the entire canvas.
1. Add a few buttons below the FlexContainer in the form. <br>Tip: Ensure that three buttons are spread across the entire canvas.
1. Using the resize handle, resize the canvas to different breakpoints, observe how the breakpoints change.
<br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/reswebnobrekpoint.gif)
## Create a form with Breakpoint Forking On
To create a form with Responsive Web with Breakpoint Forking On, do the following:
1. In your Visualizer Project, on the form that you want to use Responsive Web design, in Visualizer Canvas, select Responsive Web. <br> ![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/reswebselect.png)<br>The Responsive web layout appears on Visualizer Canvas. **Tip**: You may want to set the view of Canvas to 75%. Setting the canvas to 75% view makes it easier to navigate through three different breakpoints. 
1. Drag and drop a FlexContainer to the form.Ensure that this FlexContainer is spread across all three default breakpoints.<br>Tip: For better visibility on how the canvas changes the FlexContainer in different breakpoints, you may want to change the background color of the FlexContainer.
1. Add a few TextBox widgets to the FlexContainer. <br>**Tip**: Add three TextBox widgets spread across the entire canvas.
1. Add a few buttons below the FlexContainer in the form. <br>**Tip**: Ensure that three buttons are spread across the entire canvas.
1. On Visualizer Canvas, toggle the Breakpoint Forking button. <br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/breakpointforkingon.png)
1. At this point, your UI elements are already organized for the largest breakpoint. <br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/bpforkinglarge.png)

1. Using the canvas resize handle, resize the canvas to the tablet layout.

1. Reorganize your UI elements for this layout. <br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/bpforkingmedium.png)


1. Using the canvas resize handle, resize the canvas to the mobile layout.

1. Reorganize your UI elements for this layout.<br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/bpforkingsmall.png)


1. Your form now has three different views for three different breakpoints.
1. Using the resize handle, resize the canvas to different breakpoints, observe how the breakpoints change. <br>![Responsive Design ](https://github.com/premgvg/docs/blob/master/konylibrary/visualizer/viz_user_guide/Images/GIFS/rwbreakpyes.gif)


1. To view your app locally on an internet browser, from the Project Menu, click Run and select Run.
1. The project is built for the Responsive web channel and you can view the app in your internet browser.
To invoke any function that is not supported by Visualizer, you can do it through code. Click here for more information.
© 2019 GitHub, Inc.
Terms
Privacy
Security
Status
Help
Contact GitHub
Pricing
API
Training
Blog
About
)
