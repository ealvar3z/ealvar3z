## For all noobs who want to know

Ever wondered the semantics behind this fork bomb?

`:() { : | : & }; :`

## Steps:
========
1. we call colon
1. we pipe back to colon
1. run colon in the `bg`
1. finally call colon

And this process of putting the `:` function in the background and calling it
again, creates the fork bomb!

And now you know!
