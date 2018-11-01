# Container for bitlbee
Run it by using
```
docker run --rm -it -e BITLBEEPORT='1337' -p 1337:1337 -v $(pwd)/config:/config bitlbee
```

# Managing accounts
## Facebook
### Connecting to Facebook
I recommended that you use an app password for your Facebook account.
```
> account add facebook <email> <password>
> account facebook on
```
### Adding Facebook chats
For adding an existing Facebook chat use
```
> chat add facebook <id> #<channelname>
> /join #<channelname>
```
<id> is the ID of the chat and can be found by opening the chat on the [Messenger.com](https://www.messenger.com/) and coping  the numeric value following https://www.messenger.com/t/

## Slack
### Connecting to slack
```
> account add slack <yourusername>@<whatever.slack.com> <apitoken>
> account slack on
```
The token can be found at https://api.slack.com/custom-integrations/legacy-tokens
### Adding Slack chats
```
> chat add slack <chatname>
> /join #<chatname>
```
