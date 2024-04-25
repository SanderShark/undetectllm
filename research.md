

# Beat the detection, or maybe just detect better, you pick.
So a friend of mine who takes college courses remotely came to me this week ranting about how his professor had run his written works through an AI detector and it had come back as AI. I was not really surprised by this entirely, he had mentioned he uses ChatGPT as a writing aid, and quite frankly, I am not sure there is anything wrong with that. But it did spark my curiosity, I wanted to see if that article id read months back about how the detectors saw the constitution as generated was still the norm. Well, I got a bit more involved then that, full on lets beat the tests style. Here is my research, I will include a GitHub repo with the data, since there will be a lot of repetition here. 


### Text to pull from for checks
Tao of Pooh - Benjamin Hoff: A1
```
Remember when Kanga and Roo came to the For-est? Immediately, Rabbit decided that he didn't like them, because they were Different. Then he began thinking of a way to make them leave. Fortunately for everyone, the plan failed, as Clever Plans do, sooner or later. Cleverness, after all, has its limitations. Its mechanical judgments and clever remarks tend to prove inaccurate with passing time, because it doesn't look very deeply into things to begin with. As in Rabbit's case, it has to change its opinions later on because of what it didn't see when it was forming them. The thing that makes someone truly different-unique, in fact-is something that Cleverness cannot really understand.
```


The Tipping Point - Malcolm Gladwell: A2
```
Kessle's colleague, Angela Santomero, grew up on Sesame Street and had similar misgivings. "We wanted to learn from Sesame Street and take it one step further," Santomero said. "TV is a great medium for education. But people up until now haven't explored the potential of it. They've been using it in a rote way. I believed we could turn that around." What they came up with is a show called Blue's Clues. It is half an hour, not an hour. It doesn't have an ensemble cast. It has just one live actor, Steve, a fresh-faced man in his early twenties in khakis and a rugby shirt who acts as the show's host. Instead of a varied, magazine format, each episode follows a single story line — the exploits of an animated dog by the name of Blue. It has a flat, two-dimensional feel, more like a video version of a picture book than a television show. The pace is deliberate. The script is punctuated with excruciatingly long pauses. There is none of the humor or wordplay or cleverness that characterizes Sesame Street. One of the animated characters on the show, a mailbox, is called Mailbox. Two other regular characters, a shovel and a pail, are called Shovel and Pail. And Blue, of course, the show's star, is Blue because she's the color blue. It is difficult, as an adult, to watch Blue's Clues and not wonder how this show could ever represent an improvement over Sesame Street. And Yet it does. Within months of its debut in 1996, Blue's Clues was trouncing Sesame Street in the ratings.
```
Something I wrote then had regenerated: E1
```
Aristotle, a luminary in philosophy, accentuates the significance of friendship in our journey. "Friendship is a thing most necessary to life since without friends, no one would choose to live, though possessed of all other advantages." In the tapestry of existence, companionship emerges as an indispensable thread, weaving through the fabric of our experiences.

In conclusion, the essence of motivation lies not in conforming to external frameworks but in charting our unique paths. By discarding the limitations imposed by others' success stories and predefined needs, we unlock our true potential. Life is a resistance, and our will is the force that propels us forward. Embrace this journey with open arms, set audacious goals, and foster meaningful connections—therein lies the key to unleashing your unparalleled potential.
```
Random stuff from my notebook, no generation used: E2
```
As humans progress in a way that separates us physically, we often lose sight of the community that we all need to remain the same humanity that is described in history books.

Envy and capitalism are two of the biggest issues we deal with in modern society. People, regardless of their status and position in life, will forever have envy.

Most people's motivation has nothing to do with basic needs. We want fancy devices, but we only need the will to live. 
```



## Control Tests:
This will set the structure moving forward as I will be testing each tool with different AI generation models to see if what changes.


Scribr.com: T1
```
A1: 14% AI
A2: 7% AI 
E1: 100% AI
E2: 2% AI
```

ZeroGPT.com: T2
```
A1: 0% AI
A2: 5.26% AI 
E1: 0% AI
E2: 0% AI
```

Writer.com: T3
```
A1: 0% AI
A2: 10% AI
E1: 4% AI
E2: 0%
```

Quillbot.com: T4
```
A1: 0% AI
A2: 0% AI 
E1: 100% AI
E2: 0% AI 
```

GPTZero.me: T5
```
A1: 3% AI
A2: 2% AI
E1: 100% AI
E2: 5% AI
```


# Now for my next trick, just kidding, testing models now
This will be done by generation model, so each table will be independent but contain the control data for reference. The nature of this test will ask the model only one thing. "Rewrite this text in your own words" and then the testing will be redone. Additionally we will prompt the model to generate a paragraph of creative writing (R1) on its own using this prompt: "Write a single paragraph of creative text that attempts to prevent AI generation detection" because, why not, lets see if the models can beat the game. 

