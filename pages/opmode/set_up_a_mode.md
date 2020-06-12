**1**. We will create a module (a module is a collection of modes).
Navigate to <https://seec.intelligentplant.com/> (if required log in
using your LinkedIN, Google or Azure active directory account), click on
"Add new module" card to add your new module.

![](/opmode/opmode_step1.gif)

**2**. Once a module is added we are taken to its page where we can
start defining modes. Hit "Add new mode" card to start the process.

**3**. Here we can see that we are presented with a dialog with trend in
it. Choose your datasource and your tags which will define your mode
(Note: minimum 2 tags must be added to define a mode). Find an area in
the Trend which represents your mode (plant shutdown mode, engine
overheating, fridge freezing, etc.), highlight it and once the trend has
zoomed in - that's it. Your mode start and end dates are defined by the
area of the trend window. Once you click "OK" in Trend dialog a new
"Area" card will appear, you can edit and add new areas to tweak your
mode definition.

Give your mode a name (this will be the tagname as well in target
datasource) and a description, choose where you would like to save the
results and hit "Create Mode".

![](/opmode/opmode_step2.gif)

By default OpMode will profile 6 months of historical data and then will
subscribe to new values coming in for the selected tags. You can track
the progress displayed on the mode card or visualize them in trend by
finding your newly created tag:

##### Historical import finishing and subscribing to new values

![](/opmode/opmode_step3.gif)

##### Mode visualisation in Trend

In the picture below you can see how we superimpose mode results against
the source tag data. You can see the mode changing quite a lot ( yellow
line ).

![](/opmode/opmode_trenddemo.gif)
