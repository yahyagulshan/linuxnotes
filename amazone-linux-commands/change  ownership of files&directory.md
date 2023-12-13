when we run the ls -la command it will show us the details about type of file and ownership

(-rwxrwxr-x 1 user user 89 mar 17 01:35) something like that.

below are file types and identifier

`file type               identifier`

`directory                   d`

`regular file                -`

`character device             c`

`Link                        l`

`socket file                 s`

`pipe                        p`

`block device                b`


these are permission of file `(-rwxrwxr-x)`

first, the file's owner is the character after the type of file. and the next three characters are known by the permission of the groups. and next are the permission for others.

below are the file permissions and their orbits

`Bit                      Purpose            Octoal Value`

`r                          Read                 4`

`w                          Write                2`

`x                          Execute              1`

for directory permission, the same orbit is used 

`Bit                      Purpose            Octoal Value`

`r                          Read                 4`

`w                          Write                2`

`x                          Execute              1`

`-                        No permission          0`


for change, the permission of file command is `chmod <permission> file`
permission can be changed by symbolic mod and numeric mode.

`chmod u+rwx "file name" `      -------------------- provide full access to Owner

`chmod ugo+r-x "file name"`   -------------------- provide read access to owner, group and others, remove execute access

`chmod o-rwx "file name"`      -------------------- remove all access for others

`chmod u+rwx,g+r-x,0-rws "test-file"` ------------- Full access for Owner, add read, remove execute for group and no access for others

for numeric mode

`chmod 777 test-file` ------------------------ provide full access to Owners, group and others

`chmod 555 test-file` ------------------------ provide read and execute access to owners, groups and others.

`chmod 660 test-file` ------------------------ provide read and write access for owner and group, no access for others.

`chmod 750 test-file` ------------------------ full access for owner, read and execute for group and no access for others.

how to change the ownership of groups

`chown owner:group filename`

`chown yahya:developer testfile `--------------------------- changes owner to bob and group to developer

`chown yahya andoid.apk` ----------------------------------- changes just the owner of the file to yahya.group unchanged

`chgrp android test-file` ---------------------------------- change the group for the test-file to the group called android.
