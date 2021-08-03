# table of contents

1. [introduce-some-commands-in-LINUX](#introduce some commands in LINUX)
    1. [cd](#cd)
    2. [ls](#ls)
    3. [mkdir](#mkdir)
    4. [touch](#douch)
    5. [vim](#vim)
    6. [cat](#cat)
    7. [rm](#rm)
    8. [ps](#ps)
    9. [terminal-commands-in-python-script](#if you want to run terminal commands in python script)

# introduce some commands in LINUX 
some easy and usefull commands
## cd
    cd command directed you to  a path
    $cd /user/.... filename
    $cd .. (return parent cataloge)

## ls 
    ls+filename can check how many files are in current path
    $ls
## mkdir
    mkdir+file build a file 
    $mkdir test_touch
## touch
    touch+file build a new file
    $touch touch.txt
## vim
    use vim open a file,$ vim filename
    $vim touch.txt
    i:insert
    esc:back off the insert module
    :q(quit without save) +enter
    :wq(quit and save the result) +enter
## cat
    cat filename can check the content in the file
    $cat touch.txt
## rm
    remove file
    
    $ sudo rm file -r

    $ rm -rf file


## ps(process status)

    ps -ef | grep python (display the list of running processs in python)

    pkill python (kill all the python program

    pkill -f pii_api.py (kill the *.py)

## if you want to run terminal commands in python script

    by using: import os
    os.sys('your python commands') eg: os.sytem('ps -ef | grep python')





    
