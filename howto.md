cd IdeaProject
git clone https://github.com/Rudenches/KotlinAsFirst2020.git
cd KotlinAsFirst2020
git remote add upstream-my https://github.com/Rudenches/KotlinAsFirst2021.git
git fetch upstream-my
git branch backport
git checkout backport
git cherry-pick d535f359...FETCH_HEAD
git remote add upstream-theirs https://github.com/MeeLeSh/KotlinAsFirst2021.git
git fetch upstream-theirs
git checkout master
git merge backport upstream-theirs/master
git remote -v
git add .
commit -m "."
git push