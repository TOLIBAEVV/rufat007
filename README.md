from aiogram import types,Bot,Dispatcher,F
from aiogram.filters import Command
import asyncio
import logging
#type

api = '7855597648:AAErdPu6O5cGC0LZLZ0WpTsVOtVnGWgfTIg'
bot = Bot(api)
dp = Dispatcher()

@dp.message(Command('start','basla'))#if command=='/start' or command=='/basla':
async def send_hi(sms:types.Message):
    await sms.answer(text='salem bizin botimizga xosh keldiniz')

@dp.message(Command('help'))
async def send_hi(sms:types.Message):
    await sms.answer(text='sizge jardemim  kerekpe')

@dp.message(Command('info'))
async def send_hi(sms:types.Message):
    await sms.answer(text='bul bot sizdin sorawlarinizga juwap beredi')


async def main():
    await dp.start_polling(bot)


if __name__=='__main__':
    logging.basicConfig(level=logging.INFO)
    asyncio.run(main())