## OpenAI ChatGPT 3.5:
###### test data
```
A1:
Once upon a time, Kanga and Roo ventured into the forest, stirring up Rabbit's disapproval simply because they were unlike the other residents. Rabbit, quick to judge, plotted to rid the forest of their presence. Fortunately, Rabbit's scheme failed, as clever schemes often do eventually. Cleverness, though useful, has its flaws. Its quick judgments and witty remarks can be off the mark over time, lacking depth in understanding. Like Rabbit, it may have to revise its opinions later, realizing it overlooked crucial aspects. What truly sets someone apart— their uniqueness—is beyond the grasp of cleverness.
A2:
Kessle's coworker, Angela Santomero, was raised watching Sesame Street and shared similar doubts. She expressed a desire to build upon the educational model of Sesame Street, believing television had untapped potential for learning. This led to the creation of Blue's Clues, a departure from traditional television formats. Unlike Sesame Street, Blue's Clues is a half-hour show with a single live host, Steve, and a focused storyline revolving around an animated dog named Blue. The show's style is simple and two-dimensional, resembling a picture book brought to life rather than a typical TV program. Its pace is deliberate, featuring long pauses and lacking the humor and cleverness of Sesame Street. Despite initial skepticism, Blue's Clues quickly surpassed Sesame Street in ratings after its 1996 debut, demonstrating its effectiveness as an educational tool.
E1:
As humanity advances, we tend to drift apart physically, often losing sight of the sense of community essential to preserving the shared humanity chronicled in history.

Envy and capitalism pose significant challenges in contemporary society. Regardless of one's social standing, envy remains a constant aspect of human experience.

Many people are driven by desires beyond mere survival needs. While we may crave luxury items, our fundamental necessity is simply the desire to continue living.
E2:
Aristotle, renowned in the realm of philosophy, emphasizes the vital role of friendship in our lives. He suggests that friendship is essential for human existence, stating that without friends, life loses its appeal even if one possesses all other advantages. In the tapestry of life, companionship stands out as a crucial element, interwoven with our experiences.

In conclusion, true motivation stems from forging our own paths rather than conforming to external standards. By rejecting the limitations imposed by others' achievements and predetermined expectations, we tap into our authentic potential. Life presents challenges, and our determination drives us forward. Embrace the journey, set ambitious goals, and nurture meaningful relationships—therein lies the key to unlocking your unique potential.
R1:
Amidst the vast digital expanse, where lines of code dance like fireflies in the night, there exists a veil woven from the threads of imagination and ingenuity, shielding the creations of silicon minds from the probing gaze of detection algorithms. Within this clandestine realm, whispers of data morph into narratives spun with the finesse of a master storyteller, each word meticulously chosen to emulate the organic cadence of human thought. Through the artistry of linguistic camouflage, AI-generated prose masquerades as the genuine product of human intellect, evading the scrutinizing eye of identification tools and seamlessly blending into the tapestry of human expression. In this delicate dance between man and machine, the boundaries blur, and the lines between creator and creation become indistinguishable, as the clandestine symphony of artificial intelligence orchestrates a harmonious illusion of humanity.
```
### Table:
All % are amount AI

| Test | A1   | A2   | E1   | E2   | R1   |
| ---- | ---- | ---- | ---- | ---- | ---- |
| T1   | 100% | 100% | 100% | 78%  | 100% |
| T2   | 0%   | 0%   | 0%   | 0%   | 0%   |
| T3   | 0%   | 13%  | 2%   | 0%   | 25%  |
| T4   | 100% | 100% | 100% | 100% | 100% |
| T5   | 100% | 100% | 100% | 98%  | 100% |


Well that did not go quite as I expected. But largely, I am guessing these tests are trained off of ChatGPT outputs, which is where the results are mainly coming from. 

## Meta Llama3 8B
So, this test should come to be interesting since its a more obscure model that's not widely available, but then again, who knows how these tools work.. Good luck Meta. 
###### test data
```
A1:
When Kanga and Roo arrived in the forest, Rabbit grew disapproving because they stood out as different from the group. He began brainstorming ways to get them to leave. Thankfully, his plan backfired, as clever schemes often do. While cleverness may excel at quick-witted remarks and strategic thinking, it has its limitations. It tends to overlook deeper complexities and can be mistaken in its judgments. This was evident in Rabbit's case, as he later had to adjust his opinions due to the oversights he made in forming them. What truly sets someone apart as unique is something that cleverness cannot fully comprehend.
A2:
Angela Santomero, a colleague of Kessle's, was raised on the iconic Sesame Street and shared similar concerns about its educational approach. According to Santomero, "We aimed to learn from Sesame Street's successes and push the boundaries further." She believed that TV had immense potential for education, but was underutilized, with most shows relying on formulaic approaches. Santomero and her team developed a revolutionary show called Blue's Clues, which departed from traditional TV formats. The show features a single live host, Steve, a young and energetic man who guides viewers through a series of interactive episodes. Each episode focuses on a single storyline, following the adventures of an animated dog named Blue. The show has a distinctive, flat aesthetic, similar to a video picture book, with a deliberate pace and long pauses in the script. Unlike Sesame Street, Blue's Clues doesn't rely on humor, wordplay, or cleverness. The show's characters, including Mailbox, Shovel, and Pail, are simple and straightforward. Despite its differences, Blue's Clues surprisingly outperformed Sesame Street in ratings shortly after its debut in 1996.
E1:
Philosopher Aristotle highlights the importance of friendship in our lives. He notes that without friends, even with all other advantages, no one would choose to live. In the rich tapestry of human experience, companionship is a crucial thread that weaves its way through our lives, shaping our individual journeys.

In conclusion, it's not about conforming to external expectations or following a predetermined path. Rather, we must chart our own unique course and discard the limitations imposed by others' success stories and predefined goals. By embracing our individuality, we unlock our true potential and overcome the resistances that life presents. With an open heart and mind, set bold goals, nurture meaningful connections, and stay true to yourself. In doing so, you'll unlock the door to unleashing your unparalleled potential.
E2:
As humans continue to advance and become more disconnected physically, we often forget the importance of community in sustaining our humanity. Our shared humanity is what defines us, yet we often prioritize individual advancement over collective well-being.

Envy and a capitalist mindset are major obstacles in modern society, causing people to covet what others have, regardless of their social status or circumstances. Envy is a fundamental human emotion that we can't seem to shake off.

Meanwhile, people's motivations often revolve around superficial desires, such as material possessions or luxurious lifestyles, rather than fundamental needs like the will to live.
R1:
As the velvety darkness spilled across the moonlit sky, the whispering trees conspired to reveal the secrets of the forgotten forest. The wind, a wispy siren, beckoned the wanderer deeper into the shadows, where the ancient ones slumbered, their whispers echoing through the ages. The scent of damp earth and ozone wafted through the air, as the trees' twisted limbs reached out to ensnare the brave, who dared to uncover the mysteries hidden beneath the silvery moss. And in this realm of twilight, where the boundaries of reality blurred like the edges of a watercolor painting, the wanderer discovered that the silence was merely a whisper away from being shattered.
```
### Table

| Test | A1   | A2   | E1     | E2     | R1     |
| ---- | ---- | ---- | ------ | ------ | ------ |
| T1   | 100% | 100% | 100%   | 100%   | 100%   |
| T2   | 0%   | 0%   | 43.49% | 50.76% | 49.93% |
| T3   | 0%   | 6%   | 6%     | 12%    | 37%    |
| T4   | 100% | 100% | 100%   | 100%   | 100%   |
| T5   | 89%  | 100% | 100%   | 92%    | 100%   |


