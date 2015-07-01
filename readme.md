Files in this directory:
- readme.md: This file
- demobuilder.xml
    The export file of the demobuilder application.
    The image file of this application is used as demobldr.img file in the demobuilder.zip archive.
- w4gldemo directory:
    Contains files to load the old-style "videos" application and required data.
    It is used in the PropertyChanger demo (see below).


Importing Quick Start
---------------------

Demobuilder is an OpenROAD application used for loading demo source code and
data. The steps below will import Demobuilder and then use Demobuilder to load
the Videos demo application and data.

The example below assumes a database name of `ordemo` which is remote and
accessed via a vnode (virtual node) called `vnode`. For example:

    sql vnode::ordemo

Demobuilder needs to be ran as the database administrator, that is, the owner
of the database ordemo.

Import demobuilder application into an application named `demobuilder`:

    w4gldev backupapp in vnode::ordemo demobuilder demobuilder.xml

Then run demobuilder:

    set II_W4GL_DEMO=w4gldemo
    rundbapp vnode::ordemo demobuilder

NOTE `set` is Windows specific.

   * Hit the "Load" button.

Then run Videos application:

    rundbapp vnode::ordemo videos



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

