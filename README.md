# Persona 2: Eternal Punishment (PSP) [NPJH50581]

## About 

This is not exactly a traditional fan translation. This is a edited port of the official PSX translation.  Tatsuya's scenario's translation was used with permission from Strange Shrimp and Ohseki Ayu. 

## How to apply

You need a copy of the game in ISO format. Download and extract the p2ep_en_v1.0.zip file. Then, simply drag the ISO onto patcher.exe and wait for it to complete. Alternatively, you can pass the ISO as the first and only argument on the command line. During patching, about 1GB of extra space will be used. The original ISO is not modified. This patch has been tested on PPSSPP, PSVITA and PSP.

## Patcher

The patcher uses code from PPSSPP in order to decrypt the eboot.bin. Additionally, https://github.com/wmltogether/CriPakTools was used as a reference for the cpk code. xdelta3 is used for patching the files. The complete source code is available in patcher_src.zip

## FAQ

#### I'm used to the PSX version of the game, what's changed?

A lot.  Way too much to list here.  The good news is, we wrote it all down and included it in this handy [guide](P2EP%20guide.pdf). 

#### I really disagree with some of the localization decisions you made, can you change it?

No, we don't plan on changing anything aside from fixing bugs and typos.  However, we plan on releasing our tools so you can!  We need time to clean them up and make them easier to use by other people.  We will announce when they are ready, or feel free to check back here later.

#### I'd like to translate this to \<language\>, can you help me?

Yes, once the tools are released, they can be used to translate the game as well.  Depending on the language, some extra work might be needed on the programming side, since currently the tools support the basic Latin script and some diacritics. We also have plans to support Innocent Sin translations using the same toolset.

#### Why is the ISO half the size after patching?
The original ISO contains an encrypted copy of most of the game data as Install Data.  On UMD based games, there is an option copy this file to your PSP Memory Stick to reduce load times.  For ISOs that are already on the Memory Stick, this is completely unnecessary.  Removing it saves quite a bit of space.

#### I've played the Japanese version of the game, is there anything I should know?
The saves between the two games are fully compatible!  However, this includes Tatsuya's name, which will not be translated to english unless you start a new game or import from an english based Innocent Sin.  Additionally, if you have previously used the Install Data feature, you will need to remove the Install Data from your PSP or the game will crash.  When Install Data is present on the Memory Stick, the game will prefer it to the contents of the ISO, and because the game is patched it will crash.  

#### I want to import my save from Innocent Sin, how do I do that?

If you played the US version, simply start a new game and you will be immediately prompted.  If you played the EU version, you will need to go to the config menu first, and toggle the IS Save region and then start a new game.  If you played the Japanese, you will need to use an unpatched ISO to import.  Once you get control of Maya, you can save and then load the save in the patched version.  The same caveats regarding Tatsuya's name still apply.

#### Why are the text boxes transparent? It's really hard to read! 

This is an emulator issue.  Update to the latest version of PPSPP (1.13) and it should be fixed.  This issue does not occur on console.  

#### The game crashes when I try to return personas in the Velvet Room.

Update to a newer version of PPSSPP.  

#### I don't use windows, how can I patch my game?

If you're on linux, the patcher should work with wine.  The source is also included in the zip file, so feel free to compile from source if you'd like.  I can also provide a linux binary if there's enough demand.  If you use Mac, you can also compile the patcher yourself, but we're unable to provide binaries at this point in time. 

#### I don't trust sketchy exe files on the internet.  How do I compile the patcher?

That's not a bad thing!  The source to the patcher is included in the zip file.  It's written in rust with some borrowed c code.  Make sure you have cargo and a c compiler installed, and then simply run `cargo build --release`.  The executable will be in target/release.  Copy it to the same folder as the dist folder and everything should work.

## Team

eiowlta - programming, image editing

Sayucchi - editing, testing, misc translation

DarTisD - additional programming, testing

## More Information

For more information on our changes, the game, maps and a full walkthrough see the PSP guide. The contact guide contains every demon's response to every contact should you need something more specific than the suggested contacts in the walkthrough.

## Acknowledgements

Game by Atlus, original translation by Atlus West, modified and reproduced without permission. 

Tatsuya's scenario translation from [p2px-scenario tumblr](https://p2px-scenario.tumblr.com/), modified and reproduced with permission. 

Special thanks to CJ Iwakura and his team.  This work does not contain any work produced by them but we thank them for the discussion and collaboration we had during early development.