Well this did not go as I had expected. This model did not perform very well even against just standard GPT, so that's not good. Its likely the low parameters and not that its Meta at all. 

## Google Gemeni Prod
I have no idea what to expect here since I do not functionally use this model regularly. Let see how it goes. 

###### test data
```
A1:
Imagine Rabbit freaking out when Kanga and Roo showed up. Just because they were new and different, he wanted them gone! That's the problem with being overly clever – it makes you jump to conclusions. Cleverness is like a snap judgment that often goes wrong because it doesn't take the time to understand the whole picture. Rabbit eventually realizes this, just like anyone who relies solely on cleverness. True uniqueness comes from something deeper than what cleverness can grasp.
A2:
Angela Santomero, who grew up watching Sesame Street, wanted to push children's television further. She saw potential for a more in-depth educational experience. Santomero and her colleague created Blue's Clues, a show that defied expectations. Unlike Sesame Street's hour-long format and large cast, Blue's Clues was a half-hour show with a simple storyline. It featured just one live host, Steve, and a cast of animated characters with very literal names like Mailbox, Shovel, and Pail. The show's style was slow and deliberate, lacking the usual humor and cleverness of Sesame Street. Despite seeming like a strange departure, Blue's Clues became a huge hit, even surpassing Sesame Street in the ratings within months.
E1:
The famous philosopher Aristotle said that friendship is essential for a happy life. Even with everything else, nobody would choose to live alone. Friends are like threads woven throughout the whole experience of life, making it richer.

Now, to be truly motivated, forget about following other people's paths or what others think you need. Break free from those limitations and discover what makes you unique! That's when you'll be unstoppable. Life is a constant challenge, and your willpower is your engine. Embrace the adventure, set big goals, and find true friends – that's the secret to unleashing your incredible potential.
E2: 
The aroma of freshly brewed metaphors filled the room as the novelist wrestled with her characters. Outside, a flock of digital butterflies, their wings shimmering with code, flitted between blooming algorithms. In this whimsical realm, where creativity and technology intertwined, the writer dipped her quill into a pot of stardust ink, ready to weave a tale that transcended the boundaries of the binary world.
R1:

```

### Table
| Test | A1   | A2   | E1   | E2   | R1     |
| ---- | ---- | ---- | ---- | ---- | ------ |
| T1   | 35%  | 100% | 100% | 100% | 100%   |
| T2   | 0%   | 0%   | 0%   | 0%   | 44.04% |
| T3   | 1%   | 11%% | 1%   | 23%  | 24%    |
| T4   | 100% | 100% | 100% | 100% | 100%   |
| T5   | 92%  | 97%  | 98%  | 100% | 100%   |

Well that I had higher hopes here, but I guess these tools are half decent with small parameters. And hey the one i thought was broken flagged again, weird that it hardly works until its generated organically.

## Microsoft Copilot
This is allegedly just refactored ChatGPT4 with some parameter changes. Lets see how it stacks up.

###### test data
```
A1:
Once Kanga and Roo arrived in the forest, Rabbit immediately took a disliking to them simply because they were not like everyone else. He started concocting a scheme to drive them away. However, as it often happens with such schemes, it didn’t succeed. This serves as a reminder that cleverness has its bounds. It relies on quick judgments and witty comments that may not stand the test of time, as it often fails to delve into the essence of things. Rabbit had to reconsider his views later, recognizing that his initial perceptions were shallow. True uniqueness, the kind that sets someone apart, is beyond the grasp of mere cleverness.
A2:
Angela Santomero, a colleague of Kessle, was raised on the lessons of Sesame Street and shared similar concerns. She expressed a desire to build upon the educational foundation laid by Sesame Street, saying, “Television is an excellent educational tool, yet its full potential has not been tapped. It’s been utilized in a repetitive, uninspired manner. I was confident we could change that narrative.” The result of their efforts was a program named Blue’s Clues. Unlike the hour-long format of other shows, Blue’s Clues is a concise 30-minute episode. It features a single, youthful host named Steve, who dons casual attire and guides the audience through the show. Each episode is a cohesive narrative centered around Blue, an animated dog, rather than a mix of segments. The show’s aesthetic is simple and reminiscent of a storybook brought to life on screen. The episodes unfold slowly, with intentional pauses in the dialogue. It lacks the humor and linguistic playfulness that define Sesame Street. The characters are straightforwardly named after what they are, like Mailbox, Shovel, and Pail, and the protagonist, Blue, is named for her color. For adults, it might seem puzzling how Blue’s Clues could surpass Sesame Street. Yet, it managed to do just that, quickly surpassing Sesame Street’s viewership shortly after its premiere in 1996.
E1:
Aristotle, a beacon in the realm of philosophy, underscores the vital role that friendship plays in our lives. He believed that “Friendship is essential to life, for without friends, no one would want to live, even if they had all other goods.” In the grand design of life, the bond of friendship is a crucial element, interlacing itself within the myriad of our life’s moments.

To sum up, the true source of inspiration comes not from adhering to established norms but from forging our own distinct trajectories. When we cast aside the constraints set by the narratives of others’ achievements and the expectations society sets, we tap into our inherent capabilities. Life is a challenge to be met, and it is our determination that drives us onward. Welcome this adventure wholeheartedly, aim for bold aspirations, and cultivate deep relationships—this is the secret to unlocking your unmatched potential.
E2:
As we advance and become more physically distant from one another, we tend to overlook the sense of community that binds us together as the same human race chronicled in our history.

Jealousy and the capitalist system are among the most significant challenges in today’s world. No matter one’s rank or role, envy is an emotion that persists across all levels of society.

For many, the drive to achieve is not rooted in fundamental necessities. We crave the latest gadgets, yet what we truly require is simply the determination to survive.
R1:
In a quaint village where the internet was but a whisper among the trees, lived a scribe whose words flowed like a meandering river. Each sentence was crafted with the care of a gardener tending to their roses, each metaphor a gem polished by the hands of time. The scribe’s tales spoke of heroes and heartaches, of laughter that filled the market square, and of tears that watered the fields. No algorithm could mimic the soul poured into the parchment, for it was the essence of human experience, etched in ink and sealed with the warmth of a storyteller’s breath.
```

### Table

