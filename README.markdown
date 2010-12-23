h1. Import Mercurial/HG repositories to Git

This was copied from http://webonrails.com/2009/02/19/export-mercurialhg-repository-to-git-repository/ in case the source or repo goes down.

    git clone git://repo.or.cz/fast-export.git
    mkdir new_git_repo
    cd new_git_repo
    git init
    /path/to/hg-fast-export.sh -r /path/to/hg_repo #hg-fast-export.sh in the clone of step 1
    git-repack -a -d -f
    git checkout BRANCH_NAME # BRANCH_NAME is the name of Hg branch, in my case it was ‘trunk’
