## Tutorial on how to use screen

1. To start a screen with a named session ``screen -S session_name``
2. To detach a screen `ctrl+a d`
3. To attach to a screen `screen -r session_name`
4. To see the list of screens `screen -ls
5. To kill a screen `screen -X -S <screen_id> quit`
6. To detach from current screen `screen -d`


### Split screen (Ubuntu)

- To split vertically: `ctrl a` then `|`
- To split horizontally: `ctrl a` then `S`
- To unsplit: `ctrl a` then `Q`
- To switch from one to another: `ctrl a` then `tab`
- After splitting, you need to go the new region and activate it using `ctrl a` then `c`

For more screen commands, visit [this stack exchange post](https://unix.stackexchange.com/questions/7453/how-to-split-the-terminal-into-more-than-one-view).
