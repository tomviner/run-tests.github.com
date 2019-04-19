#!/usr/bin/env bash
{ set +x; } 2>/dev/null

# .travis.yml:
# script: curl -fLs https://shell-tests.github.io/ | bash -s

IFS=
! [ -e "tests" ] && echo "SKIP: tests/ NOT EXISTS" && exit
! [ -d "tests" ] && echo "SKIP: tests/ NOT A DIRECTORY" && exit
find="$(find "tests" -name '.*' -prune -o -type f ! -name ".*" -print)" || exit

scripts="$([[ -n "$find" ]] && while IFS= read f; do
    [ -f "$f" ] && file "$f" | awk -F":" '{print $2}' | grep -q "script" && echo "$f";:
done <<< "$find")" || exit
[[ -z "$scripts" ]] && echo "SKIP: tests/ public scripts not found" && exit

count="$(echo "$scripts" | wc -l | tr -d ' ')"
echo "tests/ - $count public scripts"
[[ -n "$scripts" ]] && while IFS= read f; do
    ( set -x; chmod +x "$f" ) || exit
    ( set -x; "$@" ) || exit
done <<< "$scripts";:
