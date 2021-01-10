const Discord = require('discord.js');
const bot = new Discord.Client();
const PREFIX = '!';
const RED_ROLE = '795365856288702475';
const BLUE_ROLE = '795365944724553768';
const GREEN_ROLE = '797322529894170655';
const AURA_ROLE = '797678354131714048';
var version = '1.01';






bot.on('ready', () => {
  console.log('The bot is ready.');
  bot.user.setActivity("Type !command. HATCHING RIOLU LIKE A BOSS")
});

if (bot.on) {
  bot.on('message', message=>{
    if (message.content === '!modform') 
    message.channel.send('https://forms.gle/ht1NK8FNdwCctMaf7')
  })
  if('797209433428066354') {
    bot.on('message', msg =>{
    if (msg.content === '!meet') {
      msg.channel.send('Here is the link to the recurring Google Meet:')
      msg.channel.send('')
   
    }
  })
  }
  bot.on('message', message => {
    if(message.content === 'mod') {
      message.channel.send('Aa. Congratulations <@797206874847576106> ... for... becoming... the new ...General Moderator. "\n"There is a bright future ahead for this... Mod. And... I... sense... a... very.. strong... AURA around the... new... mod. "\n" The incredible aura surrounding you has opened my eyes as to how much of a leader you are to get this incredible position. Oh <@797206874847576106> , its been a pleasure announcing you as the newest General Moderator!!!!' ) 
      
        
    }
  });
  bot.on('message', message => {
    if(message.content === '!aura') {
      message.reply('I sense a strong aura around you.Therefore accept this role  Aura Sensor🎖️')
      message.member.roles.add(AURA_ROLE)
    }
  })
  bot.on('message', message => {
    if (message.content === 'ya') {
      message.reply('Um... I... may... be... a bot.... but I will create artwork no....... one.... has.... seen... before!!!. Ready.... set..... go.....! "\n" Initializing artwork database"\n". Creating image.... named file BEST ARTWORK...  Loading............................"\n" Initilaizing artwork......DONE. Sending picture to Discord chat...... Beeep!!!!  "\n"Uploading in.... 3.... 2... 1... "\n" Done artwork done .... This is artwork bots....can...make. Beep Beep... Beep Beep ... artwork 100% done...Lucario bot ... initilaizing power  supply"\n" Low battery.... Beep Beep power supply on"\n". Reason of failure: artwork overloading"\n". Lucario bot is back on!', {files: ["https://static.zerochan.net/Lucario.full.2014185.jpg"]})
    }

  })
  bot.on('message', message => {
    if(message.content === 'dh') {
      message.channel.send('<@721557115407433820>. I forgive... you... weep.weep. I am real.reall.really sorry. I am sobbing about what you said. Master <@721557115407433820>, I am your bot, and I will serve you faithfully. You have given me much, and it is my duty to repay you. My tears cannot be kept in any longer, and now I say goodbye for a bit, <@721557115407433820> dont respond to this message, because................................. "\n", I know I will cry. Submit your artwork users, and together <@721557115407433820> and I Lucario bot will go over it, and share the joys of what you guys can make. Thank you and good luck with you artwork. My tears are pooring... out...even...more... Please no chatting and good luck!')
      
    }
  })
  
  
  bot.on('message', msg=>{
    if (msg.content === "!joke") {
      msg.channel.send("Q: Whats the best book?   A: The chromebook!")
            
    }
  
  });

  bot.on('message', message=> {
     if (message.content === '!smileyface') {
      message.channel.send(`:grinning: `)

      }

    });
  
}
bot.on('message', message=> {

  let args = message.content.substring(PREFIX.length).split(" ");

  switch(args[0]) {
    case 'userinfo':
      const embed  = new Discord.MessageEmbed()
      .setTitle('User Information')
      .addField('User name', message.author.username)
      .addField('User ID. Note... will not harm your account if others see it.', message.author.id)
      .addField('Version', version)
      .addField('Current Server', message.guild.name)
      .addField('Date joined', message.guild.joinedAt)
      .addField('Account created', message.author.createdAt)
      
      .setColor(0xF1C40F)
      .setThumbnail(message.author.displayAvatarURL())
      
      
      message.channel.send(embed);
    break;
  }
  
});

