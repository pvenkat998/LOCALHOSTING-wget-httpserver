# LOCALHOSTING-wget-httpserver
Just readme

PREREQUISITES : 
install python 3
install wuget (2 options visual or source ) recommended visual

VISUAL WGET https://sites.google.com/site/visualwget/a-download-manager-gui-based-on-wget-for-windows

RAW WGET http://gnuwin32.sourceforge.net/packages/wget.htm


        just installing wget is not enough, so you have to make sure it can be called from cmd
SETTING UP WGET http://noahcoad.com/post/614/using-wget-on-windows


        OPTION 1 : run cmd from working dir (use cd to go to the place wget is extracted)
        OPTION 2 : Add the to wget bin directory to your system’s path directory (tutorial),
                    so you can run it easily from the command line. basically complicated stuff once for good future.
           


Step 1 :  setup local host using python(from the pc which has the files you want to share)

python install httpserver

python -m http.server

STEP 2 : open cmd in target pc(the pc where you want to receive the files)
type below command 
first one leads to it downloaded in wget folder
2nd one leads it to download to specified folder relative or absolute (if mentioned)

wget -r -np -nH --cut-dirs=3 -R index.html http://hostname/aaa/bbb/ccc/ddd/   
wget -r -np -nH --cut-dirs=3 -R index.html http://hostname/aaa/bbb/ccc/ddd/ -P target <<folder>> 
 
Example
wget -r -np -nH --cut-dirs=3 -R index.html http://hostname/aaa/bbb/ccc/ddd/ -P target C:\wgetdownloads\
