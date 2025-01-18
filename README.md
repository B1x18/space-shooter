# Space Shooter Game

A classic arcade-style space shooter game built with Phaser 3. Navigate through space, shoot enemies and asteroids while managing your ammo, and try to achieve the highest score.

## Demo
Play DEMO: [space-shooter](https://b1x18.github.io/space-shooter/)

## 🚀 Features

- Smooth spaceship controls with thrust and rotation
- Multiple enemy types (ships and asteroids)
- Particle effects for explosions and thrusters
- Ammo management system with auto-regeneration
- Score tracking with persistent high score
- Parallax starfield background
- Pause system
- Lives system
- Sound effects and background music
- Mobile detection with warning
- Fullscreen support

## 🎯 Controls

- **W/↑** - Thrust
- **A/←, D/→** - Rotate ship
- **SPACE** - Shoot
- **ESC** - Pause/Unpause
- **F** - Toggle fullscreen

## 🛠 Setup and Installation

1. Clone the repository:
```bash
git clone https://github.com/B1x18/space-shooter.git
cd space-shooter
```

2. Add the required game assets in an `assets` folder:
```
assets/
├── rocket.png
├── enemy.png
├── asteroid.png
└── sound/
    ├── gameover.mp3
    ├── shoot.mp3
    ├── hurt.mp3
    └── theme.mp3
```

3. Test locally using a web server. You can use Python's built-in server:
```bash
# For Python 3.x
python -m http.server 8000

# For Python 2.x
python -m SimpleHTTPServer 8000
```

Then visit `http://localhost:8000` in your browser.

## 🎨 Customization

### Adding Custom Ships
Replace the `rocket.png` in the assets folder with your own ship sprite. Update the ship dimensions in the code if needed:

```javascript
player.setSize(16, 30);  // Adjust collision box size
```

### Modifying Game Parameters
Adjust these constants in the code to change game behavior:

```javascript
const DRAG = 0.99;
const ROTATION_SPEED = 3;
const ACCELERATION = 5;
const MAX_SPEED = 400;
const BULLET_LIFESPAN = 5000;
```

### Changing Difficulty
Modify enemy spawn rates in the create function:

```javascript
this.time.addEvent({
    delay: 2000,  // Adjust delay between enemy spawns (in ms)
    callback: spawnEnemy,
    callbackScope: this,
    loop: true
});
```

## 📝 License

This project is licensed under the [Unlicense](./LICENSE).

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch: `git checkout -b feature/AmazingFeature`
3. Commit your changes: `git commit -m 'Add some AmazingFeature'`
4. Push to the branch: `git push origin feature/AmazingFeature`
5. Open a Pull Request

## 🙏 Acknowledgments

- Built with [Phaser 3](https://phaser.io/phaser3)
- Sound effects from [Pixabay.com](https://pixabay.com/sound-effects/)
- Images from me :P

## 🐛 Known Issues

- Mobile devices are not supported due to control scheme
- Some browsers may require enabling autoplay for sound to work