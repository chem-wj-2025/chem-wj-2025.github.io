---
layout: post
title:  "Sample Post - test"
categories: jekyll update
---




---
layout: post
title:  "Sample Post - Typing Test"
---

<div id="typewriter"></div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const text = `그런데 새로운 방법으로 등장해요. 원격 교육은 일단 기본적으로 매체를 쓰긴 하지만 일단은 매체를 써서 학습자랑 교수자가 떨어져 있는 컨셉이에요. 일반적으로 블렌디드 러닝은 블렌디드 라는게 믹스했다 섞었다는 의미잖아요.

온오프라인을 섞습니다. 근데 뭐냐면 이런 컨셉이에요. 그냥 무조건 섞으면 되냐? 아닙니다.

면대면 학습과 온라인 학습을 의도적으로 결합해야 돼요. 의도적인 게 중요한 거예요. 왜 의도적으로 하냐? 그냥 하나만 하지.

뭐 하루 두 개 하냐 하는데 각각의 방식이 장점이 있습니다. 분명히 장점이 있어요. 예를 들어서 오프라인 강의는 돌려볼 수 있습니까? 못 본단 말이에요.

시간을 돌릴 수 없잖아요. 못 돌리니까. 온라인 강의는 보다가 이렇게 돌릴 수도 있고.

교수님이 좀 약간 말씀 느리시다. 그러면 1.5배 이렇게 하시잖아요. 심지어 2배속 하는 분들도 있고.

그래서 그런 식으로`;

    const container = document.getElementById("typewriter");
    let i = 0;

    function typeNext() {
      if (i < text.length) {
        container.innerHTML += text[i] === '\n' ? '<br>' : text[i];
        i++;
        setTimeout(typeNext, 30);
      }
    }

    typeNext();
  });
</script>

<style>
  #typewriter {
    font-family: 'Courier New', monospace;
    font-size: 1.2rem;
    white-space: pre-wrap;
    word-break: break-word;
    line-height: 1.8;
    color: black;
  }
</style>
