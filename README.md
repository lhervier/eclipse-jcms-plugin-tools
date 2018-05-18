# eclipse-jcms-plugin-tools

Eclipse JCMS Plugin Tools - Tools to develop JCMS in Eclipse. 
We are looking for contributors so don't hesitate to get in touch with us in this public space hosted by Jalios : http://community.jalios.com/jcms/jc_97906/fr/eclipse-jcms-plugin-tools

# Compilation

Import the 4 projects into Eclipse (Oxygen is the current version)

- sync : This is a standalone Library, compiled using Maven
- com.jalios.ejpt : This is the main plugin. It used the sync library
- com.jalios.ejpt.feature : This is the feature plugin
- com.jalios.ejpt.site : This is the update site plugin

Compile the sync project using maven. You can lauch it from command line, or use the Eclipse project context menu "Run As / Maven install"

You then need to copy the jar generated in the target folder (the one with the "with-dependencies" prefix) into the root folder of the 
"com.jalios.ejpt" project. This will make you replace an existing jar.

Open the site.xml file present in the "com.jalios.ejpt.site" plugin, and click the "Build All" button. The update site will be generated in the same folder.

You can zip the content of the "com.jalios.ejpt.site" folder (excluding the Eclipse .project file) and distribute it as a standard Eclipse Update Site.

# Installation

From a stock Eclipse Oxygen, use the menu "Help / Install new software". 

Click the "Add" button to add a new location :

- Name it "Ejpt"
- Add a new location that points to the zip file (if using the "Archive" button), or to the "com.jalios.ejpt.site" project (if using  the "Local" button").

Click finish, and follow the wizard...

Once Eclipse is restarted, you can check the the plugin have been made available by looking at the "Jalios Plugin" menu.

# Using the plugin

Jalios Community website is your friend here...