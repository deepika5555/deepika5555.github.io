
# Clone repository (only needed first time)
git clone https://github.com/yourusername/portfolio.git

# Navigate to project directory
cd portfolio

# Ensure NVM is available
source ~/.nvm/nvm.sh

# Install and use Node.js 18 (Gatsby requirement)
nvm install 18
nvm use 18

# Install global dependencies
npm install -g yarn
npm install -g gatsby-cli

# Clear cache (helps prevent build issues)
gatsby clean

# Install project dependencies with legacy peer deps flag
yarn install --legacy-peer-deps
# OR if using npm
# npm install --legacy-peer-deps

# Increase Node memory limit (prevents segmentation faults)
export NODE_OPTIONS="--max-old-space-size=8192"

# Make your changes to the site as needed

# Add your changes to git
git add .
git commit -m "deploying changes"
git push origin main  # or whatever your default branch is

# Build and deploy
gatsby build
npm run deploy

<!-- gatsby develop -->  use this for local development
gatsby develop


Troubleshooting Tips:
export NODE_TLS_REJECT_UNAUTHORIZED=0
rm -rf node_modules package-lock.json yarn.lock
npm cache clean --force

npm rebuild sharp
npm rebuild
