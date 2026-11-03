# THIRD PARTY NOTICES

사우나 고요(SAUNA GOYO)는 아래 오픈소스와 녹음 소리를 포함해 배포합니다. 각 라이선스 전문 또는 링크와 저작권 표기를 싣습니다.

| 구성요소 | 버전 | 라이선스 | 용도 |
|---|---|---|---|
| three.js | 0.128.0 | MIT | 3D 화면 그리기 (번들에 포함) |
| Pretendard | 1.3.9 | SIL Open Font License 1.1 | 화면 글꼴 (자체 호스팅) |
| Vite | 8.3.5 | MIT | 빌드 도구. 배포물에는 모듈 미리 불러오기용 작은 런타임 코드만 포함 |
| @vercel/analytics | 2.0.1 | MIT | Vercel Web Analytics 페이지 방문 집계 (번들에 포함, 같은 출처 `/_vercel/insights/script.js`만 불러옴) |
| Birds In The Morning (BurghRecords) | Freesound #554513 | CC0 1.0 | 외기욕 쉼터·고요 카페·노천탕 낮 새소리 (`public/sounds/birds.m4a`) |
| Yeongdong Summer Night – Insect Chorus Soundscape (Cheolmin_Lee) | Freesound #841277 | CC BY 4.0 | 노천탕 밤 풀벌레 소리 (`public/sounds/insects.m4a`) |

텍스처, 벽화, 풍경, 캐릭터는 모두 코드로 직접 생성하며 외부 에셋을 쓰지 않습니다. 소리도 코드로 합성하되, 새소리와 풀벌레 소리만 위 표의 녹음 파일을 씁니다.
빌드 도구는 배포물에 포함되지 않습니다(Vite의 작은 런타임 코드는 예외로 아래에 고지합니다). 실시간 서버(Cloudflare Worker)에는 외부 오픈소스 코드가 포함되지 않습니다.

---

## three.js (MIT)

- 저장소: https://github.com/mrdoob/three.js
- 버전: 0.128.0

```
The MIT License

Copyright © 2010-2021 three.js authors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
```

---

## Pretendard (SIL Open Font License 1.1)

- 저장소: https://github.com/orioncactus/pretendard
- 버전: 1.3.9
- Reserved Font Name: Pretendard
- 글꼴 파일은 수정하지 않고 그대로 배포합니다. 글꼴을 단독으로 판매하지 않습니다.

