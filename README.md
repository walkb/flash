# Flash
Submission for MHacks 17

Authors:
- [Walker Broadbent](https://github.com/walkb) (Frontend functionality, development, design)
- [supasuge](https://github.com/supasuge) (Backend functionality, Project planning, documentation)
- [Hiramw2](https://github.com/Hiramw2) (Presentation, project planning, frontend design)
- [Rahult4](https://github.com/Rahult4) (Presentation, project planning, user experience testing)

## Background
### My experience at MHacks 17
MHacks 17 was my first ever hackathon experience, and I would say it was a good one. I handled everything related to the front-end, with assistance on layout ideas and some testing from other members.

This is a separate copy of the repository so that I can continue to work on it and experiment in my free time. Please see [supasuge](https://github.com/supasuge) for the original public repository, and the [devpost](https://devpost.com/software/lectures-expedited).

### Future work
I will organize this project into two primary branches -- one will be the final product of the hackathon, and the other will be an updated version as I continue this project.

## Purpose
Learning outside of your courses can be difficult. A course generally has a lot of resources to improve your learning experience, but what about when you're just watching tutorials, lectures, etc., on YouTube? A lot of information slips away without spaced repetition, and the goal of this project is to solve that issue.

## Breaking it down
### Project Goal
Our initial goal was to allow the user to input a combination of documents (files, PDF, image, YouTube video URL, etc.) and generate study materials for the topic.

### Usage
Input a YouTube URL, specify whether you want a quiz, flashcards, select how many flashcards and questions you want, and then press submit!

### Technologies
- Backend: `Flask`, `openai`
- Frontend: `Next.js`, `React`
- API:
  - `Youtube Transcript API`: fetches full video transcript using YouTube's API
  - `OpenAI`: uses the YouTube transcript and queries in order to generate the study material
  - `Groq`: due to a lack of time, we were unable to use their larger selection of LLM to replace just OpenAI.

### Challenges
Our group had a large conflict of skills, which unfortunately was too difficult to overcome in the 24 hours we had to design and finish a project. However, having four people with varying backgrounds (despite the experience gap) was still better than having just two people when trying to plan the overall project and develop features. Regardless, we were able to create a simple but cool project, which I consider a success for my first ever Hackathon.

### What I learned
I was able to gain a lot of experience developing in a team environment, how LLM wrappers worked, and how to connect Next.js to a backend API.

### What's next?
- Explore other LLM, potentially one of the open source LLMs to make this project accessible.
- Continue improving the front-end design.
- Add export functionality for various file types
- Create a login system with authentication to store user data and potentially flashcards/quizzes/notes, etc.

### How to run the project 
#### Linux (Ubuntu)
To run the backend, first install dependencies:
- Activate a virtual environment
- `cd Backend/app`
- `pip install -r Backend/requirements.txt`
- `cd ..`

To make this simple, you can perform the following to run the backend flask API:

```bash
cd Backend
source env/bin/activate # Unix environment
.\env\Scripts\Activate.ps1 # Windows Environment
pip install -r requirements.txt
flask run
```

To run the frontend for the first time:
- Navigate to frontend directory, i.e.: `cd Frontend`
- `npm install`: Install node.js dependencies
- `npm run dev`: Run next.js development server
- `cd ..`: cd back into `/Flask`

OR you can simple run the script `start.sh` script. Note that this may require admin privileges.

This may require adding executable permissions to the shell script, which currently is only made for Linux.

  
#### Windows
```powershell
cd Backend
python -m venv wenv
.\wenv\Scripts\Activate.ps1
pip install -r requirements.txt
flask run
# open another terminal
cd ..\Frontend
npm install
npm run dev
```

