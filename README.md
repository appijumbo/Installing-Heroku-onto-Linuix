# Heroko Command Line Installation for Linux Ubuntu

* Go into the Downloads directory

```
cd ~/Downloads
```

* Check uname -m, find if X86_64 or X86; and make a note of it (assumed x64 for this description) 
```
uname -m
```

* get the x64 from the website url ie wget

```
wget https://cli-assets.heroku.com/heroku-cli/channels/stable/heroku-cli-linux-x64.tar.gz -O heroku.tar.gz
```

* extract the tarball
```
tar -xvzf heroku.tar.gz
```

* make sure parent directories exist, make them if they don't /usr/local/lib and /usr/local/bin no errors if exiisting

```
mkdir -p /usr/local/lib /usr/local/bin
```

* Now find the exact name of the file downloaded

```
find ~/Downloads -name heroku-cli*
```

* as superuser, move the 'heroku-cli-XXXXXX' file into /usr/local/lib/heroku
 
mv heroku-cli-XXXXXX /usr/local/lib/heroku
 
for example
 
```
 sudo mv heroku-cli-v6.13.12-c65a3c3-linux-x64 /usr/local/lib/heroku
 
```

( just ensure you have a space before /usr/local.lib/heroku)

8) Finally make a symbolic link

```
sudo ln -s /usr/local/lib/heroku/bin/heroku /usr/local/bin/heroku
```