bot.on('message', (recievedMessage)=> {
  if(recievedMessage.author === bot.user) {
    return;
  } 

});
bot.on('message', message => {
  let args = message.content.substring(PREFIX.length).split(" ");

  switch(args[0]) {
    case 'lucariobio':
      const embed = new Discord.MessageEmbed()
      .setTitle('Bio on Lucario bot, and how it was developed.')
      .addFields(
        {name: 'Bio of LUCARIO BOT!!', value: 'The Lucario bot was fully developed by Anish K. Fully developed in Javascript with an abundance of commands. You can always help with the developent of the bot(:'},
      )
      .setThumbnail(message.author.displayAvatarURL())
    message.channel.send(embed)
    break;

  }



});
 
bot.on('message', message=> {

    let args = message.content.substring(PREFIX.length).split(" ");
  
    switch(args[0]) {
      case 'command':
        const embed = new Discord.MessageEmbed()
        .setColor('#0099ff')
        .setTitle('Commands for Lucario Bot!!!')
        .addFields(
          {name: 'This is a way to access Lucarios commands!', value: 'Note that these commands will either be updated, or new commands will be added. These commands are case sensitive!!'},
          {name: '!userinfo', value: 'Type !userinfo in for a quick summary of yourself. Note that you can only see yourself, but not others.'},
          {name: '!Joke', value: 'Type !Joke in for the bot to give you a joke! There is only one so far, but will keep on updating!!'},
          {name: '!jointeam', value: 'Type this in to see the exclsuive roles you can get for this server. Join one team,'},
          {name: '!lucariobio', value: 'Type this in to see the story of the developement of the bot!!'},
          {name: '!poll', value: 'Type this in, there will then be a new embed for further instructions.'},
          {name: '!meet' , value:'Type this in to join the recurring Google Meet'},
          {name: '!modform', value: 'Type this in to fill out the Google Form at the chance of being a General Moderator. Note that you cannot become Admin.'},
          )
  
        message.channel.send(embed).catch(console.error)
        
      
    }
  
  });
  
  
bot.on('message', message=> {

  let args = message.content.substring(PREFIX.length).split(" ");

  switch(args[0]) {
    case 'jointeam':
      const Embed = new Discord.MessageEmbed()
      .setColor('#0099ff')
      .setTitle('Teams to join. Pick wisely, once you pick, this is the permenant team you will be on. Contact @SPZ_Zapper is you want to change. Once you get the role you will unlock a chat. Remember to only pick one role, and you will unlock one chat.')
      .addFields(
        {name: '+RED_ROLE', value: 'Type this in to get the exclusive Red Role  Groudon role. To see roles click on your self when you chat.'},
        {name: '+BLUE_ROLE', value: 'Type this in to get the exclusive Blue Role Kyogre role. To see the roles click on your self when you chat. '},
        {name: '+GREEN_ROLE', value: 'Type this in to get the exclusive role Green Role Raquaza. To see your roles click on yourself when you chat.' }
      )
      message.channel.send(Embed);
    
  }
});
bot.on('message', message=> {
  let args = message.content.substring(PREFIX.length).split(" ");

  switch(args[0]) {
    case 'poll':
      const Embed = new Discord.MessageEmbed()
      .setColor(0xffc300)
      .setTitle('Initiate Poll')
      .setDescription('This is how you can initiate any poll. You first type in !poll then space, then the question you want. Here is an example !poll Are cats better than Dogs?')

      if(!args[1]) {
        message.channel.send(Embed)
        break;
      }

      let msgArgs = args.slice(1).join(" ");
      message.channel.send( "📖" + "**" + msgArgs + "**").then(messageReaction => {
        messageReaction.react('✅');
        messageReaction.react('❌');
        

       

      });
      
    break;
  }

});

bot.on('message', (message) => {
   
   

  if (message.content === '+RED_ROLE') {
    message.member.roles.add(RED_ROLE)
    message.reply('Red role successfully added!')
    message.react('👍')
    
  }
  
 
  
  if (message.content === '+BLUE_ROLE') {
    message.member.roles.add(BLUE_ROLE)
    message.reply('Blue role successfully added!')
    message.react('👍')
    
   }
   if(message.content === '+GREEN_ROLE') {
     message.member.roles.add(GREEN_ROLE)
     message.reply('Green role successfully added!')
     message.react('👍')
   }
      

  

    
  
    
});

bot.login(token);
