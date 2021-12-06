(async () => {
    const Discord = require("discord.js");
    const Database = require("easy-json-database");
    const devMode = typeof __E_IS_DEV !== "undefined" && __E_IS_DEV;
    const delay = (ms) => new Promise((resolve) => setTimeout(resolve, ms));
    const s4d = {
        Discord,
        database: new Database(`${devMode ? S4D_NATIVE_GET_PATH : "."}/db.json`),
        joiningMember: null,
        reply: null,
        tokenInvalid: false,
        tokenError: null,
        checkMessageExists() {
            if (!s4d.client) throw new Error('You cannot perform message operations without a Discord.js client')
            if (!s4d.client.readyTimestamp) throw new Error('You cannot perform message operations while the bot is not connected to the Discord API')
        }
    };
    s4d.client = new s4d.Discord.Client({
        intents: [Object.values(s4d.Discord.Intents.FLAGS).reduce((acc, p) => acc | p, 0)],
        partials: ["REACTION"]
    });

    var arguments2, command;


    s4d.client.on('guildMemberAdd', async (param1) => {
        s4d.joiningMember = param1;
        s4dmessage.channel.send(String((s4d.joiningMember.guild.name)));
        s4dmessage.channel.send(String('YES ANOTHER HUMAN JOINED FINALLY!!!! But if it was a fellow bot then that\'s fine-'));
        s4dmessage.channel.send(String((s4dmessage.author.username)));
        s4d.joiningMember = null
    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        if ((s4dmessage.content) == '/ping') {
            s4dmessage.channel.send(String('How dare you ping me son of a child- '));
        }

    });

    await s4d.client.login('OTE3MjUyMjY0OTYyNDQxMjc2.Ya1_vQ.VZfWetdKf7XBbHQK5z-dZRt0KrU').catch((e) => {
        s4d.tokenInvalid = true;
        s4d.tokenError = e;
    });

    s4d.client.on('guildMemberRemove', async (param1) => {
        s4d.leavingMember = param1;
        s4dmessage.channel.send(String('Guys someone decided to to jump off the window? 911? lol'));
        s4dmessage.channel.send(String((s4d.leavingMember.user.username)));
        s4dmessage.react(':place_of_worship:');
        s4d.leavingMember = null
    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/fish') {
            s4dmessage.channel.send(String('OI OI OI OI WHAT DO U WANT MEH TO SAY TO U LAHHHH????'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/cat') {
            s4dmessage.channel.send(String('Mannn cats are adorable- But I wish I can send you one :\'))'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/MAIKAAA') {
            s4dmessage.channel.send(String('@MaikaChat send help-'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/what_Fish?') {
            s4dmessage.channel.send(String('Fish yesss.... FISHHHHHHHHHHHH AAHAHAHAHAHAHAHAHAHAHA FISHHHHHHHHHHHH THAT\'S ME'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/dog') {
            s4dmessage.channel.send(String('Hehe dogs lol'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/deathnote') {
            s4dmessage.channel.send(String('WHY WOULD YOU DO THIS WHYYY'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/gold') {
            s4dmessage.channel.send(String('Piglin went to steal gold ingot '));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/iron') {
            s4dmessage.channel.send(String('*Iron Golem Killed you* FATALITY '));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/doublefish') {
            s4dmessage.channel.send(String('BOOP beep Bleep FISH!'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });

    s4d.client.on('messageCreate', async (s4dmessage) => {
        arguments2 = (s4dmessage.content).split(' ');
        command = arguments2.splice(0, 1)[0];
        if (command == '/diamonds') {
            s4dmessage.channel.send(String('WOOOOOOOOOOOHOOOOOOOOOO DIAMONDS LETS GOOOOOOO'));
            s4dmessage.channel.send(String((arguments2.join(' '))));
        }

    });


    return s4d;
})();
