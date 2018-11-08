#!/usr/bin/env python3
# -*- coding: utf-8 -*-

from urllib import request
import re

with request.urlopen('') as f:
    data = f.read()
    print('Status:',f.status,f.reason)
    for k,v in f.getheaders():
	    print('%s:%s' % (k,v))
    print ('Data:',data.decode('utf-8'))