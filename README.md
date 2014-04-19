JAR Class File Updater
======================

Command line executable JAR that patches an archive (WAR/JAR) file with patches found in a directory:

    ./patches

These patches can be class files or other resources.

This allows for the process of monkey patching an archive in a more controlled manner than unzipping
the archive, overwriting the file and rezipping the archive.

This also makes a backup of the archive it is patching.

n.b. This matches on resource name (rather than path) so an entry called Main.class in two different 
packages is treated as the same entry.  

This is currently interactive requiring the user to confirm the application of each patch

To run archive updater:

    java -jar archiveupdater.jar <name_of_archive_to_patch>


