VERSION CONTROL 

Version control, also known as source control, is a system that tracks and manages changes to code or documents over time. It allows teams to collaborate, revert to previous versions, and easily track any changes made. In essence, it's a way to maintain a history of modifications, making it easier to manage complex projects and recover from errors. 

IMPORTANCE OF VERSION CONTROL

TRACK CHANGES OVERTIME:
VCS allow developers to track every modification made to the codebase. This means you can always go back to previous versions, ensuring no change are lost.

COLLABORATION:
VCS simplify collaboration between team members. Everyone can work on different parts of the project without worrying about overwriting each other's work.

CODE HISTORY AND AUDIT TRAILS: With version control, you can see who made specific changes, when they were made and why. This audit trail is invaluable for debugging, reviewing or maintaining code.

BACKUP AND RECOVERY: Version control systems provide a way to back up your project. If something goes wrong, you can easily recover previous versions.

BRANCHING AND MERGING:
You can create branches for different features or bug fixes, allowing multiple developers to work simultaneously without interfering with each other’s code. Once the work is complete, the branches can be seamlessly merged back into the main project.

GIT

Git is a distributed version central system (VCS) that help users to track changes in their code base, collaborate with other users and manage multiple versions of a project. Simply put, Git is use to back up a code. Git is decentralized, which means it does not require a central server.

GITHUB

Is a web-base platform designed for version control and collaboration. It host git repositories (remote repo) and provides interface to manage your code.
Github offers remote services and also provides a space for easy collaborations between developers.

DIFFERENCE BETWEEN GIT AND GITHUB

Git: Git is a distributed version control system for tracking changes in source code during software development. Git is a software, a command-line tool. Git is installed locally on the system.

GitHub: GitHub is a web-based Git repository hosting service, which offers all of the distributed revision control and source code management (SCM) functionality of Git as well as adding its own features. GitHub is a service, a graphical user interface hosted on the web.

COMPREHENSIVE GIT AND GITHUB SETUP FOR BEGINNERS

On Linux (Ubuntu)

1. Install Git
	sudo apt update
	sudo apt install git

2. Configure Git (One-time setup)
Set your name and email (used for commits):
	git config --global user.name "Your Name"
	git config --global user.email "you@example.com"

3. Generate SSH Key (to connect GitHub)
	Step 1: Generate the SSH key
		ssh-keygen -t ed25519 -C "you@example.com"

		Press Enter 3 times to accept the defaults.

	Step 2: Add your SSH key to the SSH agent
		eval "$(ssh-agent -s)"
		ssh-add ~/.ssh/id_ed25519

	Step 3: Add the public key to GitHub
		cat ~/.ssh/id_ed25519.pub

		Copy the output.
		Go to GitHub > Settings > SSH and GPG keys > New SSH key.
		Paste the key, give it a name (e.g., "My localPC").

4. Create a GitHub Repository

	Go to https://github.com
	Click New Repository
	Give it a name, e.g., my-first-repo

	Leave all default settings and click Create Repository

5. Initialize a Local Git Repo

	mkdir git-setup
	cd git-setup
	git init
	touch README.md
	echo "# My First Repo" >> README.md
	git add .
	git commit -m "Initial commit"

6. Connect Local Repo to GitHub

	git remote add origin git@github.com:yourusername/my-first-repo.git
	git branch -M main
	git push -u origin main


