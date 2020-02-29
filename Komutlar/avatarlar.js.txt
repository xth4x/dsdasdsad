const Discord = require('discord.js');

exports.run = (client, message, args) => {
    
    let user;
    
    if (message.mentions.users.first()) {
      user = message.mentions.users.first();
    } else {
        user = message.author;
    }
    
    const avatar = new Discord.RichEmbed()
        .setColor("RANDOM")
        .setAuthor("» Fade City Profilin,")
        .setImage(user.avatarURL)
    message.channel.sendEmbed(avatar)
    
};

exports.conf = {
  enabled: true, 
  guildOnly: false, 
  aliases: ["pp"],
  permLevel: `Yetki gerekmiyor.` 
};

exports.help = {
  name: 'Profil',
  category: 'kullanıcı',
  description: 'Belirtilen Kişinin veya Komutu Yazan Kişinin Profilini Atar.',
  usage: '+profil <@kişi-etiket> veya +profil'
};