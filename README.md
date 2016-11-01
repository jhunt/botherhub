A Github Nag Utility
====================

If you manage lots of small open source projects, and use the
Github Releases feature (which is *awesome*), you may be wondering
if there is a way to run a report on what repos have commits that
haven't been released, to aid in your release activities.

Hey!  That's what `github-nagger` does!

Usage is straightforward:

    github-nagger org/repo [org/repo...]

If you have lots of stuff under one org, you can use a neat bash
trick to ease the typing:

    github-nagger org/{repo1,other-repo,some-tools,etc}

Output is suitable for being emailed:

    $ ./check starkandwayne/{safe,shield,genesis}
    checking github.com/starkandwayne/safe... 
    starkandwayne/safe has 4 changes since the last release; and ought to be released
     5ad9934    Add Windows binary to pipeline             8 hours ago    James Hunt
     94989cd    Fix `safe get` single-value call output    8 hours ago    James Hunt
     d1e3d4e    Add test for single-value `get`            8 hours ago    James Hunt


    checking github.com/starkandwayne/shield... OK
    checking github.com/starkandwayne/genesis... 
    starkandwayne/genesis has 6 changes since the last release; and ought to be released
     caf0868    Fix minor bugs                                         3 days ago    James Hunt
     c368c4f    New `genesis update` command                           3 days ago    James Hunt
     0f52094    Only check/verify Releases / Stemcells / Index once    3 days ago    James Hunt
     d5a6cb0    More Finesse when handling BOSH directors              3 days ago    James Hunt
     6da79f3    Add env, site, type to name.yml                        3 days ago    James Hunt

Happy Releasing!
