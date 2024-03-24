# Quick Install

Documented by [The Model.earth Project Team](/io)

[Earthscape](../) is a fork of [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) by [Nick Wrigley](https://twitter.com/mckaywrigley).  

These steps are from: [github.com/mckaywrigley/chatbot-ui](https://github.com/mckaywrigley/chatbot-ui), but you may need to setup a virtual environment using conda in order to avoid dependencies/version issues on your computer. 

1. Clone the forked repo to local desktop.
2. Create and activate a new virtual environment using conda (may skip this if don't want to use the virtual environment)
3. cd into the repository, run npm install and brew install supabase/tap/supabase (I'm a MacOS)
4. run supabase start, but before that make sure Docker is installed and running on you computer. This step takes a while since Docker needs to pull images and create the containers.
5. run supabase status. This should gives the configuration information needed.
6. run cp .env.local.example .env.local as specified in the readme.
7. Open the .env.local file (note it might be a hidden file in the repo), fill in the NEXT_PUBLIC_SUPABASE_URL, NEXT_PUBLIC_SUPABASE_ANON_KEY and SUPABASE_SERVICE_ROLE_KEY information by using the configuration information obtained from step 5.
8. npm run chat. 

Kudos to Ziyao!
<br>

## Local Setup

[Install Docker](https://docs.docker.com/get-docker/) if you don't have it on your computer yet.

Fork and clone our repo from [github.com/modelearth/earthscape](https://github.com/modelearth/earthscape/)

In your webroot run:
Note, this is not the conda virtual environment.
You might need to use a conda virtual environment if other errors occur.

	git clone https://github.com/modelearth/earthscape.git earthscape &&
	cd earthscape

Start a virtual environment folder.
Add X to reuse the existing .gitignore: .env\*.local

	python3 -m venv .envX.local &&
	source .envX.local/bin/activate

Question for Ziyao: If running in conda, does the .gitignore need to be modified?


## Run update

	npm run update

If you run a hosted instance you'll also need to run: 
TO DO: Add link on "hosted instance" to provide clarity.

	npm run db-push


Mac cmd. For Windows [see detailed steps](../)

	brew install supabase/tap/supabase

Start superbase and fill secrets:

	supabase start &&
	cp .env.local.example .env.local &&
	supabase status


Add some global API Keys in the file: .env.local.example
NOTE: [Hosted site](https://www.chatbotui.com) seems to only work with a ChatGPT key.

<!--
## Current Errors

Errors are occurring because Docker was not yet configured.
TO DO: Please add Docker setup info above.

npm run update
failed to connect to postgres: failed to connect to host=127.0.0.1 user=postgres database=postgres: dial error (dial tcp 127.0.0.1:54322: connect: connection refused)

supabase start
failed to start docker container: Error response from daemon: Mounts denied: approving /Users/helix/Library/Data/earthscape/supabase/functions: file does not exist

supabase status
Error response from daemon: No such container: supabase_db_chatbotui
-->

## Run NextJS using Github Pages

Next, please add [steps for deploying NextJS to Github](https://www.freecodecamp.org/news/how-to-deploy-next-js-app-to-github-pages/) without Vercel.

We will also docment how to sync from Github to a site hosted with our [Cloudflare&nbsp;Setup](https://model.earth/localsite/start/cloudflare/).


## The Free Energy Principle

The free energy principle is a theoretical framework suggesting that the brain reduces surprise or uncertainty by making predictions based on internal models and updating them using sensory input. It highlights the brain's objective of aligning its internal model with the external world to enhance prediction accuracy.

#### Natural Intelligence vs Artificial Intelligence

[Verses AI - Genius Beta Signup](https://www.verses.ai/genius)
Unlike AI trained on enormous datasets to excel at pattern recognition and reconstruction, Verses AI "Genius" utilizes nature-inspired biological processes to generate agents and collaborate to exhibit the dynamic behaviors of autonomous intelligent systems. This enables Verses to manage uncertainty and risk as it strives to create safe and sustainable environments at&nbsp;scale.