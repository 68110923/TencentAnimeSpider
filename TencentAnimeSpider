

import requests
import re
import json

head = {}
head['User-Agent'] = "Mozilla/5.0 (compatible; MSIE 9.0; Windows NT 6.1; Trident/5.0;"
url = 'https://new.qq.com/ch/comic/'
response = requests.get(url,headers=head)
html = response.text
#print(html)
pat_1 = re.compile(r'({"app_id".*?"vurl".*?})',re.S)
ls = pat_1.findall(html)
print(len(ls))
for item in ls:
    data = json.loads(item)
    print(data['title'])
    print(data['intro'])
    print(data['category1_chn'],data['category2_chn'],data['category_chn'])
    print(data['vurl'])
    print(data['multi_imgs'])
    print(data['imgs'])
    print('='*60)



for page in range(1,10):
    print('page:',page)
    url = 'https://pacaio.match.qq.com/irs/rcd'
    params={
        'cid':'146',
        'token':'49cbb2154853ef1a74ff4e53723372ce',
        'ext':'comic',
        'page':page,
        'expIds':'20190225009411 | 20190225008985 | 20190225008966 | t0842g3m06a | 20190225008942 | 20190225008669 | 20190225008646 | 20190225008595 | b08429fk0q7 | 20190225008579 | 20190225008423 | 20190225008403 | 20190225008373 | g0842gyn3j9 | 20190225008363 | 20190225008344 | 20190225008324 | 20190225008306 | u08421d08my',
        'callback':'__jp7',
    }

    response = requests.get(url,params=params,headers=head)
    html = response.text
    pat_a = re.compile(r'"data":(.*?}])',re.S)
    ls = pat_1.findall(html)
    print(len(ls))
    for item in ls:
        data = json.loads(item)
        print(data['title'])
        print(data['intro'])
        print(data['category1_chn'],data['category2_chn'],data['category_chn'])
        print(data['vurl'])
        print(data['multi_imgs'])
        print('='*60) 
