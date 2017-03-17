# fancylists
A small tool for managing lists. It provides a double-end queue like interface
and can be used with other console utilities through pipes.

### Example
Assume that we have some program named producer and when it's executed it
produces some URLs that we want to pass to `wget`. Assume that we have two
`cron` jobs; one of them executes the following command (which appends produced
URLs to the list named _downdloads_):
`producer | fl downloads -a`
and the other one passes the list to `wget` and clears it:
`fl downloads -lc | wget -i -`

### Interface
Fancylists supports double-end queue like interface. It means that it can be
used as a FIFO and LIFO data structure at the same time, which provides a
fine-grained control over the contents of a list.
