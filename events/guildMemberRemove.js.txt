module.exports = member => {
  let guild = member.guild;
  member.send('Görüşürüz');
  guild.defaultChannel.sendMessage(`${member.user.username} gitti.`);
};
