module.exports = member => {
    let username = member.user.username;
    member.sendMessage('HoşGeldin ');
    member.guild.defaultChannel.send('hoşGeldin '+username+'');
};
