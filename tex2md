#!/usr/bin/python

# purpose:
# enclose $math$ environments within `backticks`

import re
import os
import sys

if len(sys.argv) != 2 or not os.path.isfile(sys.argv[1]):
    print 'bad filename argument'
    sys.exit(1)

s = open(sys.argv[1]).read()
s = re.sub('\$\$(?P<id>[^\$]+)\$\$', '`$$\g<id>$$`', s)
s = re.sub('(?P<ld>[^$])\$(?P<id>[^\$]+)\$(?P<ed>[^$])',
    '\g<ld>`$\g<id>$`\g<ed>', s)

print s,
