# comb the cat

Comb the cat while it isn't looking. If it turns around and you're still combing, you'll find out.

## Play

Play it at [cat.excl.sh](https://cat.excl.sh), or open `index.html` in a browser.

To play on a phone, serve the folder and open it from the phone on the same wifi:

```
python3 -m http.server 8000
```

Then go to `http://<your-computer-ip>:8000`. GitHub Pages works too.

## How it works

Hold and drag on the cat to comb it. The score goes up with how far you drag. Every few seconds the cat turns to look at you, and you have 0.4s to stop. Sometimes it turns right away. Sometimes it catches you and just stares for a bit before it jumps.

Your best score is kept in localStorage.

## Changing things

Timings live at the top of the script in `index.html`. `GRACE_MS` is the reaction window, `SUDDEN_LOOK_CHANCE` controls how often the cat turns fast, and `SCARE_DELAY_CHANCE` sets how often it stares before the jumpscare.

To use your own cat, replace the files and keep the names:

- `cat-away.png` and `cat-look.png` should be the same size with the body in the same place, or the cat jumps when it turns
- `cat-scare.jpg` is the jumpscare
- `vine-boom.mp3` plays when the cat turns, `roar.mp3` on the jumpscare
