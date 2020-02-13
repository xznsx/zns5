print("""          [Hi Bro To My Program]          """)

    import time

    from instabot import Bot
    choese = input("""
    1 - whatch Your Following
    2 - Whatch User In File
    3 - Whatch Pages User Story's 
    
    input :""")
    if choese == "3":
     
     
   import requests
   import time
   def get_id(username):
       url = "https://www.instagram.com/web/search/topsearch/?context=blended&query=qnpk&rank_token=0.3953592318270893&count=1"
       response = requests.get(url)
       respJSON = response.json()
       try:
           user_id = str(respJSON['users'][0].get("user").get("pk"))
           return user_id
       except:
           return "Unexpected error"
   lineList = [line.rstrip('\n') for line in open("users.txt")]
   from instabot import Bot
   o = 1
   bot = Bot()
   user_name = input("Input Your User Name :")
   password = input("Input Your Password :")
   bot = bot.login(username=user_name, password=password)
   tr = int(input("Input Your Time sleep:"))
   for user in lineList:
       link = "https://gramho.com/followers/"+user
       re = requests.session()
       site = re.get(link)
       o = str(site.text)
       for i in o :
           if "@" in i :
               user=str(i.split("@")[1]).split("</span>")[0]
               if "h1" in user:
                   continue
               else:
                   user_id = get_id(user)
                   bot = Bot()
                   story = bot.watch_users_reels(user_id)
                   if story == False:
                       print("Sorry Im Pand :( ")
                       break
                   if story == True:
                       print(str(o)," => ",user)
                   if o == 50:
                       o = 0
                       time.sleep(10)
                   time.sleep(tr)
                   o+=1 
    if choese == '1':
        bot = Bot()
        username = input('input your user Login :')

        password = input('Enter your password:')
        om = bot.login(username=username, password=password)
        if om == True:
            choes = str(input('Login Done Start (y,n) :'))
            tr = int(input('Input Time Sleep :'))
            if choes == 'y':
                omar = bot.following
                i = 1
                o = 1
                for user in omar:
                    r = bot.watch_users_reels(user)
                    o += 1
                    if o == 102:
                        o = 1
                        time.sleep(10)
                    if r == False:
                        print('im pande :( ')
                        break
                    else:
                        print(str(i) + ' => Done =>', user)
                        time.sleep(tr)
                        i += 1
        else:
            print('login error')
    if choese == '2':
        bot = Bot()
        username = input('input your user Login :')

        password = input('Enter your password:')
        om = bot.login(username=username, password=password)
        if om == True:
            choes = str(input('Login Done Start (y,n) :'))
            if choes == 'y':
                i = 1
                o = 1
                file_name = input('input file name :')
                tt = int(input('input time sleep :'))
                file = open(file_name,'r')
                for user in file:
                    r = bot.watch_users_reels(get_id(user))
                    o += 1
                    if o == 102:
                        o = 1
                        time.sleep(10)
                    if r == False:
                        print('im pande :( ')
                        break
                    else:
                        print(str(i) + ' => Done =>', user)
                        time.sleep(tt)
                        i += 1
