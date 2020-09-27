import tweepy
import os
def create_api():
   consumer_key = os.getenv('consumer_key')
   consumer_secret = os.getenv('consumer_secret')
   access_token = os.getenv('access_token')
   access_token_secret = os.getenv('access_token_secret')
   auth = tweepy.OAuthHandler(consumer_key, consumer_secret)
   auth.set_access_token(access_token, access_token_secret)
   api = tweepy.API(auth,wait_on_rate_limit= True,wait_on_rate_limit_notify=True)
   api.verify_credentials()
   print('API Created')
   return api
   def followers_count(user):
      emoji_numbers = {0:"0️⃣",1:"1️⃣",2:"2️⃣",3:"3️⃣",4:"4️⃣",5:"5️⃣",6:"6️⃣",7:"7️⃣",8:"8️⃣",9:"9️⃣"}
      followers_split = [int(i) for i in str(user)]
      followers_in_emoji = [emoji_numbers[j] for j in followers_split if j in emoji_numbers.keys()]             
      print(followers_in_emoji)
import time
def followers_count(user):
      emoji_numbers = {0:"0️⃣",1:"1️⃣",2:"2️⃣",3:"3️⃣",4:"4️⃣",5:"5️⃣",6:"6️⃣",7:"7️⃣",8:"8️⃣",9:"9️⃣"}
      followers_split = [int(i) for i in str(user.followers_count)]
      followers_in_emoji =''.join([emoji_numbers[j] for j in followers_split if j in emoji_numbers.keys()])             
      return followers_in_emoji

api = create_api()
while True:
    user = api.get_user('SasmithaRajave1')
    print(user)
    api.update_profile(name =  f'Sasmitharajavelu|{followers_count(user)} Followers')
    print(f'updating twitter name = Sasmitharajavelu {followers_count(user)} Followers')
    print('waiting to refresh')
    time.sleep(60)                      
