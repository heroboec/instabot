# Как использовать
** Важно! Прочитайте инструкцию от начала до конца, а затем действуйте! Удачи! **
## Как работать? ##
Вам понадобится скачанный проект. В папке *** instabot/examples/ *** находятся скрипты для работы
## Как запустить скрипт? ##
Откройте командную строку, при помощи команды *** cd *** перейдите в каталог проекта, а именно *** instabot/examples ***. 
Наберите 
``` python 
python name.py param
```
где *** name *** – название скрипта, *** param *** – необходимый параметр для запуска скрипта. Не для всех скриптов нужен аргумент
## Как я могу узнать для какого скрипта необходим входной параметр? ##
Запустите скрипт, набрав 
``` python
python name.py
```
Скрипт остановится, если нет необходимых параметров и даст вам об этом знать.
Пример. 
Запускаем скрипт 
``` python
python like_hashtags.py. 
``` 
Скрипт останавливается и выводит нам сообщение: 
``` python
error: the following arguments are required: hashtags.
```
То есть мы должны были вести хештеги. 
Правильный пример: 
``` python
python like_hashtags.py follow
```
## Всё включено
*** multi_script_CLI.py *** – скрипт, который содержит все функции. При первом его запуске вам будет предложено настроить скрипт. Настройки скрипта хранятся в файле *** setting.txt ***.
Также будут созданы файлы: *** hashtag_file.txt, users_file.txt, whitelist.txt, blacklist.txt, comment.txt ***.
## 24/7
Да, есть скрипт, который круглосуточно фолловит подписчиков и подписки определенных людей, а также лайкать фотографии по хэштегам и фотографии людей. Все это позволяет скрипт - *** ultimate.py ***, который находится в папке *** /instabot/examples/ultimate/ ***. В папке также находятся другие текстовые файлы для работы скрипта. В этих файлах каждый новый параметр нужно писать с новой строки.
## График работы
Также есть скрипт, который будет работать круглосуточно, НО этот скрипт будет действовать по плану. Этот скрипт – *** ultimate.py *** в папке *** /instabot/examples/ultimate_schedule/ ***. Вы можете открыть код любым редактором и поправить его – это будет легко, так как присутствуют комментарии в важных частях кода.
## Как правильно настроить скрипт
Для того, чтобы ваш аккаунт не был забанен - нужно настроить скрипт
Пример, допустим нам нужно лайкать фотографии по хештегу каждую минуту. Преждего всего время в секундах.
Откройте *** like_hashtags.py *** при помощи текстового редактора. Найдите такие строчки (примерно они так должны выглядеть)
``` python
bot = Bot()
bot.login(username=args.u, password=args.p,
          proxy=args.proxy)
```
Дальше в строке
``` python
bot = Bot()
```
нам нужно написать в скобках параметр. Этим параметром является *** like_delay ***. Этому параметру нужно присвоить значение 60, так как нам нужно, чтобы каждую минуту лайкал фотографию по хештегу.
В итоге это будет выглядеть вот так
``` python
bot = Bot(like_delay=60)
bot.login(username=args.u, password=args.p,
          proxy=args.proxy)
```
### Список параметров

| Параметр| Описание | Пример |
| ------------- |:-------------:| ------:|	
| proxy | Proxy for Instabot | None|	
| max_likes_per_day| How many likes the bot will perform per day| 1000|
| max_unlikes_per_day | How many medias the bot will unlike in a day| 1000|	
| max_follows_per_day| Max number of follow per day| 350|
| max_unfollows_per_day| Max number of follow per day| 350|
| max_comments_per_day| Max number of comments per day| 100|
| max_likes_to_like| If the media has more likes then this value - it will be ignored and not be liked | 200|
| filter_users | Filter users if True | True|
| max_followers_to_follow| If the user has more followers than this value - the user will not be followed or liked. | 2000|
| min_followers_to_follow| If the user has fewer followers than this value - the user will not be followed or liked.| 10|
| max_following_to_follow| If the user has more followings than this value - the user will not be followed or liked.| 10000|
| min_following_to_follow| If the user has fewer followings than this value - the user will not be followed or liked.| 10|
| max_followers_to_following_ratio| if the user's followers/following is greater than this value - the user will not be followed or liked.| 10|
| max_following_to_followers_ratio| if user's following/followers is greater than this value - he will not be followed or liked.| 2|
| min_media_count_to_follow| If the user has fewer media count than this value - the user will not be followed. | 3|
|max_following_to_block|If the user have a following more than this value - the user will be blocked in blocking scripts because he is a massfollower| 2000|
| max_likes_to_like | Max number of likes that can media have to be liked | 100 |
| like_delay | Delay between likes in seconds| 10|
| unlike_delay | Delay between unlikes in seconds | 10|
| follow_delay | Delay between follows in seconds| 30|
| unfollow_delay | Delay between unfollows in seconds| 30|
| comment_delay | Delay between comments in seconds|  60|
| whitelist | Path to the file with users that shouldn't be unfollowed| "whitelist.txt"|
| blacklist | Path to the file with users that shouldn't be followed, liked or commented | "blacklist.txt"|
| comments_file | Path to the comments database | "comments.txt" |
| stop_words| A list of stop words: don't follow a user if they have any of these stop words in their description| ['shop', 'store', 'free']|



