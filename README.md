# DomainAlerting
Daily alert when a new domain name is registered and contains your keywords.

## Description
DomainAlerting tool allows you to perform two main actions (for educational purposes only):

- ### Download newly registered domains
![image](https://user-images.githubusercontent.com/75697623/151710260-353f03a2-1b95-4e64-ba1d-6d611da8805a.png)

- ### Send automatic email alert
You can setup a wordlist and be alerted by email when you have a match (exemple here with "google|amazon").
![image](https://user-images.githubusercontent.com/75697623/151710269-3def8c7d-8db7-49b1-82fb-124bbb1865de.png)

## Prerequisite

```bash
apt install mailutils
pip3 install -r requirements.txt
```
## Configuration
Inside the file "launcher.sh", complete:
- Your keywords (Line 4: #Keywords to complete)
- Your receiver email (Line 5: #Email to complete)

Then, create a daily crontab job:
```bash
crontab -e #edit user's crontab
0 8 * * * /path/launcher.sh #set daily crontab (here at 8 am for example)
```

## Contributing
Feel free to clone this project. For major changes, please open an issue first to discuss what you would like to change.

## License
[MIT](https://choosealicense.com/licenses/mit/)
