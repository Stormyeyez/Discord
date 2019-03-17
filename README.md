const Discord = require("discord.js");
const client = new Discord.Client();
 
client.on("ready", () => {
  console.log("I am ready!");
});
 
let prefix = "~";
client.on("message", (message) => {
  if (message.author.id === client.user.id || message.author.bot) return;
  let args = message.content.split(" ").slice(1);
  if (message.content.startsWith(prefix + "ping")) {
    message.channel.send("pong!");
  }
});
 
client.login("SuperSecretBotTokenHere");
