# example-code
example code for Baltic bot in discord.js-command
~Code below~
-----------------
const commando = require('discord.js-commando');

class DiceRollCommand extends commando.Command {
  constructor(client) {
    super(client, {
      name: 'roll',
      group: 'random',
      memberName: 'roll',
      description: 'rolls a die',
    });
  }

  async run(message, args) {
    var roll = Math.floor(Math.random() * 6) + 1;
    message.channel.send("You rolled a " +roll);
  }

}

module.exports = DiceRollCommand;
