# -drshox_ai_bot

from telegram import Update
from telegram.ext import Updater, CommandHandler, CallbackContext

TOKEN = "8487690379:AAE1DBfQnAs9TzUora43zdwL5npe2E8RYFQ"

def start(update: Update, context: CallbackContext):
    update.message.reply_text("Salom! Bot ishlayapti ✅")

def main():
    updater = Updater(TOKEN)
    dp = updater.dispatcher
    dp.add_handler(CommandHandler("start", start))
    updater.start_polling()
    updater.idle()

if __name__ == "__main__":
    main()
