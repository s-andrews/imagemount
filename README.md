# ImageMount

This is an implementation of a FUSE filesystem layer which provides controlled access to data under a root-only accesible mount point to a set of users on a cluster (or other unix system).

The system is fairly simple in that it is configured by a file which simply maps usernames to top level directories in the common mount point and then makes those folders selectively visible on the FUSE mount point.

This was written specifically for usage on our cluster, but in theory it should work for any other system where you want to provide managed access to a folder based on simple name based rules in the top level folders.