```
Copyright (c) 2021, Kil Hyung-jin (https://github.com/orioncactus/pretendard),
with Reserved Font Name Pretendard.

This Font Software is licensed under the SIL Open Font License, Version 1.1.
This license is copied below, and is also available with a FAQ at:
https://scripts.sil.org/OFL


-----------------------------------------------------------
SIL OPEN FONT LICENSE Version 1.1 - 26 February 2007
-----------------------------------------------------------

PREAMBLE
The goals of the Open Font License (OFL) are to stimulate worldwide
development of collaborative font projects, to support the font creation
efforts of academic and linguistic communities, and to provide a free and
open framework in which fonts may be shared and improved in partnership
with others.

The OFL allows the licensed fonts to be used, studied, modified and
redistributed freely as long as they are not sold by themselves. The
fonts, including any derivative works, can be bundled, embedded, 
redistributed and/or sold with any software provided that any reserved
names are not used by derivative works. The fonts and derivatives,
however, cannot be released under any other type of license. The
requirement for fonts to remain under this license does not apply
to any document created using the fonts or their derivatives.

DEFINITIONS
"Font Software" refers to the set of files released by the Copyright
Holder(s) under this license and clearly marked as such. This may
include source files, build scripts and documentation.

"Reserved Font Name" refers to any names specified as such after the
copyright statement(s).

"Original Version" refers to the collection of Font Software components as
distributed by the Copyright Holder(s).

"Modified Version" refers to any derivative made by adding to, deleting,
or substituting -- in part or in whole -- any of the components of the
Original Version, by changing formats or by porting the Font Software to a
new environment.

"Author" refers to any designer, engineer, programmer, technical
writer or other person who contributed to the Font Software.

PERMISSION & CONDITIONS
Permission is hereby granted, free of charge, to any person obtaining
a copy of the Font Software, to use, study, copy, merge, embed, modify,
redistribute, and sell modified and unmodified copies of the Font
Software, subject to the following conditions:

1) Neither the Font Software nor any of its individual components,
in Original or Modified Versions, may be sold by itself.

2) Original or Modified Versions of the Font Software may be bundled,
redistributed and/or sold with any software, provided that each copy
contains the above copyright notice and this license. These can be
included either as stand-alone text files, human-readable headers or
in the appropriate machine-readable metadata fields within text or
binary files as long as those fields can be easily viewed by the user.

3) No Modified Version of the Font Software may use the Reserved Font
Name(s) unless explicit written permission is granted by the corresponding
Copyright Holder. This restriction only applies to the primary font name as
presented to the users.

4) The name(s) of the Copyright Holder(s) or the Author(s) of the Font
Software shall not be used to promote, endorse or advertise any
Modified Version, except to acknowledge the contribution(s) of the
Copyright Holder(s) and the Author(s) or with their explicit written
permission.

5) The Font Software, modified or unmodified, in part or in whole,
must be distributed entirely under this license, and must not be
distributed under any other license. The requirement for fonts to
remain under this license does not apply to any document created
using the Font Software.

TERMINATION
This license becomes null and void if any of the above conditions are
not met.

DISCLAIMER
THE FONT SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO ANY WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT
OF COPYRIGHT, PATENT, TRADEMARK, OR OTHER RIGHT. IN NO EVENT SHALL THE
COPYRIGHT HOLDER BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY,
INCLUDING ANY GENERAL, SPECIAL, INDIRECT, INCIDENTAL, OR CONSEQUENTIAL
DAMAGES, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING
FROM, OUT OF THE USE OR INABILITY TO USE THE FONT SOFTWARE OR FROM
OTHER DEALINGS IN THE FONT SOFTWARE.
```

---

## Vite (MIT)

- 저장소: https://github.com/vitejs/vite
- 버전: 8.3.5

```
MIT License

Copyright (c) 2019-present, VoidZero Inc. and Vite contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## @vercel/analytics (MIT)

- 저장소: https://github.com/vercel/analytics
- 버전: 2.0.1

```
The MIT License (MIT)

Copyright (c) 2026 Vercel, Inc.

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 녹음 소리

### Birds In The Morning (CC0 1.0)

- 제목: Birds In The Morning
- 작성자: BurghRecords
- 주소: https://freesound.org/people/BurghRecords/sounds/554513/
- 라이선스: CC0 1.0 Universal (퍼블릭 도메인 기증), https://creativecommons.org/publicdomain/zero/1.0/
- 배포 파일: `public/sounds/birds.m4a`
- 변경 내용: 56초 구간을 잘라 내고, 끝과 처음을 4초 겹쳐 반복용으로 이음. 모노로 합치고, 가까운 새 울음이 튀지 않게 음량을 고르게 다듬고 키움. AAC(56kbps)로 인코딩.
- CC0라 표기 의무는 없지만 출처를 밝혀 둡니다.

### Yeongdong Summer Night – Insect Chorus Soundscape (CC BY 4.0)

- 제목: Yeongdong Summer Night – Insect Chorus Soundscape
- 작성자: Cheolmin_Lee
- 주소: https://freesound.org/people/Cheolmin_Lee/sounds/841277/
- 라이선스: Creative Commons Attribution 4.0 International (CC BY 4.0), https://creativecommons.org/licenses/by/4.0/
- 배포 파일: `public/sounds/insects.m4a`
- 변경 내용: 32초 구간을 잘라 내고, 끝과 처음을 4초 겹쳐 반복용으로 이음. 모노로 합치고 음량을 키움. AAC(48kbps)로 인코딩.
- 원 저작물에 대한 보증은 없으며(CC BY 4.0 제5조), 작성자가 이 서비스를 후원하거나 보증하지 않습니다.
