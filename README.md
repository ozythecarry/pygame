# pygame
import pygame
import time
import random

WIDTH, HEIGHT= 1000, 800
WIN = pygame.display.set_mode((WIDTH, HEIGHT))
pygame.display.set_caption("Dodge 'em all")

BG = pygame.transform.scale(pygame.image.load("bg.jpeg"), (WIDTH, HEIGHT))

PLAYER_WIDTH = 40
PLAYER_HEIGHT = 60
PLAYER_VEL= 5
def draw(player):
    WIN.blit(BG, (0, 0))

    pygame.draw.rect(WIN, "yellow", player)
    pygame.display.update()

def main():
    run = True

    player = pygame.Rect(200, HEIGHT - PLAYER_HEIGHT, PLAYER_WIDTH, HEIGHT)

    while run:
        for event in pygame.event.get():
            if event.type == pygame.QUIT:
                run = False
                break

        keys = pygame.key.get_pressed()
        if keys[pygame.K_LEFT]
            player.x -= PLAYER_VEL
        draw(player)

    pygame.quit()

if __name__ == "__main__":
    main()
