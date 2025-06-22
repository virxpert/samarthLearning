# Copying Treasures

## Adventure 5: Duplicating with `cp`

After creating magic scrolls with the `touch` command, Tux and Ada were becoming quite good at navigating and creating things in Linuxland. But now they faced a new problem.

"Wizard Linus," said Tux thoughtfully, "I made a special scroll in my TuxTreasures folder, but now I want to share it with Ada without giving away my only copy. Is there a way to make a duplicate?"

"What an excellent question!" smiled the wizard. "In Linuxland, we use the `cp` command, which stands for 'Copy', to duplicate our scrolls and treasures."

"That sounds perfect!" said Ada. "How does it work?"

"Let's try it," replied the wizard. "First, let's go to Tux's treasure directory." He typed:

```bash
cd ~/TuxTreasures
```

"Now let's see what's here," continued the wizard:

```bash
ls
```

They saw all the scrolls they had created earlier.

"Let's copy the scroll_of_friendship to a new scroll called shared_friendship," suggested the wizard. He typed:

```bash
cp scroll_of_friendship shared_friendship
```

Then they checked to see if it worked:

```bash
ls
```

And there it was! A new scroll called "shared_friendship" appeared alongside the original!

"It worked!" cheered Tux. "Now I can share my scroll with Ada but still keep my original!"

## Copying to Different Places

Just then, Firefox bounded up with an excited look in his eyes.

"I see you're learning about copying," said Firefox. "But did you know you can also copy things directly to different places in Linuxland?"

"Different places? You mean different directories?" asked Ada.

"Exactly!" said Firefox. "You don't have to copy something to the same directory and then move it. You can copy it directly to where you want it to go!"

"That sounds very useful," said Tux. "How do we do that?"

"Let me show you," replied Firefox. "First, let's make sure Ada has a treasure directory of her own." He typed:

```bash
mkdir ~/AdaTreasures
```

"Now, let's copy Tux's scroll_of_wisdom directly into Ada's treasure directory," explained Firefox. He typed:

```bash
cp scroll_of_wisdom ~/AdaTreasures/wisdom_from_tux
```

"Notice that I gave it a new name in its new home," pointed out Firefox. "Let's check if it worked by looking in Ada's directory." He typed:

```bash
ls ~/AdaTreasures
```

And there it was! The scroll appeared in Ada's treasure directory with its new name.

"That's amazing!" exclaimed Ada. "I have my own copy now, with a special name to remember that it came from Tux!"

## Copying Entire Directories

As they were practicing copying scrolls, Owliver swooped down and perched nearby.

"I see you're getting good at copying individual scrolls," hooted Owliver. "But what if you wanted to copy an entire directory with all its contents?"

"Can we do that?" asked Tux, his eyes wide with wonder.

"Indeed you can," replied Owliver, "but you need to use a special flag with the `cp` command. It's the `-r` flag, which stands for 'recursive'."

"What does 'recursive' mean?" asked Ada.

"It means that the command will go into all the folders within folders, copying everything it finds," explained Owliver. "Let me show you." He typed:

```bash
mkdir ~/TuxTreasures/SecretCollection
touch ~/TuxTreasures/SecretCollection/rare_gem.txt
touch ~/TuxTreasures/SecretCollection/ancient_map.png
```

"I've created a directory with some special treasures inside," said Owliver. "Now let's copy the whole collection to Ada's treasures." He typed:

```bash
cp -r ~/TuxTreasures/SecretCollection ~/AdaTreasures/
```

"Now let's check if it worked," continued Owliver. He typed:

```bash
ls ~/AdaTreasures/
```

They saw "SecretCollection" in the list. Then they looked inside:

```bash
ls ~/AdaTreasures/SecretCollection/
```

And there were all the treasures, perfectly copied!

"That's incredible!" exclaimed Tux. "We copied a whole collection of treasures at once!"

## Preserving Special Powers with `-p`

Wizard Linus stepped forward with a thoughtful expression. "There's one more important thing about copying that you should know," he said.

"What's that?" asked Ada.

"Sometimes scrolls have special powers—permissions that control who can read them or change them," explained the wizard. "When you copy a scroll, these special powers might not get copied unless you use another special flag: `-p`, which stands for 'preserve'."

"Let me show you," continued the wizard. He typed:

```bash
cp -p scroll_of_courage ~/AdaTreasures/courage_preserved
```

"This copies the scroll and preserves all its special powers exactly as they were in the original," explained the wizard.

"And we can combine flags too," added Firefox. "If we want to copy a directory recursively AND preserve all the special powers, we can use:"

```bash
cp -rp ~/TuxTreasures/SecretCollection ~/AdaTreasures/SpecialPowersCollection
```

"Linuxland is so clever!" said Tux. "There are so many magical combinations to do exactly what we want!"

## Practice Challenge: The Great Library Exchange

Now it's your turn to copy treasures in Linuxland! Open your terminal and try these commands:

1. Make sure your castle from the previous adventure is ready:
   ```bash
   cd ~/LinuxCastle
   ```

2. Create a new directory for shared scrolls:
   ```bash
   mkdir SharedLibrary
   ```

3. Copy a scroll from your TowerRoom/Library to the SharedLibrary:
   ```bash
   cp ~/LinuxCastle/TowerRoom/Library/adventure.txt ~/LinuxCastle/SharedLibrary/
   ```

4. Create a collection of scrolls and copy the whole collection:
   ```bash
   mkdir ~/LinuxCastle/TowerRoom/Library/MagicCollection
   touch ~/LinuxCastle/TowerRoom/Library/MagicCollection/spell1.txt
   touch ~/LinuxCastle/TowerRoom/Library/MagicCollection/spell2.txt
   cp -r ~/LinuxCastle/TowerRoom/Library/MagicCollection ~/LinuxCastle/SharedLibrary/
   ```

5. Verify your copies with `ls`:
   ```bash
   ls ~/LinuxCastle/SharedLibrary/
   ls ~/LinuxCastle/SharedLibrary/MagicCollection/
   ```

**Bonus Challenge**: Copy a scroll to three different places in your castle with different names in each place! For example, copy a scroll called "magic_spell.txt" to the GreatHall, Garden, and TowerRoom, but with different names in each location.

## What's Next?

In our next adventure, Tux and friends will learn how to move and rename their scrolls and treasures with the `mv` command!

[Click here to continue to the next adventure: Moving Things Around](06-moving-things-around.md)
