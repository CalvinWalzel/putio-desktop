# Putio Desktop Client

This program periodically checks a folder in your put.io account. It creates the same folder, file structure in your computer. Downloads are done with multiple connections and this makes it fast.

## How to use

```
./putio-desktop -oauth-token=XXXXXX \
                -putio-folder="Send Home" \
                -local-path=/Users/refik/putio-files \
                -check-minutes=15
                -callback=/Users/refik/filebot.sh \
                -remove-remote=true
```

### Options

- **-oauth-token** - You can get yours from [here](https://put.io/v2/oauth2/apptoken/1681).
- **-putio-folder** - The folder on put.io that will be watched for files. This folder has to be on the root of "Your Files".
- **-local-path** - The folder on your computer where the files on put.io will be downloaded to.
- **-check-minutes** - How regularly in minutes the folder on put.io should be checked. Defaults to 5 minutes.
- **-callback** - The path to a local executable that will be started once all downloads are done.
- **-remove-remote** - Whether the downloaded files should be deleted from put.io. Either `true` or `false`.

### A word from the maintainer (of this fork)
I've forked and modified this project because of my own requirements. I had no previous experience with go. If there are any issues with how I have modified the code or added features, feel free to open an issue or submit a PR to improve it. I'd love to learn from my mistakes :)

In general: PRs with new features are always welcome.


