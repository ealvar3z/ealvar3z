## Thursday, April 22, 2021, 2:01:24AM EDT <1619071284>

### Interesting facts about Bash

```
* Network connections can happen without external
  utilities.

  It supports network connections via two virtual device
  directories it "creates" in '/dev/'. 

  '/dev/tcp/host/port' and '/dev/udp/host/port'.

  This is a crazy feature for a shell to have. I haven't seen
  them widely used either.

* When something is run asynchronously in bash with '&', it
  runs in a subshell (a second bash process).

  What this means is that the async code cannot communicate
  with the blocking code. Therefore, variables get set in the input loop
  and once multiple loops are running, they won't be visible in the async
  listener loop. For example:

  One can utilize files for IPC between the two. The current channel can 
  communicate by maintaining a symlink and checking its target where needed.

  Example: .c -> '#current_channel'


