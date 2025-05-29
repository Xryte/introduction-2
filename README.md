echo "Репозиторий с ветками" > README.md
git add README.md
git commit -m "Добавил README.md"
git push -u origin main

git checkout -b other
touch other.txt
git add other.txt
git commit -m "Добавил файл main.txt на ветку main"
git push -u origin other

git checkout main
touch main.txt
git add main.txt
git commit -m "Добавил файл main.txt на ветку main"
git push

git merge other -m "Слияние ветки other в main"
git push
