# bestway
제일 좋은 것은 백업하고 지우고 다시 만드는 것.
 

# truncate-github-history

git clone https://github.com/lancard/$repository.git
cd $repository
git checkout --orphan temp $(LAST_COMMIT_HASH)
git commit -m "Truncate history"
git push origin temp
cd ..

# after that, change default repo to temp, and delete master.

# then, rename temp to master
