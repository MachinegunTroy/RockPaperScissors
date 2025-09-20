# RockPaperScissors
My second RL project. I wanted to try MARL and decided to embark on a simple rock paper scissors project.

It was tough as there were many type errors with PyTorch tensors and infinite loops going on with the environment's step function not ending episodes or switching agents correctly. Eventually after fixing them
and using google collab's T4 GPU to run, both agents were trained pretty quickly and smoothly.

As player_1 was always able to see player_0's first move and never had to make the first move itself, it had the information advantage and exploited that to achieve an average reward of +0.978 over 20000 episodes of training,
compared to player_0's average reward of -0.978.

In 10000 episodes with a deterministic policy of epsilon = 0, we can see that player_1 was fully trained and won all 10000 games against player_0. 

My insight is that I probably should have masked the first move to player_1 and allowed them both to only see moves made on the previous round, or let them both take turns to make the first move.

My key takeaways was about how this project was much easier since I used a lot of boilerplate codes from my first blackjack rl project, and I have more experience and knowledge on how to create MARL systems.
