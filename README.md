EASY-LN
=======

This allows you to create links to arbitrary locations where the target is interpreted as relative to the current location. This differs from the default ln command, which interprets the target location as relative to the link.

The main benefit of this is the ability to navigate the filesystem using the shell features such as tab completion for *both* the link *and* the target.

Installation
------------

Clone the repository and put easy-ln in a folder on your path, or add the repository folder to your path.

This supports antigen installation.

Useage
------

As much as possible the useage matches the useage of ln. *The main difference is that this creates symbolic links*.

easy-ln [-T] TARGET    LINK_NAME (1st form)
easy-ln      TARGET              (1st form)
easy-ln      TARGET... DIRECTORY (1st form)
easy-ln -t   DIRECTORY TARGET... (1st form)

In the 1st form, create a link to TARGET with the name LINK_NAME. In the 2nd form, create a link to TARGET in the current directory. In the 3rd and 4th forms, create links to each TARGET in DIRECTORY. This will always create symbolic links.

This command is designed to make it easier to create links that are not in the current directory. When using the base ln command, the TARGET is always relative to the LINK_NAME. When using this command, the TARGET is always relative to the calling location.

Example:

    ln -s target folder/folder/link
    This will create a link to folder/folder/target.

    easy-ln target folder/folder/link
    This will create a link to target.

Currently this always creates absolute links. That may change in future.
