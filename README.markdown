h1. Import Mercurial/HG repositories to Git

This was copied from [WebOnRails](http://webonrails.com/2009/02/19/export-mercurialhg-repository-to-git-repository/) in case the source or repo goes down.

    git clone git://github.com/alexgorbatchev/hg-to-git.git
    mkdir new_git_repo
    cd new_git_repo
    git init
    cd ..
    hg-to-git/hg-fast-export.sh -r ./new_git_repo
    git-repack -a -d -f
    git checkout BRANCH_NAME
