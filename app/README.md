# Quick Install

Documented by [The Model.earth Project Team](/io)

[Earthscape](https://model.earth/earthscape/) is a fork of [Chatbot UI](https://github.com/mckaywrigley/chatbot-ui) by [Nick Wrigley](https://twitter.com/mckaywrigley).  

These steps are based on [github.com/mckaywrigley/chatbot-ui](https://github.com/mckaywrigley/chatbot-ui)

1.) Fork and clone the [Earthscape fork of Chatbot UI](https://github.com/modelearth/earthscape/) to your local desktop.

2.) Confirm your python and conda versions are current.

	python -V && conda -V

If older than python 3.12 and conda 23.3, [see our upgrade notes](https://model.earth/io/coders/python/).

3.) You can create a virtual environment using conda to avoid dependencies/version issues on your computer.

By using conda, no extra env files will reside in your repo. Choose y.

	conda create --name myenv &&
	conda activate myenv && conda --v

Or you can reuse the existing .gitignore: .env\*.local by adding X:

	python3 -m venv .envX.local &&
	source .envX.local/bin/activate

4.) In the local repo:

	run npm install &&
	brew install supabase/tap/supabase

For Windows [see detailed steps](../)

5.) Start Docker on your computer. If you don't have Docker on your computer yet, [Install Docker](https://docs.docker.com/get-docker/).

You should see a whale icon at the top.
Click to see a green dot to confirm it is running.

	docker pull supabase/postgres

6.) This step takes a while since Docker needs to pull images and create the containers.

	supabase start &&
	cp .env.local.example .env.local

7.) Run this to get the configuration information needed.

	supabase status

8.) run cp .env.local.example .env.local as specified in the readme.

	cp .env.local.example .env.local

9.) Open the .env.local file (note it might be a hidden file in the repo).

10.) Fill in the the configuration information obtained from step 5.

NEXT\_PUBLIC\_SUPABASE\_URL  
NEXT\_PUBLIC\_SUPABASE\_ANON\_KEY  
SUPABASE\_SERVICE\_ROLE_KEY

11.) Run

	npm run chat

12.) Add some global API Keys in the file: .env.local.example

NOTE: [Hosted site](https://www.chatbotui.com) seems to only work with a ChatGPT key.


## Run update

When you return to edit, update your local files:

	npm run update

<!-- WE ARE LOCAL, not needed
If you run a hosted instance you'll also need to run: 
TO DO: Add link on "hosted instance" to provide clarity.

	npm run db-push

conda env create -f environment.yml
-->


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

Next, we'll add [steps for deploying NextJS to Github](https://www.freecodecamp.org/news/how-to-deploy-next-js-app-to-github-pages/) without Vercel.

We will also docment how to sync from Github to a site hosted with our [Cloudflare&nbsp;Setup](https://model.earth/localsite/start/cloudflare/).


## The Free Energy Principle

The free energy principle is a theoretical framework suggesting that the brain reduces surprise or uncertainty by making predictions based on internal models and updating them using sensory input. It highlights the brain's objective of aligning its internal model with the external world to enhance prediction accuracy.

#### Natural Intelligence vs Artificial Intelligence

[Verses AI - Genius Beta Signup](https://www.verses.ai/genius)
Unlike AI trained on enormous datasets to excel at pattern recognition and reconstruction, Verses AI "Genius" utilizes nature-inspired biological processes to generate agents and collaborate to exhibit the dynamic behaviors of autonomous intelligent systems. This enables Verses to manage uncertainty and risk as it strives to create safe and sustainable environments at&nbsp;scale.