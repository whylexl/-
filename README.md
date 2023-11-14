<!-- Yandex.Metrika counter -->
<script type="text/javascript" >
   (function(m,e,t,r,i,k,a){m[i]=m[i]||function(){(m[i].a=m[i].a||[]).push(arguments)};
   m[i].l=1*new Date();
   for (var j = 0; j < document.scripts.length; j++) {if (document.scripts[j].src === r) { return; }}
   k=e.createElement(t),a=e.getElementsByTagName(t)[0],k.async=1,k.src=r,a.parentNode.insertBefore(k,a)})
   (window, document, "script", "https://mc.yandex.ru/metrika/tag.js", "ym");

   ym(95558985, "init", {
        clickmap:true,
        trackLinks:true,
        accurateTrackBounce:true
   });
</script>
<noscript><div><img src="https://mc.yandex.ru/watch/95558985" style="position:absolute; left:-9999px;" alt="" /></div></noscript>
<!-- /Yandex.Metrika counter -->

import logging
from aiogram import Bot, Dispatcher, types
from aiogram.utils.markdown import h2, h3, bold, italic, code
from string import Template

logging.basicConfig(level=logging.INFO)
bot = Bot("BOT_TOKEN")
dp = Dispatcher(bot)

@dp.message_handlers(content_types=['text'])
async def process_text_messages(message: types.Message):
    if message.text.lower() == 'Приветик!':
        await message.answer("Привет! Я твой новый друг Тинь. Вместе со мной ты узнаешь много нового о финансовой грамотности)")
    elif message.text.lower().startswith('Тинь'):
        await bot.send_message(message.from_user.id, f'Привет! Как я могу тебе помочь?')
    elif 'привет' in message.text:
        await message.reply("Привет!")
    else:
        await message.
{
   "диалог" :[
    {
      "share_photo" : " Логическое значение, обозначающее, была ли фотография опубликована в этом ходе. " ,
       "user_id" : " 0 или 1. Идентификатор пользователя этого хода. " ,
       "message" : " Текст одного хода разговора. Пусто, когда Share_photo это правда » .
    }
  ],
  "dialogue_id" : " Целое число. Уникальный идентификатор диалога. " ,
   "photo_description" : " Строка. Описание фотографии. Включает информацию о метках объектов на фотографии. " ,
   "photo_url" : " URL фотографии. "
  "photo_id" : " Идентификатор изображения фотографии в открытом наборе данных изображений. "
}
