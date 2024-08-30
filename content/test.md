<!DOCTYPE html>
<html lang="ko">

<head>
  <meta charset="UTF-8">
  <title>HTML 각주 예시</title>
  <style>
    sup {
      font-size: 0.75em;
    }

    .footnotes {
      border-top: 1px solid #ddd;
      padding-top: 1em;
      font-size: 0.85em;
    }
  </style>
</head>

<body>
  <p>이것은 각주가 필요한 문장입니다.<sup><a href="#footnote1" class="footnote-ref">[1]</a></sup></p>
  <p>여기 또 다른 각주가 있습니다.<sup><a href="#footnote2" class="footnote-ref">[2]</a></sup></p>
  
  <p>
      a
      a
      aa

      a
      a
      a
      a
      a
      a
      a
      a
      a

      a
      a
      a
      a

      a
      a

      a
      a
      a

      a

      a
      a

      a

      a
      a

      a
      a
      a
      a

      a
      a
      a

      a
      a
      a

      aaa
      a

      a
      a
      a

      a
      a

      a
      a
      a

      a
      a

      a
      a
      a

      a
      a
      a

      a
      a
      a

      a
      a

      a
      a

      a
      a
      a

      a
      a
      a

      a
      a

      a
      a

      a
      a
      a
      a

      a
      a

      a
      a

      aaa

      aa
      a

      a
      a
      a

      a
      a
      a
      a
      a
      aa
      a
      a
      a
      a
      a
      a
      a
      a

      a
      a
      a

      a
      a

      a
      a
      a

      a
      a
      a
      a
      a

      a
      a
      a
      a

      a
      a

      a
      a
      a

      a
      a
      a

      a
      a
      a

      a
      a

      a
      a
      a

      a


  </p>

  <div class="footnotes">
    <hr>
    <ol>
      <li id="footnote1">첫 번째 각주 내용입니다. <a href="#" class="footnote-backref" data-ref="footnote1">↩</a></li>
      <li id="footnote2">두 번째 각주 내용입니다. <a href="#" class="footnote-backref" data-ref="footnote2">↩</a></li>
    </ol>
  </div>

  <script>
    document.addEventListener('DOMContentLoaded', (event) => {
      // 각주 참조 클릭 이벤트
      document.querySelectorAll('.footnote-ref').forEach(link => {
        link.addEventListener('click', function (e) {
          e.preventDefault();
          const targetId = this.getAttribute('href').slice(1);
          const targetElement = document.getElementById(targetId);
          if (targetElement) {
            targetElement.scrollIntoView({behavior: 'smooth'});
          }
        });
      });

      // 각주에서 본문으로 돌아가는 링크 클릭 이벤트
      document.querySelectorAll('.footnote-backref').forEach(link => {
        link.addEventListener('click', function (e) {
          e.preventDefault();
          const refId = this.getAttribute('data-ref');
          const refs = document.querySelectorAll(`a[href="#${refId}"]`);
          if (refs.length > 0) {
            refs[0].scrollIntoView({behavior: 'smooth'});
          }
        });
      });
    });
  </script>
</body>

</html>
