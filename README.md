## Contents

- [About](#about)
- [Actions](#actions)
- [SASS](#sass)
- [Dark Mode](#dark-mode)

## About
A blog based on the Hyde theme for github pages.
This site costs me the price of the domain, $12/year, reach out if you're interested in doing the same.

## Actions
Theres a github action setup to rebuild the site at 06:30am UTC(12:30am CST) The yml file is in the .github directory.  
This keeps is mainly to keep the day counter in the currents.html updated everyday.

### Tokens
 * Settings > dev settings > repo token 
 * Repo Settings > secrets > new secret > name it USER_TOKEN > paste repo token

## SASS
Using the SASS from the Poole project I was able to move hyde from CSS to SASS. While I'm not taking advantage of everything SASS has to offer it is nice to have variables and partials. All partials are loaded in the styles.scss file, along with the google fonts using @import

## Dark Mode 
The 'Dark Mode' colors are set in the variables.scss file