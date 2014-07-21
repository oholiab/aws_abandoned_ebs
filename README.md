What is it?
-----------
This is a utility for iterating over your aws accounts and regions and
hilighting any ebs volumes that are not currently marked as in-use.

It's a real hack, building on older code I used in the most ad-hoc way I could
so please do not consider this code good or tested. I can do better but time is
money :)

Output is in json format with a hash that contains an array of volume metadata
under the "volumes" key and stats for the various accounts and regions under the
"stats" key.

Usage
-----
This project depends on https://github.com/oholiab/awswrapper, which will be
automatically cloned to a subdirectory.

It should be invoked thusly:

    aws_abandoned_ebs account1 account2 ...

where account1 and account2 are accounts as defined in
https://github.com/oholiab/awswrapper/blob/master/README.md

Dependencies
------------
You will need ruby>=1.8.7, bundler (if you don't want to install the gems
in Gemfile manually), git and the aws command line utility.
