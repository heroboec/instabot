# auto_post
Allows you to post photos regularly from the local folder

## How to run
Run the script
```
python auto_post.py
```

## Settings
- photos are stored in _pics_ folder
- name of the photo should look like "# Caption text.jpg"
  - #(number) determines posts ordering
  - "Caption text" is what you will see under your photo in IG
  - Only _jpg_ files are processed
- list of posted photos stored in _pics.txt_ (in order not to post one photo several times)
- frequency of posting is determined by
```
timeout = 24*60*60 # 24 hours
```

___
_by @ppleskov_
