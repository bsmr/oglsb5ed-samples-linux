Some commands used to cleanup/organize the code:

Create .gitignore files for executables in Linux tree:

    for M in $(find "Linux" -type f -iname 'Makefile' | sort) ; do P=$(dirname $M) ; E=$(cat $M | grep '^MAIN' | awk -F' = ' '{ print $2 }') ; echo -e "# ignore executeable\n${E}" >"$P/.gitignore" ; done

# EOF
