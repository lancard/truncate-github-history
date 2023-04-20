# truncate-github-history

git clone https://github.com/lancard/$repository.git
cd $repository
git checkout --orphan temp $(LAST_COMMIT_HASH)
git commit -m "Truncate history"
git push origin temp
cd ..

# after that, change default repo to temp, and delete master.

# then, rename temp to master
