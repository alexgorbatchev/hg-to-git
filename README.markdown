# Import Mercurial/HG repositories to Git

This was copied from [WebOnRails](http://webonrails.com/2009/02/19/export-mercurialhg-repository-to-git-repository/) in case the source or repo goes down.

    git clone git://github.com/alexgorbatchev/hg-to-git.git
    hg clone http://...
    mkdir new_git_repo
    cd new_git_repo
    git init
    cd ../new_git_repo
    ../hg-to-git/hg-fast-export.sh -r ../your_hg_project
    git repack -a -d -f
    git checkout master

You will need `mercurial` Python egg

    easy_install mercurial

