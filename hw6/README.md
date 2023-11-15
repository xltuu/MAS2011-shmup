MAS2011-shmup
=============
### Play Space Shooter and having fun

* How To Play

    When you start the program, you will be the UFO, and meteor rotate. If push space bar, you can shoot bullet. If push the left, right key, you can avoid the meteor. On the upper left screen, there is an HP bar that shrinks when it crushes a meteor. When you crush with meteor and die, don't worry. You have 3 chance additionally. 

    Good Luck!

* Playing image
  
  <img src="playing.png" width="300px" height="px"></img>

* plyer, bullet, meteor

    <img src="img/witch.png" width="50px" height="px"></img>
    <img src="img/laserBlue08.png" width="50px" height="px"></img>
    <img src="img/potion_red_big.png" width="50px" height="px"></img>
* code 
    ```python
        bullet_img = []
        bullet_list = ["laserBlue09.png", "laserBlue10.png", "laserBlue08.png"]
        for bimg in bullet_list:
            bullet_img.append(pygame.image.load(path.join(img_dir, bimg)).convert())
    ```
    ```python
        class Bullet(pygame.sprite.Sprite):
        def __init__(self, x, y):
            pygame.sprite.Sprite.__init__(self)
            self.image_orig = random.choice(bullet_img)
            self.image_orig.set_colorkey(BLACK)
            self.image = self.image_orig.copy()
            self.rect = self.image.get_rect()
            self.rect.bottom = y
            self.rect.centerx = x
            self.speedy = -10
    ```

    define 3 bullet images, and randomly appear.
