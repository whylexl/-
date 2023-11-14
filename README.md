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
