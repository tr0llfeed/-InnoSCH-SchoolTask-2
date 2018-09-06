var translate = require('yandex-translate')('token');
const TelegramBot = require('node-telegram-bot-api');
const token = 'token';
const bot = new TelegramBot(token, {polling: true});


bot.on('message', (msg) => {
 var chatId = msg.chat.id;
 var text = msg.text;
 var uname = msg.from.username;
 console.log(uname+": "+text);
    
    
 translate.translate(text, { from:'ru', to: 'tt' }, function(err, res) {
    console.log("Answer to "+uname+": "+res.text);
    return bot.sendMessage(chatId, ""+res.text);
 });    

});
