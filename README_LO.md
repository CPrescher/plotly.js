# Modified version of plotly.js

This forked version of plotly.js contains a branch called ordiology that sources a local version of gl-heatmap2d that has been modified to create a discretised heatmap rather than an interpolated one.

The heatmapgl covert.js trace in the src code has also been modified to widen the bounds to fit the discretised gl-heatmap2d.

## Set up
### Cloning the repository
git clone https://github.com/ordiology/plotly.js
cd plotly.js
git checkout -b ordiology
touch testing-push
git add .
git commit -m "testing commit to branch"
git push --set-upstream origin ordiology

### Setting up the plotly test environment
mv package-lock.json package-lock-safe.json
npm install
npm audit fix
npm run pretest
npm start
