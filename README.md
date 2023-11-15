# pirate-game
1. Importing Libraries
   1) import pygame
   2) import random
   3) from os import path
   4) Here, the code imports the Pygame library for building games, the random module for generating random numbers, and the path module from the os library to handle file paths.

2. Setting up Constants
   1) WIDTH = 480
   2) HEIGHT = 600
   3) FPS = 60
   4) These constants define the width and height of the game window and the frames per second for the game.
  
3. Defining Colors
   1) WHITE = (255, 255, 255)
   2) BLACK = (0, 0, 0)
   3) RED = (255, 0, 0)
   4) GREEN = (0, 255, 0)
   5) BLUE = (0, 0, 255)
   6) YELLOW = (255, 255, 0)
  
4. CREATING SPRITE GROUPS
   1) all_sprites = pygame.sprite.Group()
   2) mobs = pygame.sprite.Group()
   3) bullets = pygame.sprite.Group()
  
5. Creating Player and Mobs
   1) player = Player()
   2) all_sprites.add(player)
   3) for i in range(8):

6. Setting up Score and Playing Background Music
   1) score = 0
   2) pygame.mixer.music.play(loops=-1)

7. Main Game Loop
   1) while running:

8. Event Handling
   1) for event in pygame.event.get():
   2)    if event.type == pygame.QUIT:
   3)       running = False

9. Updating Sprites
   1) all_sprites.update()

10. Checking Collisions
      1) hits = pygame.sprite.groupcollide(mobs, bullets, True, True)
      2) for hit in hits:

11. Drawing the Screen
      1) screen.fill(BLACK)
      2) screen.blit(background, background_rect)
      3) all_sprites.draw(screen)
      4) draw_text(screen, str(score), 50, WIDTH / 2, 10)
      5) draw_shield_bar(screen, 5, 5, player.shield)
      6) pygame.display.flip()

12. Quitting the Game
      1) pygame.quit()

 
