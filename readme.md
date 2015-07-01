Files in this directory:
- readme1st.txt: This file
- demobuilder.zip:
    The archive containing files to load the old-style "videos" application and required data.
    It is used in the PropertyChanger demo (see below).
- demobuilder.xml
    The export file of the demobuilder application.
    The image file of this application is used as demobldr.img file in the demobuilder.zip archive.


PropertyChanger Demo
--------------------

1. In your Ingres DBMS installation: Make sure you have a for your use.
   If not done already, create a database, e.g. "createdb videos" for creating a "videos" database.
2. Install the demobuilder into your existing OpenROAD 6.2 installation:
   Copy the "ingres" sub-directory from the demobuilder.zip into the OpenROAD 6.2 %II_SYSTEM% directory.
   This will add files/directories to the existing one.
3. Launch an OpenROAD Command Window (from the "Actian OpenROAD 6.2" group in the Start menu).
4. Launch the "demobuilder.bat" script and follow the prompts to load the Videos application and the test data:
    - Enter the database (from step 1) and hit <OK>
    - Select the Videos application and hit <Load>
    - Check the Trace Window for success - hit <Close> afterwards.
5. Launch the OpenROAD Workbench and connect with a profile for the database used in the previous step
    - Create a new profile if you have none yet.
6. Test the Videos application.
   The Videos application has an old (Windows XP like) look & feel.
7. Use the PropertyChanger to modify the Videos application into Windows7 style.

