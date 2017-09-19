+++
showonlyimage = false
draft = false
image = "img/portfolio/football.jpg"
date = "2017-09-19T00:00:00+00:00"
title = "NFL In Game Win Probability"
weight = 0
+++

I did the NBA in game win probability, but I really wanted to do one for the NFL,
so here we are. This is all based on the great explanations at [Pro Football Reference](https://www.pro-football-reference.com/about/win_prob.htm), with some
more intermediate graphics and steps that helped me understand it better.

### In Game Probability

The first thing I wanted to do was to recreate the win probability laid out
that the score is a normal random variable, centered around the current point
differential. The sigma of the curve decreases linearly as the game progresses,
so the curve gets more pointy until the very end of the game, where there is
only a single outcome.

<select id="game-picker">
  <option value="1">WAS vs CIN, 10/30/2016 (Tie Game)</option>
  <option value="0">MIN vs CLE, 9/13/2009 (Just a Game)</option>
  <option value="2">BAL vs MIN, 12/8/2013 (Wild Last Two Minutes)</option>
  <option value="3">DET vs PHI, 12/8/2013 (Snow Bowl!)</option>
</select>

<div>
  <canvas id="chart"></canvas>
  <div style="color: #999999;">
    <div style="margin-top: 10px;">
      <div class="col-md-6 text-center"><span id="game-time"></span></div>
      <div class="col-md-6 text-center">Lead: <span id="lead"></span></div>
    </div>
    <div>
      <div class="col-md-4 text-center">Win: <span id="percent-win"></span>%</div>
      <div class="col-md-4 text-center">Tie: <span id="percent-tie"></span>%</div>
      <div class="col-md-4 text-center">Loss: <span id="percent-loss"></span>%</div>
    </div>
  </div>
  <input id="slider" type="range"/>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/Chart.js/2.7.0/Chart.bundle.min.js"></script>
  <script src="https://cdnjs.cloudflare.com/ajax/libs/decimal.js/7.2.4/decimal.min.js"></script>
  <script src="/js/igwip_nfl.js"></script>
</div>
<div style="margin-bottom: 20px;"></div>

Pretty fun, right? The data for this comes from nflscrapR author [Max Horowitz's Kaggle page](https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016). Without his
work, I don't believe there would be any good free data on the NFL.

## Including Expected Points
The previous win probabilities don't take into account the current state of
players on the field. If you are up by two, but the opposing team is at your 30
yard line with 10 seconds left, they'll probably kick a field goal and go home.
Right now this model doesn't account for this, but we can if we included the
expected number of points for their current drive.

I hope to get to this eventually ;)

## Additional Reading

* [PFR In Game Win Probability](https://www.pro-football-reference.com/about/win_prob.htm)
* [NFL Play by Play Data](https://www.kaggle.com/maxhorowitz/nflplaybyplay2009to2016)
* [Quarter By Quarter Probability](http://www.footballperspective.com/quarter-by-quarter-team-win-probability-added/)
* [CMU Expected Points Model](https://www.cmusportsanalytics.com/nfl-expected-points-nflscrapr-part-2-multinomial-logistic-regression/)

The image for this post can be found [here](https://unsplash.com/search/photos/american-football?photo=iezcEpGuYdE).
