import pandas as pd

# Загружаем набор данных
data = pd.read_csv('photochat_dataset.csv')

# Извлекаем диалоги и изображения
dialogs = data['dialog']
images = data['image_link']

# Создание словаря
dialog_image_dict = {}
for i in range(len(dialogs)):
    dialog = dialogs[i]
    image = images[i]
    

# Код будет идти сюда
import difflib

user_response = "User's response goes here"  # Заменить ответом пользователя
# Найди наиболее подходящюю реплику в базе данных
most_similar_replica = difflib.get_close_matches(user_response, dialogs, n=1)
data = pd.read_csv('./photochat_dataset.csv')
import requests

# Настроить персональный доступ
headers = {
    'Authorization': 'token your_personal_access_token'
}

# Отправь cсылкe на картинку
comment_data = {
    'body': f'![Image]({image_link})'
}

response = requests.post('https://api.github.com/repos/{owner}/{repo}/issues/{issue_number}/comments', json=comment_data, headers=headers)

# Возможность отреагировать пользователю на картинку
emoji_reactions = ['+1', 'heart']
for emoji in emoji_reactions:
    reaction_response = requests.post(f'https://api.github.com/repos/{owner}/{repo}/issues/comments/{response["id"]}/reactions/{emoji}', headers=headers)

if most_similar_replica:
    print(f"The most similar replica to the user's response is: {most_similar_replica[0]}")
    # Now you can retrieve the image link corresponding to this replica from the dialog_image_dict
    if most_similar_replica[0] in dialog_image_dict:
        image_link = dialog_image_dict[most_similar_replica[0]]
        print(f"The corresponding image link is: {image_link}")
    else:
        print("No image link found for the most similar replica")
else:
    print("No similar replica found in the dataset")
# Assume image_link contains the URL of the found image
# Write a command to send the image to the user
send_image_to_user(image_link)

import requests

# Set up your Yandex Metrica API key
api_key = 'your_api_key'

# Define the event parameters
event_params = {
    'event_name': 'test_event',
    'data': {
        'param1': 'value1',
        'param2': 'value2'
    }
}

# Send the event
response = requests.post(f'https://api-metrica.yandex.net/management/v1/counter/{api_key}/events', json=event_params)

# Check the response
if response.status_code == 200:
    print("Event sent successfully")
else:
    print(f"Failed to send the event. Status code: {response.status_code}, Error message: {response.text}")
