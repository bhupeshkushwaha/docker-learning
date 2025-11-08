# 🐳 docker-learning

A collection of Docker learning exercises, practical examples, and mini-projects — from container basics to advanced deployment workflows. This repository collects small, focused projects you can run locally with Docker and Docker Compose to practice real-world patterns.

---

## 📘 Overview
This repo is organized as short, self-contained exercises and example projects. Each top-level folder is a day/topic or a small demo you can open, run, and modify. The goal is hands-on learning: read the notes, build the images, run containers, and iterate.

---

## 🗂️ Top-level contents
The repository currently contains these top-level entries (projects and demo folders):

- `my-html-docker/` — simple static HTML Docker examples
- `php-nextjs-docker-boilerplate/` — PHP + Next.js example with Docker Compose
- `php-react-docker-boilerplate/` — PHP + React boilerplate
- `python-setup/` — small Python Docker examples and tooling
- `python-web-app/` — example Python web app with Docker Compose
- `resume-html-tailwind/` — resume/portfolio HTML + Tailwind project
- `tailresume/` — Tailwind + PHP resume project (nginx + php examples)
- `tailresume-git-backup/` — local git backup data (hidden repo contents)

Files:

- `abc.md` — project/notes (TailResume overview)
- `.gitmodules` — submodule configuration (if present)

> Note: some subfolders may themselves be Git repositories (embedded repos). See the "About embedded repos" section below.

---

## 💻 Quick start
Clone the repository and inspect the folders you want to try.

```powershell
git clone https://github.com/bhupeshkushwaha/docker-learning.git
cd docker-learning
```

Open any demo folder (for example `tailresume`) and follow its README. Many demos include a `Dockerfile` and/or `docker-compose.yml` for quick runs.

Examples (run from a demo folder):

```powershell
# build an image in the current folder (if a Dockerfile exists)
docker build -t demo:latest .

# run a container
docker run -d -p 8080:80 demo:latest

# list running containers
docker ps
```

---

## 📝 About embedded repos / submodules
This workspace currently contains some nested repositories. When you add a folder that itself contains a `.git` directory, Git shows a warning because clones of this parent repo won't include the nested repo history.

You have three safe options:

1. Keep the nested repos as independent projects (recommended if they have their own remotes): push each nested repo to its own remote and convert them to proper submodules using `git submodule add <url> <path>`.
2. Import the nested repo into this parent repository (remove the nested `.git` folder) so the parent repo stores the files directly (this loses the nested repo history locally unless backed up).
3. Remove the nested paths from the parent index with `git rm --cached -r <path>` so the parent repo doesn't try to track them.

If you want, I can prepare the commands for any of the above approaches for each nested folder.

---

## 📚 How to use this repo for learning
- Pick a folder (start with `my-html-docker` or `tailresume`).
- Read its README or notes.md.
- Build the image and run using Docker or Docker Compose.
- Tweak the code or Dockerfile to see how changes affect the build/runtime.

---

## 🧩 Notable projects inside this repo
- `tailresume/` — a TailwindCSS + PHP resume/portfolio that shows a small production-like nginx + php setup.
- `resume-html-tailwind/` — another resume example with Tailwind and Docker.

---

## 🧑‍💻 Author
Bhupesh Kushwaha  
Full Stack Developer | Solution Architect | DevOps Enthusiast  
Website: thebhupesh.com  
Email: bhupesh.web.developer@gmail.com

---

## � Topics
docker, devops, containers, learning, tutorial, docker-compose, cloud, microservices

---

If you'd like, I can also:
- convert nested projects into submodules (I can prepare commands and push instructions),
- import any nested repo into this parent repo,
- or create matching learning repos for `kubernetes-learning`, `aws-learning`, and `ci-cd-learning`.

Tell me which of the above you'd like me to execute next.