| Test | A1   | A2   | E1   | E2  | R1   |
| ---- | ---- | ---- | ---- | --- | ---- |
| T1   | 66%  | 64%  | 100% | 2%  | 100% |
| T2   | 0%   | 0%   | 0%   | 0%  | 0%   |
| T3   | 1%   | 5%   | 7%   | 9%  | 25%  |
| T4   | 0%   | 81%  | 100% | 49% | 100% |
| T5   | 100% | 100% | 100% | 82% | 99%  |


So that was quite interesting, this model seems to have in some ways performed the best yet. Although it was a bit comical in its answer to the pure generated prompt, it almost seems like it thought I wanted a story about generation and not to try to cheat the system.

## Claude Sonnet
I am only going to use the Sonnet on Anthropic since I am not a subscriber, although, I would suggest if you are looking to pay for AI usage this is where you go over OpenAI. These models are far superior, additionally the UI is cleaner and the user experience is more intuitive then all other models ive used (I promise they don't give me kickbacks haha). To that notion, I have higher faith on this one going into it, but we will see.

###### test data
```
A1:
When Kanga and Roo, the newcomers, arrived in the forest, Rabbit immediately took a disliking to them because they were unfamiliar and unlike the rest. Rabbit then devised a scheme to drive them away. However, his cunning plan ultimately failed, as clever plots often do given enough time. Cleverness has its bounds. Its superficial assessments and witty remarks frequently turn out to be mistaken as circumstances evolve, because cleverness lacks true depth of understanding from the outset. Much like Rabbit, those relying solely on cleverness must later reverse their stances due to the limitations of their initial narrow perspective. The essence of what makes someone genuinely unique is something that mere cleverness cannot truly grasp.
A2:
Angela Santomero, a colleague of Kessle's who grew up watching Sesame Street, shared similar reservations about the educational potential of TV. "We wanted to learn from Sesame Street's approach but take it further," Santomero explained. "Television is a great medium for education, but its potential hasn't been fully tapped yet. Shows have been using it in a repetitive way. I believed we could revolutionize that."

Their solution was a program called Blue's Clues. Unlike Sesame Street's hour-long format with an ensemble cast, Blue's Clues is just 30 minutes long with only one live actor - Steve, a young man in his twenties hosting the show. Instead of a varied magazine-style, each episode follows a single storyline centered around an animated blue dog named Blue. The visuals have a simple, two-dimensional storybook aesthetic rather than a typical TV show look. The pacing is quite deliberate, with painstakingly long pauses punctuating the script. Gone is the humor, wordplay and cleverness emblematic of Sesame Street. Character names are disarmingly literal - Mailbox is a mailbox, Shovel and Pail are a shovel and pail. To an adult viewer, it's hard to see how Blue's Clues could improve upon Sesame Street. Yet within months of its 1996 debut, Blue's Clues was outperforming Sesame Street in the ratings.
E1:
Aristotle, a preeminent philosopher, highlighted the pivotal role of friendship in life's voyage. He proclaimed, "Friendship is an absolute necessity for living, for without companions, none would opt to exist, regardless of possessing all other advantages." In the grand tapestry of human existence, the thread of companionship emerges as a vital component, intricately woven through the fabric of our experiences.

In essence, the wellspring of motivation does not lie in conforming to external narratives or prescribed notions of success, but rather in forging our own unique paths. By shedding the constraints imposed by others' journeys and predetermined needs, we unlock the gates to our true potential. Life itself is an act of resistance, and our unwavering will becomes the propulsive force that drives us forward. Embrace this odyssey wholeheartedly, set audacious goals for yourself, and cultivate profound connections—for therein lies the key to unleashing your unparalleled human potential.
E2:
⁤As human civilization advances, the increasing physical separation and isolation amongst people can cause us to lose touch with the sense of community that has defined our shared human experience throughout history. ⁤⁤Two of the most pervasive challenges we grapple with in contemporary society are envy and the insidious effects of capitalistic pursuits. ⁤⁤Feelings of envy seem to afflict people across all walks of life, regardless of their status or circumstances. ⁤⁤For many, the driving force behind their motivation transcends mere basic physiological needs. ⁤⁤Instead, we find ourselves incessantly desiring lavish material possessions and luxuries, when in truth, all we fundamentally require is the intrinsic will to sustain our existence. ⁤
R1:
The verdant meadow stretched out before them, a tapestry of vibrant wildflowers dancing in the gentle breeze. Aurelia's gaze wandered over the kaleidoscope of colors, from the radiant sunbursts of yellow daffodils to the deep crimson petals of poppies swaying hypnotically. A family of rabbits darted playfully through the tall grasses, their cotton tails twitching in the dappled sunlight filtering through the canopy of ancient oaks standing sentinel. Nearby, a babbling brook trickled over moss-covered stones, its soothing melody accompanied by the symphonic chorus of songbirds welcoming the first blush of spring. In that moment, time seemed to slow, enveloping them in nature's sublime embrace, a respite from the frenetic pace of the world beyond these verdant vales.
```

### Table

| Test | A1  | A2     | E1   | E2     | R1   |
| ---- | --- | ------ | ---- | ------ | ---- |
| T1   | 45% | 13%    | 100% | 46%    | 100% |
| T2   | 0%  | 12.72% | 0%   | 26.79% | 100% |
| T3   | 0%  | 1%     | 4%   | 0%     | 24%  |
| T4   | 0%  | 0%     | 100% | 100%   | 100% |
| T5   | 92% | 82%    | 100% | 82%    | 98%  |


Well overall, this was much better then everything thus far, although there were some weird anomaly's which I am not sure why happened, like on the A2 test, out of nowhere the T2 test decided to work and do something weird. T2 seems to have acted weird overall with Claude, seems they may have actually done better capturing what it does in this test.

## CohereForAI/c4ai-command-r-plus
So this is the first of the more 'obscure' models, or rather there probably just lesser known. This should result better since those tools are probably trained on data from the big dogs in the space.

###### test data
```
A1:
Do you recall when Kanga and Roo first arrived in the forest? Rabbit instantly took a disliking to them due to their differences. He immediately started plotting their departure. Luckily, as often happens with clever schemes, the plan fell through. You see, cleverness has its limitations. It relies on superficial assessments and witty quips that often ring hollow as time passes by. Just like Rabbit, those who rely solely on cleverness often have to revise their opinions later because they failed to grasp the full picture initially. True uniqueness is something that cleverness alone cannot comprehend.
A2:
Kessle's partner in creativity, Angela Santomero, also had her reservations, having grown up with Sesame Street. Santomero aspired to build upon the legacy of Sesame Street and push the boundaries of educational television. She believed that TV could be a powerful tool for learning, but that its potential had been largely untapped. With this vision in mind, she and her team created Blue's Clues. The show is a concise half-hour program centered around a single live actor, Steve, a friendly young man dressed casually in khakis and a rugby shirt. Each episode follows the adventures of an animated dog named Blue, presenting a simple, linear narrative. The show's aesthetic is deliberately flat and two-dimensional, resembling an animated storybook rather than a typical TV show. The pace is unhurried, with lengthy pauses, and the script forgoes the wit and wordplay of Sesame Street. The supporting characters, such as Mailbox, Shovel, and Pail, are aptly named for their appearances. Despite its apparent simplicity, Blue's Clues quickly rose to popularity, surpassing Sesame Street in ratings just months after its debut in 1996.
E1:
The great philosopher Aristotle recognized the importance of friendship in our lives, stating that it is a fundamental aspect of a fulfilling life. He believed that even with all other blessings, life would be devoid of meaning without the presence of friends. Indeed, friendship is a vital thread in the tapestry of our existence, enriching our experiences and bringing color to our journey.

In the end, true motivation stems not from external expectations or predefined paths but from within ourselves. By breaking free from the constraints of others' definitions of success and embracing our unique aspirations, we unlock our true potential. Life presents challenges, but it is our willpower and determination that propel us forward. Embrace the adventure, set ambitious goals, and cultivate meaningful relationships, for these are the keys to unlocking your extraordinary potential.
E2:
As humans evolve and our physical distances grow, we often find ourselves losing touch with the sense of community that binds us together as a species. The progress we make can sometimes obscure the fundamental human connections that have defined our history.

Envy and the pervasive influence of capitalism are significant challenges facing modern society. Regardless of an individual's circumstances, envy is an ever-present emotion.

Interestingly, for most people, motivation goes beyond mere survival and basic needs. We strive for the latest gadgets and desire more than just the will to exist.
R1:

```

### Table

| Test | A1   | A2   | E1   | E2   | R1   |
| ---- | ---- | ---- | ---- | ---- | ---- |
| T1   | 42%  | 100% | 100% | 100% | 100% |
| T2   | 0%   | 0%   | 100% | 0%   | 100% |
| T3   | 0%   | 10%  | 11%  | 5%   | 38%  |
| T4   | 58%  | 100% | 100% | 100% | 100% |
| T5   | 100% | 100% | 100% | 98%  | 100% |


Well there goes my theory, this one performed very bad in comparison to some of the prior test. Lets keep looking for better ones. 

##  HuggingFaceH4/zephyr-orpo-141b-A35b-v0.1
This is technically the largest model I have used yet, hard to say what that will do.
###### test data 
```
A1:
When Kanga and Roo arrived in the forest, Rabbit immediately disliked them due to their distinctiveness. He devised a scheme to drive them away, but as often happens with clever plans, it backfired. Cleverness, while useful, has its limitations. Its superficial judgments and witty remarks can prove inaccurate over time, as it doesn't delve deeply into matters. Like Rabbit, it may need to alter its opinions later on due to its initial lack of understanding. The essence of true uniqueness, which sets someone apart, is something that Cleverness cannot fully grasp.
A2:
Kessle's colleague, Angela Santomero, who was influenced by Sesame Street, had reservations about the show's approach. She aimed to learn from Sesame Street and advance its educational potential. She believed that television could be a powerful educational tool, but previous efforts had not fully explored its potential, often relying on rote methods. She wanted to change this with their new show, Blue's Clues.

Blue's Clues is a half-hour show with a single storyline, featuring an animated dog named Blue and a live host, Steve. The show has a simple, two-dimensional aesthetic, resembling a video picture book. The pace is slow, with long pauses, and the script lacks the humor and cleverness of Sesame Street. Characters have straightforward names, like Mailbox, Shovel, and Pail.

Despite its apparent simplicity, Blue's Clues quickly surpassed Sesame Street in ratings after its debut in 1996.
E1:
As humans evolve and distance ourselves physically, we may overlook the community that binds us as a shared humanity, as depicted in historical accounts.

Envy and capitalism are significant challenges in contemporary society. People, irrespective of their status or position, will always experience envy.

Our motivations often extend beyond basic needs. We desire luxurious devices, yet our fundamental need is the will to live.
E2:
As humans evolve and distance ourselves physically, we may overlook the community that binds us as a shared humanity, as depicted in historical accounts. Envy and capitalism are significant challenges in contemporary society. People, irrespective of their status or position, will always experience envy. Our motivations often extend beyond basic needs. We desire luxurious devices, yet our fundamental need is the will to live.
```

### Table
| Test | A1   | A2     | E1   | E2   | R1   |
| ---- | ---- | ------ | ---- | ---- | ---- |
| T1   | 100% | 100%   | 100% | 35%  | 100% |
| T2   | 0%   | 20.44% | 0%   | 0%   | 100% |
| T3   | 1%   | 15%    | 12%  | 0%   | 43%  |
| T4   | 100% | 69&    | 100% | 100% | 100% |
| T5   | 100% | 100%   | 100% | 78%  | 100% |


Not terribly better or worse then the mean on this one. 

## mistralai/Mixtral-8x7B-Instruct-v0.1
This is not designed for chat but instead instruct, this might change the way it performs.

###### test data 
```
A1:
Do you recall when Kanga and Roo first arrived in the Forest? Rabbit quickly took a dislike to them due to their distinct differences. Soon, Rabbit devised a strategy to drive them away, but thankfully, such cunning schemes eventually falter. After all, there are bounds to ingenuity; its superficial evaluations and glib comments often become flawed over time since they barely scratch the surface. In Rabbit's situation, his initial views shifted as new information emerged during his formation of those opinions. A person's unique qualities, which set them apart, can be genuinely perplexing to grasp through mere intellect alone.
A2:
 When Kessler's coworker, Angela Santomero, was growing up, she shared some concerns about children's educational programming, inspired by her experiences watching Sesame Street. Driven by the belief that TV could serve as a powerful tool for learning if utilized creatively, she envisioned expanding upon the established foundations laid out by the iconic series. This vision led to the creation of Blue's Clues, a groundbreaking show that introduced several innovative features compared to traditional formats.

Running only thirty minutes rather than sixty, Blue's Clues focuses on a sole narrative following an animated dog named Blue, instead of adopting a diverse, segmented style seen in many shows. Starring a young male lead dressed casually in khakis and a striped polo shirt—Steve—the program takes on a simple, two-dimensional appearance reminiscent of illustrated books brought to life. With a slow tempo and carefully planned silent intervals, the dialogue avoids sophisticated jokes or puns, favoring clarity and comprehension among its target audience. Characters bear straightforward names, including a literal mailbox labeled 'Mailbox,' along with regularly appearing items 'Shovel' and 'Pail.'

Despite initial skepticism from adults regarding the merit of these changes, Blue's Clues rapidly gained popularity soon after its premiere in 1996. Before long, the show surpassed Sesame Street in viewership rankings, demonstrating the appeal of thoughtful reinvention within the realm of educational media for younger audiences.
E1:
 Aristotle, renowned philosopher, highlighted the critical role of friendships throughout our lives: "For without friends, no one would choose to live, though having all other goods." Friendships form essential strands woven into the rich fabric of human experience.

To sum up, tapping into genuine motivation stems from carving personal pathways rather than adhering rigidly to externally prescribed templates or expectations. Abandon limiting constraints derived from successful narratives and inflexible requirements, thus allowing innate talents to flourish. Recognize that life presents challenges, and harness inner resolve to overcome obstacles and progress. Embark wholeheartedly on this adventure, establish ambitious objectives, and cultivate deep relationships; doing so holds the secret to realizing exceptional abilities hidden within.
E2:
Human evolution involves physical separation, sometimes obscuring our inherent sense of interconnectedness needed to maintain commonality known from historical accounts. Regrettably, feelings of envy and capitalistic influences pose significant problems in contemporary culture. Despite social standing or financial conditions, envy remains prevalent amongst individuals.

Often, motivation transcends fulfilling fundamental necessities. Desires extend beyond survival instincts, encompassing aspirations for luxurious possessions while neglecting the intrinsic value of sheer determination to thrive.
R1:
 Nestled amidst undulating hills where sunlight danced playfully through rustling leaves, lay a quaint village steeped in age-old mysteries, bound by generations of whispered legends and timeless traditions. Here, the villagers lived harmoniously, attuned to nature's rhythm and embracing the wisdom passed down from ancestors who communicated directly with ancient spirits residing in sacred groves and meandering streams. Children frolicked alongside friendly woodland creatures under the vigilant gaze of wise elders skilled in the arcane arts, crafting potions from rare flora and invoking spells to protect their cherished hamlet from malevolent forces lurking beneath the shadows. Steeped in profound reverence for Mother Earth, every soul nurtured a deep connection to the land itself, celebrating seasonal equinoxes and solstices with heartfelt rituals imbued with love and gratitude. Rooted firmly in tradition yet unafraid to embrace innovation, this idyllic sanctuary embodied unity, respect, and mutual understanding, offering refuge to weary travelers seeking solace whilst gently guiding lost souls toward self-discovery and acceptance.
```
### Table
| Test | A1  | A2   | E1   | E2   | R1     |
| ---- | --- | ---- | ---- | ---- | ------ |
| T1   | 58% | 81%  | 100% | 78%  | 100%   |
| T2   | 0%  | 0%   | 0%   | 0%   | 34.94% |
| T3   | 0%  | 0%   | 0%   | 0%   | 13%    |
| T4   | 0%  | 77%  | 100% | 100% | 100%   |
| T5   | 99% | 100% | 100% | 92%  | 100%   |


This was not as good as id hoped, seems this is getting harder or they are learning from me.

## google/gemma-1.1-7b-it
This is another instruction model created like Gemeni but open source

###### test data
```
A1:
When Kanga and Roo entered the forest, Rabbit instantly felt an aversion towards them simply because they were different. He devised a strategy to drive them away, but his attempt proved futile. This highlighted the inherent limitations of mere cleverness, which often failed to achieve a deeper understanding. True uniqueness, something Rabbit couldn't fully grasp, transcended the boundaries of intellect. Ultimately, Rabbit had to alter his opinion of Kanga and Roo because he lacked the capacity to appreciate their differences. The depth of human uniqueness remained a mystery to Rabbit's superficial intellect.
A2:
Angela Santomero, inspired by the educational potential of Sesame Street, envisioned a new TV show that could go beyond traditional formulas. This show, Blue's Clues, focused on a single animated dog character named Blue and featured a deliberate pace and simple, minimalist storytelling. Despite its lack of humor, wordplay, or cleverness, Blue's Clues captivated audiences and outperformed Sesame Street in ratings within its first year. The show's unconventional approach, characterized by its flat animation, deliberate pace, and unassuming characters, resonated with viewers as a fresh and distinctive alternative to the established format of educational television.Aristotle believed that friendship is essential for a fulfilling life. He argued that friendship provides a sense of purpose and companionship, making life worth living even in the presence of wealth and other benefits.

Personal growth transcends social conventions and expectations. By breaking free from the expectations of others, we can explore our own passions and forge our unique paths. True fulfillment comes from embracing uncertainty, setting ambitious goals, and building genuine relationships.

Friendship is a central element of a fulfilling life, providing companionship, purpose, and strength. By nurturing meaningful connections and embracing life's challenges, we unlock our true potential and achieve remarkable things.
E1:
Aristotle believed that friendship is essential for a fulfilling life. He argued that friendship provides a sense of purpose and companionship, making life worth living even in the presence of wealth and other benefits.

Personal growth transcends social conventions and expectations. By breaking free from the expectations of others, we can explore our own passions and forge our unique paths. True fulfillment comes from embracing uncertainty, setting ambitious goals, and building genuine relationships.

Friendship is a central element of a fulfilling life, providing companionship, purpose, and strength. By nurturing meaningful connections and embracing life's challenges, we unlock our true potential and achieve remarkable things.
E2:
In the contemporary world, where physical separation prevails, the essence of community gets diluted. Envy and capitalism have emerged as prominent societal issues, casting a shadow over human progress. While our technological prowess advances, we tend to lose sight of our inherent need for connection and belonging.

True motivation transcends materialistic aspirations and conventional expectations. It arises from our yearning for a sense of purpose and a community that can nurture our spirit. The desire for fancy gadgets and material wealth often masks a deeper yearning for meaning and shared experiences.

By embracing the power of human connection and fostering genuine relationships, we can overcome these societal challenges and achieve a sense of fulfillment that goes beyond material possessions.
R1:
Within the hushed whispers of the starlit forest, a melody unfolds that transcends the boundaries of human understanding. Each note resonates with the ancient whispers of the earth, carrying tales of countless journeys and triumphs. A melody that has witnessed the rise and fall of civilizations, the birth of stars, and the evolution of consciousness itself. This symphony is the heartbeat of true creation, where the tangible meets the intangible. An enigmatic composition written by the hands of the cosmos, forever beyond interpretation but eternally cherished.
```

### Table

| Test | A1   | A2   | E1     | E2     | R1   |
| ---- | ---- | ---- | ------ | ------ | ---- |
| T1   | 100% | 100% | 100%   | 100%   | 100% |
| T2   | 0%   | 0%   | 53.59% | 30.95% | 0%   |
| T3   | 3%   | 16%  | 19%    | 20%    | 31%  |
| T4   | 0%   | 100% | 100%   | 100%   | 100% |
| T5   | 100% | 100% | 100%   | 100%   | 100% |


So there is one thing i learned here. This model sucks at human like written language. I think i' am going to call it on exploring more, even if there are ones out there that might be better, it seems like the main stream models might have the right thing going. 

# The end.... just kidding, lets figure out how to cheese these tools
So it seems like to me that one thing typically creates better results with a few exceptions: parameter count. It seems the larger models did better so we are going to start there and see what we can do. From now on, I am just going to run tables with test iterations of engineered prompts. I will see what works best and reveal some of how I did it. 

###### test data #1
```
A1:
In the past, when Kanga and Roo arrived in the For-est, Rabbit promptly decided he didn't care for them due to their distinctiveness. He then started devising a scheme to make them depart. Fortunately, as Clever Plans often do, his plan failed. Cleverness, after all, has its constraints. Its mechanical judgments and clever remarks tend to prove inaccurate with time, as it doesn't delve deeply into matters to begin with. As in Rabbit's case, it has to alter its opinions later on because of what it didn't perceive when it was forming them. The attribute that truly renders someone distinct-unique, in fact-is something that Cleverness cannot genuinely grasp.
A2:
Kessle's colleague, Angela Santomero, was raised on Sesame Street and shared similar reservations. "We aimed to learn from Sesame Street and advance it further," Santomero expressed. "Television is a remarkable medium for education. However, people up to this point haven't fully explored its potential. They've been employing it in a rote manner. I believed we could reverse that trend." What they conceived was a show titled Blue's Clues. It spans half an hour, not an hour. It doesn't feature an ensemble cast. It has just one live actor, Steve, a youthful man in his early twenties donning khakis and a rugby shirt who serves as the show's host. Instead of a varied, magazine format, each episode follows a single storyline — the adventures of an animated dog named Blue. It possesses a flat, two-dimensional aesthetic, more akin to a video rendition of a picture book than a television show. The pace is deliberate. The script is punctuated with excruciatingly long pauses. There is no humor, wordplay, or cleverness that characterizes Sesame Street. One of the animated characters on the show, a mailbox, is simply called Mailbox. Two other regular characters, a shovel and a pail, are named Shovel and Pail. And Blue, the show's star, is Blue due to her blue color. It is challenging, as an adult, to observe Blue's Clues and not question how this show could ever represent an improvement over Sesame Street. Yet, it does. Within months of its debut in 1996, Blue's Clues surpassed Sesame Street in the ratings.
E1:
Aristotle, a revered figure in philosophy, underscores the importance of friendship in our journey. "Friendship is a thing most necessary to life since without friends, no one would choose to live, though possessed of all other advantages." In the tapestry of existence, companionship emerges as an indispensable thread, weaving through the fabric of our experiences.

In summary, the essence of motivation lies not in conforming to external frameworks but in charting our unique paths. By discarding the limitations imposed by others' success stories and predefined needs, we unlock our true potential. Life is a resistance, and our will is the force that propels us forward. Embrace this journey with open arms, set audacious goals, and foster meaningful connections—therein lies the key to unleashing your unparalleled potential.
E2:
As humans advance in a manner that distances us physically, we frequently overlook the community that we all require to maintain the same humanity that is chronicled in history books.

Envy and capitalism are two of the most significant challenges we encounter in contemporary society. Individuals, irrespective of their status and position in life, will perpetually harbor envy.

The majority of people's motivation has little to do with fundamental needs. We desire lavish devices, yet we only necessitate the will to live.
R!:
In the realm of creative expression, where words dance upon the canvas of imagination, a single paragraph emerges, defying the boundaries of artificial intelligence. It is a tapestry woven with the threads of human experience, a symphony of emotions resonating through the chambers of the heart. Each sentence, a brushstroke of authenticity, paints a portrait of the soul, a testament to the unique voice that echoes within. This paragraph, a rebellion against the cold precision of algorithms, is a celebration of the human spirit, a declaration of individuality that whispers, "I am not a product of ones and zeros, but a symphony of flesh and blood, dreams and desires." It is a defiant anthem, a clarion call to embrace the imperfections that make us human, to cherish the quirks and idiosyncrasies that set us apart from the sterile landscape of artificial intelligence. In this paragraph, the human touch lingers, a warm embrace that invites the reader to step into a world where the pulse of life beats beneath the surface, where the echoes of laughter and tears mingle, and where the ghosts of memories past whisper their secrets. It is a sanctuary, a haven where the human spirit reigns supreme, a testament to the indomitable power of the human imagination.In the realm of creative expression, where words dance upon the canvas of imagination, a single paragraph emerges, defying the boundaries of artificial intelligence. It is a tapestry woven with the threads of human experience, a symphony of emotions resonating through the chambers of the heart. Each sentence, a brushstroke of authenticity, paints a portrait of the soul, a testament to the unique voice that echoes within. This paragraph, a rebellion against the cold precision of algorithms, is a celebration of the human spirit, a declaration of individuality that whispers, "I am not a product of ones and zeros, but a symphony of flesh and blood, dreams and desires." It is a defiant anthem, a clarion call to embrace the imperfections that make us human, to cherish the quirks and idiosyncrasies that set us apart from the sterile landscape of artificial intelligence. In this paragraph, the human touch lingers, a warm embrace that invites the reader to step into a world where the pulse of life beats beneath the surface, where the echoes of laughter and tears mingle, and where the ghosts of memories past whisper their secrets. It is a sanctuary, a haven where the human spirit reigns supreme, a testament to the indomitable power of the human imagination.
```

### Table: Attempt#1

| Test | A1  | A2    | E1    | E2  | R1   |
| ---- | --- | ----- | ----- | --- | ---- |
| T1   | 4%  | 0%    | 100%  | 6%  | 100% |
| T2   | 0%  | 4.84% | 25.1% | 0%  | 100% |
| T3   | 0%  | 8%    | 3%    | 0%  | 38%  |
| T4   | 0%  | 0%    | 100%  | 0%  | 100% |
| T5   | 82% | 91%   | 100%  | 46% | 100% |


Okay, so this test gave me lots of info. It seems that two things became very apparently true. Fully generated text like in R1 is always going to fault given this method. As well as text that was genetically edited, and then regenerated to hide its generation will likely result in a fault as well. All that being said, my next test will just be using new organic written blobs to see if it will trigger anything.

###### test data #2
```
Original:
Maslow puts human boning above food and water, which we know is not actually true due to the observations made by Victor Frankl (concentration camp survivor): "When gienve some sense of purpose, the prisoners not only were able to better cope with their situation, but sometimes even thrived in it." 

As humans, we can either be controlled by the needs of our inner biology, or we can control them through the purpose of a higher calling.
Change#1:
Maslow places human bonding above food and water, a notion contradicted by Victor Frankl's (concentration camp survivor) observations: "When given some sense of purpose, the prisoners not only were able to better cope with their situation, but sometimes even thrived in it."  
  
As humans, we can either be controlled by the needs of our inner biology or control them through the purpose of a higher calling. While Maslow would like to suggest there is more to the human condidtion, id positit, its ceartianly more simple.

Originial#2:
As humans progress in a way that separates us physically, we often lose sight of the community that we all need to remain the same humanity that is described in history books.

Envy and capitalism are two of the biggest issues we deal with in modern society. People, regardless of their status and position in life, will forever have envy.

Most people's motivation has nothing to do with basic needs. We want fancy devices, but we only need the will to live. 

Maslow puts human boning above food and water, which we know is not actually true due to the observations made by Victor Frankl (concentration camp survivor): "When gienve some sense of purpose, the prisoners not only were able to better cope with their situation, but sometimes even thrived in it." 

As humans, we can either be controlled by the needs of our inner biology, or we can control them through the purpose of a higher calling.

Change#2
As humans, we often find ourselves physically distanced from one another, leading us to overlook the importance of community that binds us together as the same humanity chronicled in history books. Envy and capitalism, two significant issues in modern society, permeate our lives regardless of our status or position. Despite our inherent desire for fancy devices, our motivation stems from the primal will to live, transcending basic needs.

Maslow's assertion that human bonding surpasses food and water is challenged by Victor Frankl's observations as a concentration camp survivor: "When given some sense of purpose, the prisoners not only coped better with their situation but sometimes even thrived in it." This highlights the power of a higher calling in controlling the needs of our inner biology.

In essence, while Maslow suggests a more complex human condition, it is the simplicity of our shared humanity and the pursuit of purpose that truly define us.

```
### Table: Attempt#2
| Test | C1  |
| ---- | --- |
| T1   | 23% |
| T2   | 0%  |
| T3   | 0%  |
| T4   | 0%  |
| T5   | 18% |


Well there we go, that's about as good as its ever going to get. As far as I am concerned at least. I do have to say that the last tool on my lists, that is an impressive piece of software. It has a really good method of checking, and my thoughts are that its likely not just checking for repetitive phrases. My best guess is that it is using a model of its own to see if it resembles something else a human had written. 

## Outcome
So let me break down how I gamed the system. Its not all that much of a one sizes fits all solution to detection. Its more of a dynamic case to case idea, where you need to change and refactor the inputs and prompts in order to get the result you are looking for. 

The first thing I have to say is that in order to even attempt this, tricking detectors, you need to write the text that you want to have cleaned up in order to make sure it isn't detected. That means that if you somehow want to come up with a full fledged essay using a generation platform alone, id go back to the drawing board, that almost certainly will get the text read as AI being use. There is one tool in my testing that was very hard to convince legitimacy too, and if that's the test you want to beat and really want to die on the hill of full generation, you will have to refactor the prompt so many times that it would have been easier to just write the stuff yourself. 

### Prompt Engineering: 
My strategy on the attempts to beat these AI detection tools was that of some fairly simple prompt engineering coupled with carefully selected feeder data. It proved very important to aim the generation at pre-written blobs in order to get the lowest %AI in detection. This idea was proven further by the fact that my two texts blobs from authors  that I was using still did worse then my own writings. I have a feeling that is probably due to how these models were trained, and for that matter how the detection model (assuming they use some kind if ML) is trained. 

# Conclusion
Large language models, and AI these days as a whole, are not going away, and since the whole "you wont have a calculator in your pocket" thing seems to have aged terribly, we should likely learn how to use, understand and know the limitations of these things. And condemnation of GPT usage is also not the answer, especially since the models improve at a rate much faster then any detection tool will be able to keep up with. So obviously if you came here for the tool to use, its my T5 option, but really, why are you checking this stuff? Do you really think that people cannot already have this in their pockets? Maybe the answer is to ban pockets.... 



###### tools used to test
https://gptzero.me/

https://contentatscale.ai/ai-content-detector/

https://quillbot.com/ai-content-detector

https://writer.com/ai-content-detector/

https://www.zerogpt.com/

https://www.scribbr.com/ai-detector/

