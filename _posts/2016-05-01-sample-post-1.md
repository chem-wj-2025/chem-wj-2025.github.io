---
layout: post
title:  "Sample Post - test"
categories: jekyll update
---




<h3>자막</h3>
<div id="subtitle-box" style="height: 300px; overflow-y: auto; border: 1px solid #ccc; padding: 1rem;"></div>

<h3>요약</h3>
<div id="summary-box" style="height: 200px; overflow-y: auto; border: 1px solid #ccc; padding: 1rem;"></div>

<style>
  #subtitle-box, #summary-box {
    font-family: 'Courier New', monospace;
    font-size: 1.1rem;
    white-space: pre-wrap;
    word-break: break-word;
    line-height: 1.8;
    color: black;
  }

  .chunk {
    opacity: 0;
    animation: fadeIn 1s forwards;
    margin-bottom: 1rem;
  }

  @keyframes fadeIn {
    to {
      opacity: 1;
    }
  }
</style>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    // ✅ 자막 - 한 줄씩 타이핑
    const subtitleLines = [
      "그런데 새로운 방법으로 등장해요.",
      "원격 교육은 기본적으로 매체를 써서 학습자랑 교수자가 떨어져 있는 컨셉이에요.",
      "일반적으로 블렌디드 러닝은 믹스했다 섞었다는 의미잖아요.",
      "온오프라인을 섞습니다. 그런데 그냥 무조건 섞으면 되냐? 아닙니다.",
      "면대면 학습과 온라인 학습을 의도적으로 결합해야 해요.",
      "왜 의도적으로 하냐? 그냥 하나만 하면 되지 않냐?",
      "각각의 방식이 장점이 있습니다.",
      "오프라인 강의는 돌려볼 수 없지만, 온라인 강의는 되돌릴 수도 있고 배속 재생도 가능하죠.",
      "그래서 그런 식으로..."
    ];

    const subtitleBox = document.getElementById("subtitle-box");
    let lineIndex = 0;
    let charIndex = 0;

    function typeLine() {
      if (lineIndex >= subtitleLines.length) return;

      const line = subtitleLines[lineIndex];
      if (charIndex < line.length) {
        subtitleBox.textContent += line[charIndex];
        charIndex++;
        subtitleBox.scrollTop = subtitleBox.scrollHeight;
        setTimeout(typeLine, 30);
      } else {
        subtitleBox.textContent += '\n';
        lineIndex++;
        charIndex = 0;
        setTimeout(typeLine, 300);
      }
    }

    typeLine();

    // ✅ 요약 - 덩어리 5초 간격 출력
    const textChunks = [
      "원격 교육은 매체를 활용해 교수자와 학습자가 떨어진 상태에서 진행되며, 블렌디드 러닝은 온라인과 오프라인 학습을 의도적으로 결합하는 방식이다.",
      "각각의 방식은 되돌려보기, 실시간 상호작용 등 고유한 장점이 있으며, 이를 조화롭게 활용하는 것이 중요하다."
    ];

    const summaryBox = document.getElementById("summary-box");
    let currentIndex = 0;

    function showNextChunk() {
      if (currentIndex < textChunks.length) {
        const p = document.createElement("p");
        p.className = "chunk";
        p.textContent = textChunks[currentIndex];
        summaryBox.appendChild(p);
        summaryBox.scrollTop = summaryBox.scrollHeight;
        currentIndex++;
        setTimeout(showNextChunk, 5000);
      }
    }

    showNextChunk();
  });
</script>
