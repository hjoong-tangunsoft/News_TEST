<style>
:root {
  --cursor-color: #8b5cf6;
  --copilot-color: #0969da;
  --claude-color: #ff6b35;
  --jetbrains-color: #e91e63;
  --bg-color: #ffffff;
  --card-bg: #f8fafc;
  --text-primary: #1e293b;
  --text-secondary: #64748b;
  --border-color: #e2e8f0;
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-md: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
  --gradient-cursor: linear-gradient(135deg, #8b5cf6 0%, #7c3aed 100%);
  --gradient-copilot: linear-gradient(135deg, #0969da 0%, #0550ae 100%);
  --gradient-claude: linear-gradient(135deg, #ff6b35 0%, #f4511e 100%);
  --gradient-jetbrains: linear-gradient(135deg, #e91e63 0%, #c2185b 100%);
}

* {
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', 'Noto Sans', Helvetica, Arial, sans-serif;
  line-height: 1.6;
  color: var(--text-primary);
  background: var(--bg-color);
  margin: 0;
  padding: 0;
}

.container {
  max-width: 900px;
  margin: 0 auto;
  padding: 2rem 1rem;
}

/* Header Styles */
.header {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
  padding: 3rem 2rem;
  border-radius: 12px;
  margin-bottom: 2rem;
  box-shadow: var(--shadow-lg);
  text-align: center;
}

.header h1 {
  margin: 0 0 0.5rem 0;
  font-size: 2.5rem;
  font-weight: 700;
  text-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
}

.header .subtitle {
  font-size: 1.1rem;
  opacity: 0.95;
  margin: 0;
}

/* Index Styles */
.index-section {
  background: var(--card-bg);
  border-radius: 12px;
  padding: 1.5rem;
  margin-bottom: 2rem;
  box-shadow: var(--shadow-md);
  border-left: 4px solid #667eea;
}

.index-section h2 {
  margin-top: 0;
  color: var(--text-primary);
  font-size: 1.5rem;
}

.index-links {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
  gap: 0.75rem;
  list-style: none;
  padding: 0;
  margin: 0;
}

.index-links li {
  margin: 0;
}

.index-links a {
  display: block;
  padding: 0.75rem 1rem;
  background: white;
  border-radius: 8px;
  text-decoration: none;
  color: var(--text-primary);
  transition: all 0.2s ease;
  border: 1px solid var(--border-color);
  font-weight: 500;
}

.index-links a:hover {
  background: #667eea;
  color: white;
  transform: translateY(-2px);
  box-shadow: var(--shadow-md);
}

/* Card Styles */
.card {
  background: white;
  border-radius: 12px;
  padding: 2rem;
  margin-bottom: 2rem;
  box-shadow: var(--shadow-md);
  border-top: 4px solid var(--border-color);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.card:hover {
  transform: translateY(-2px);
  box-shadow: var(--shadow-lg);
}

.card.cursor {
  border-top-color: var(--cursor-color);
}

.card.copilot {
  border-top-color: var(--copilot-color);
}

.card.claude {
  border-top-color: var(--claude-color);
}

.card.jetbrains {
  border-top-color: var(--jetbrains-color);
}

.card h2 {
  margin-top: 0;
  font-size: 2rem;
  font-weight: 700;
  color: var(--text-primary);
  padding-bottom: 0.5rem;
  border-bottom: 2px solid var(--border-color);
}

.card.cursor h2 {
  color: var(--cursor-color);
  border-bottom-color: var(--cursor-color);
}

.card.copilot h2 {
  color: var(--copilot-color);
  border-bottom-color: var(--copilot-color);
}

.card.claude h2 {
  color: var(--claude-color);
  border-bottom-color: var(--claude-color);
}

.card.jetbrains h2 {
  color: var(--jetbrains-color);
  border-bottom-color: var(--jetbrains-color);
}

.card h3 {
  font-size: 1.5rem;
  font-weight: 600;
  margin-top: 1.5rem;
  margin-bottom: 1rem;
  color: var(--text-primary);
}

.card h4 {
  font-size: 1.25rem;
  font-weight: 600;
  margin-top: 1rem;
  margin-bottom: 0.75rem;
  color: var(--text-secondary);
}

/* Table Styles */
.overview-table {
  width: 100%;
  border-collapse: collapse;
  margin: 1.5rem 0;
  background: white;
  border-radius: 8px;
  overflow: hidden;
  box-shadow: var(--shadow-sm);
}

.overview-table thead {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
  color: white;
}

.overview-table th {
  padding: 1rem;
  text-align: left;
  font-weight: 600;
  font-size: 0.95rem;
  text-transform: uppercase;
  letter-spacing: 0.5px;
}

.overview-table td {
  padding: 1rem;
  border-bottom: 1px solid var(--border-color);
}

.overview-table tbody tr:hover {
  background: var(--card-bg);
}

.overview-table tbody tr:last-child td {
  border-bottom: none;
}

/* Info Box Styles */
.info-box {
  background: var(--card-bg);
  border-left: 4px solid #667eea;
  border-radius: 8px;
  padding: 1.25rem;
  margin: 1.5rem 0;
}

.info-box ul {
  margin: 0.5rem 0;
  padding-left: 1.5rem;
}

.info-box li {
  margin: 0.5rem 0;
}

/* Blockquote Styles */
blockquote {
  border-left: 4px solid #667eea;
  background: var(--card-bg);
  padding: 1.25rem 1.5rem;
  margin: 1.5rem 0;
  border-radius: 8px;
  font-style: italic;
  color: var(--text-secondary);
}

/* Link Styles */
a {
  color: #667eea;
  text-decoration: none;
  font-weight: 500;
  transition: color 0.2s ease;
}

a:hover {
  color: #764ba2;
  text-decoration: underline;
}

/* List Styles */
ul, ol {
  padding-left: 1.5rem;
}

li {
  margin: 0.5rem 0;
}

/* Highlight Section */
.highlight-section {
  background: linear-gradient(135deg, #f6f8fa 0%, #ffffff 100%);
  border-radius: 12px;
  padding: 2rem;
  margin: 2rem 0;
  box-shadow: var(--shadow-md);
}

.highlight-section h2 {
  margin-top: 0;
  color: var(--text-primary);
  font-size: 2rem;
}

/* Footer */
.footer {
  text-align: center;
  padding: 2rem 0;
  color: var(--text-secondary);
  font-size: 0.9rem;
  border-top: 1px solid var(--border-color);
  margin-top: 3rem;
}

/* Responsive Design */
@media (max-width: 768px) {
  .container {
    padding: 1rem 0.5rem;
  }

  .header {
    padding: 2rem 1rem;
  }

  .header h1 {
    font-size: 2rem;
  }

  .card {
    padding: 1.5rem;
  }

  .index-links {
    grid-template-columns: 1fr;
  }

  .overview-table {
    font-size: 0.9rem;
  }

  .overview-table th,
  .overview-table td {
    padding: 0.75rem 0.5rem;
  }
}

/* Badge/Importance Styles */
.importance-badge {
  display: inline-block;
  padding: 0.25rem 0.75rem;
  border-radius: 12px;
  font-size: 0.85rem;
  font-weight: 600;
  background: var(--card-bg);
  color: var(--text-primary);
}

.importance-high {
  background: linear-gradient(135deg, #fef3c7 0%, #fde68a 100%);
  color: #92400e;
}

.importance-medium {
  background: linear-gradient(135deg, #dbeafe 0%, #bfdbfe 100%);
  color: #1e40af;
}

.importance-low {
  background: linear-gradient(135deg, #f3f4f6 0%, #e5e7eb 100%);
  color: #4b5563;
}
</style>

<div class="container">

<div class="header">
  <h1>🚀 AI 코딩 어시스턴트 위클리 #002</h1>
  <p class="subtitle">2025년 12월 16일</p>
  <p style="margin-top: 1rem; opacity: 0.9;">이번 주 주요 AI 코딩 도구들의 업데이트를 정리했습니다.</p>
</div>

<div class="index-section">
  <h2>📑 목차 (Index)</h2>
  <ul class="index-links">
    <li><a href="#jetbrains-ai-assistant--junie">JetBrains AI Assistant & Junie</a></li>
    <li><a href="#cursor">Cursor</a></li>
    <li><a href="#github-copilot">GitHub Copilot</a></li>
    <li><a href="#claude-anthropic">Claude (Anthropic)</a></li>
    <li><a href="#이번-주-하이라이트">이번 주 하이라이트</a></li>
    <li><a href="#다음-주-예고">다음 주 예고</a></li>
    <li><a href="#참고-링크">참고 링크</a></li>
  </ul>
</div>

<div class="card" style="background: linear-gradient(135deg, #f6f8fa 0%, #ffffff 100%);">
  <h2>한눈에 보기</h2>
  <table class="overview-table">
    <thead>
      <tr>
        <th>도구</th>
        <th>주요 업데이트</th>
        <th>중요도</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td><strong>JetBrains AI</strong></td>
        <td>Junie AI Chat 통합</td>
        <td>⭐⭐⭐</td>
      </tr>
      <tr>
        <td><strong>Cursor</strong></td>
        <td>Debug Mode 출시</td>
        <td>⭐⭐⭐</td>
      </tr>
      <tr>
        <td><strong>GitHub Copilot</strong></td>
        <td>GPT-5.2 공개 프리뷰</td>
        <td>⭐⭐⭐</td>
      </tr>
      <tr>
        <td><strong>Claude</strong></td>
        <td>4.5 시리즈 모델 출시</td>
        <td>⭐⭐</td>
      </tr>
    </tbody>
  </table>
</div>

<div class="card jetbrains" id="jetbrains-ai-assistant--junie">
  <h2>JetBrains AI Assistant & Junie</h2>
  
  <div class="info-box">
    <h3>업데이트 정보</h3>
    <ul>
      <li><strong>업데이트 날짜</strong>: 2025년 12월 8일</li>
      <li><strong>지원 IDE</strong>: IntelliJ IDEA, PyCharm, WebStorm, GoLand, Rider 등 모든 JetBrains IDE</li>
    </ul>
  </div>

  <h3>AI Assistant 변경사항</h3>
  
  <h4>🤖 Grok Models 추가 (2025-12-02)</h4>
  <p>xAI의 Grok 모델 패밀리가 모든 JetBrains IDE의 AI Chat에 추가되었습니다:</p>
  <ul>
    <li>Grok 4</li>
    <li>Grok 4.1 Fast</li>
    <li>Grok 4.1 Fast (Non-Reasoning)</li>
    <li>Grok Code Fast 1</li>
  </ul>
  <p>이제 더 많은 모델 선택권을 가지게 되었습니다.</p>

  <h4>🌟 Gemini 3 Pro 출시 (2025-11-18)</h4>
  <p>Google의 최신 AI 모델 Gemini 3 Pro가 JetBrains IDEs에서 출시되었습니다. AI Chat과 Junie 코딩 에이전트를 지원하며, 다음과 같은 특징이 있습니다:</p>
  <ul>
    <li><strong>코드베이스 이해 및 스타일 적응</strong>: 프로젝트의 컨벤션을 학습하여 저장소에 자연스러운 변경을 생성</li>
    <li><strong>정확한 지시 따르기</strong>: 복잡한 프롬프트와 긴 문서를 이해하고 정확한 결과 제공</li>
    <li><strong>프론트엔드 개발 강점</strong>: 멀티모달 프론트엔드 생성과 복잡한 UI 작업에 특히 강함</li>
  </ul>

  <h4>🔧 Bring your own AI agent (2025-12-05)</h4>
  <p>JetBrains IDEs에 자체 AI 에이전트를 가져올 수 있는 기능이 추가되었습니다. 이는 커스텀 에이전트를 사용하고 싶은 개발자들에게 유용합니다.</p>

  <h3>Junie 변경사항</h3>
  
  <h4>🎯 Junie가 AI Chat에 통합됨 (2025-12-08) ⭐ <strong>주요 업데이트</strong></h4>
  <p>Junie가 JetBrains AI Chat에 통합되어 별도의 인터페이스 없이 AI Chat에서 직접 사용할 수 있습니다 (Beta).</p>
  
  <p><strong>변경 사항</strong>:</p>
  <ul>
    <li>AI Chat에서 Junie를 에이전트 선택기에서 선택하여 사용 가능</li>
    <li>별도의 Junie 플러그인 인터페이스가 단일 통합 공간으로 병합</li>
    <li>기존 Junie 플러그인은 계속 사용 가능하며, 설정은 점진적으로 통합</li>
  </ul>
  
  <p><strong>사용 방법</strong>:</p>
  <ol>
    <li>IDE에서 AI Chat 열기</li>
    <li>에이전트 선택기에서 "Junie" 선택</li>
    <li>프롬프트 실행 - 에이전트가 자동으로 다운로드 및 설치됨</li>
  </ol>
  
  <p>이 통합으로 Junie와 AI Chat 간의 전환이 더욱 원활해졌습니다.</p>

  <h4>🚀 Gemini 3 Pro 지원 (2025-11-18)</h4>
  <p>Junie가 Gemini 3 Pro 모델을 지원합니다. 더 똑똑한 추론, 강력한 지시 따르기, 워크플로우에의 원활한 통합을 제공합니다.</p>

  <h3>개발자에게 미치는 영향</h3>
  <p>Junie의 AI Chat 통합은 UX 개선의 중요한 단계입니다. 이제 하나의 인터페이스에서 모든 AI 기능을 사용할 수 있어 워크플로우가 더욱 간소화됩니다. Gemini 3 Pro는 특히 프론트엔드 개발 작업에서 강력한 성능을 보여줍니다.</p>
</div>

<div class="card cursor" id="cursor">
  <h2>Cursor</h2>
  
  <div class="info-box">
    <h3>버전 정보</h3>
    <ul>
      <li><strong>버전</strong>: 2.2</li>
      <li><strong>릴리즈 날짜</strong>: 2025년 12월 10일</li>
    </ul>
  </div>

  <h3>주요 변경사항</h3>
  
  <h4>🐛 Debug Mode</h4>
  <p>앱에 런타임 로그를 삽입하여 버그의 근본 원인을 찾습니다. 스택, 언어, 모델 전반에서 작동하며, 실제 실행 데이터를 기반으로 정확한 버그 수정을 제안합니다.</p>
  
  <blockquote>
    <strong>💡 왜 중요한가요?</strong><br>
    기존 AI는 버그를 설명하면 "이럴 것 같다"며 수백 줄의 추측성 코드를 뱉어냈습니다. Debug Mode는 <strong>실제 런타임 데이터</strong>를 기반으로 정확한 수정만 제안합니다.
  </blockquote>

  <h4>🎨 Browser layout and style editor</h4>
  <p>새로운 브라우저 사이드바와 컴포넌트 트리로 디자인과 코딩을 동시에 수행할 수 있습니다. 요소를 이동하고, 색상을 업데이트하며, 레이아웃을 테스트하고 CSS를 실시간으로 실험한 후 변경사항을 코드베이스에 즉시 적용할 수 있습니다.</p>

  <h4>📊 Plan Mode improvements</h4>
  <p>인라인 Mermaid 다이어그램 지원으로 에이전트가 자동으로 시각화를 생성하고 스트리밍합니다. 또한 선택한 to-do를 새 에이전트에 전송하는 옵션이 추가되었습니다.</p>

  <h4>⚖️ Multi-agent judging</h4>
  <p>여러 에이전트를 병렬로 실행할 때 Cursor가 자동으로 모든 실행을 평가하고 최적의 솔루션을 추천합니다. 선택된 에이전트에 선택 이유가 주석으로 표시됩니다.</p>

  <h4>📌 Pinned chats</h4>
  <p>에이전트 사이드바에서 채팅을 상단에 고정하여 나중에 참조할 수 있습니다.</p>

  <h3>최근 업데이트 히스토리</h3>
  
  <div class="info-box">
    <h4>Cursor 2.1 (2025-11-21)</h4>
    <ul>
      <li>Improved Plan Mode: 계획 생성 시 명확화 질문에 대한 인터랙티브 UI 제공</li>
      <li>AI Code Reviews: Cursor에서 직접 버그를 찾고 수정</li>
      <li>Instant Grep (Beta): 모든 grep 명령이 즉시 실행됨</li>
    </ul>
  </div>

  <div class="info-box">
    <h4>Cursor 2.0 (2025-10-29)</h4>
    <ul>
      <li>Multi-Agents: 최대 8개의 에이전트를 병렬로 실행</li>
      <li>Composer: 유사한 지능의 모델보다 4배 빠른 에이전트 코딩 모델</li>
      <li>Browser (GA): Browser for Agent가 일반 출시</li>
      <li>Sandboxed Terminals (GA): macOS에서 보안 샌드박스 실행</li>
    </ul>
  </div>

  <h3>개발자에게 미치는 영향</h3>
  <p>Debug Mode는 특히 복잡한 버그를 다룰 때 큰 도움이 됩니다. 실제 런타임 데이터를 기반으로 하기 때문에 추측성 수정보다 훨씬 정확합니다. Browser Style Editor는 프론트엔드 개발자에게 특히 유용하며, 디자인과 코드를 동시에 작업할 수 있어 워크플로우가 크게 개선됩니다.</p>
</div>

<div class="card copilot" id="github-copilot">
  <h2>GitHub Copilot</h2>
  
  <div class="info-box">
    <h3>업데이트 정보</h3>
    <ul>
      <li><strong>게시 날짜</strong>: 2025년 12월 11일</li>
      <li><strong>대상 플랫폼</strong>: Visual Studio Code, Copilot Chat in github.com, GitHub Mobile, Copilot CLI</li>
    </ul>
  </div>

  <h3>주요 변경사항</h3>
  
  <h4>🤖 OpenAI GPT-5.2 공개 프리뷰 (2025-12-11)</h4>
  <p>OpenAI의 최신 모델 GPT-5.2가 GitHub Copilot에 공개 프리뷰로 추가되었습니다. 이 모델은 <strong>긴 컨텍스트</strong>와 <strong>프론트엔드 UI 생성</strong>에 특화되어 있습니다.</p>
  
  <p><strong>사용 가능한 플랜</strong>: Copilot Pro, Pro+, Business, Enterprise</p>
  
  <p><strong>사용 방법</strong>:</p>
  <ul>
    <li>Visual Studio Code 1.104.1 이상에서 모델 선택기에서 GPT-5.2 선택</li>
    <li>Copilot Chat in github.com</li>
    <li>GitHub Mobile (iOS 및 Android)</li>
    <li>Copilot CLI</li>
  </ul>
  
  <p>Enterprise와 Business 플랜의 경우 관리자가 Copilot 설정에서 GPT-5.2를 활성화해야 합니다.</p>

  <h4>🔄 Auto model selection 일반 출시 (2025-12-10)</h4>
  <p>GitHub Copilot in Visual Studio Code에서 자동 모델 선택 기능이 일반 출시되었습니다. Auto 모드에서 Copilot이 현재 모델 가용성에 따라 자동으로 모델을 선택합니다.</p>

  <h4>📊 코드 생성 메트릭 대시보드 (2025-12-05)</h4>
  <p>GitHub Copilot 코드 생성 라인 수(LoC) 메트릭을 대시보드에서 확인할 수 있습니다. Enterprise 관리자는 코드 생성 인사이트 대시보드에서 이 메트릭을 볼 수 있습니다.</p>

  <h4>🔍 Visual Studio 11월 업데이트 (2025-12-03)</h4>
  <p>Visual Studio에서의 Copilot 업데이트. Intent detection for all-in-one search 기능이 추가되어 "Did you mean" 기능으로 검색 용어를 분석합니다.</p>

  <h3>개발자에게 미치는 영향</h3>
  <p>GPT-5.2는 특히 프론트엔드 개발과 긴 컨텍스트가 필요한 작업에 유용합니다. Auto model selection은 모델 선택의 번거로움을 줄여주며, 코드 생성 메트릭은 팀의 Copilot 사용 현황을 파악하는 데 도움이 됩니다.</p>
</div>

<div class="card claude" id="claude-anthropic">
  <h2>Claude (Anthropic)</h2>
  
  <div class="info-box">
    <h3>업데이트 정보</h3>
    <ul>
      <li><strong>발표 날짜</strong>: 2025년 11월 24일</li>
      <li><strong>대상 제품</strong>: Claude Opus, Sonnet, Haiku</li>
    </ul>
  </div>

  <h3>주요 변경사항</h3>
  
  <h4>🧠 Claude Opus 4.5 출시 (2025-11-24)</h4>
  <p>Claude Opus 4.5 모델이 출시되었습니다. Anthropic의 최고 성능 모델로, 복잡한 추론 작업에 최적화되어 있습니다.</p>

  <h4>🚀 Claude Haiku 4.5 및 Sonnet 4.5 출시 (2025-11-19)</h4>
  <p>Claude Haiku 4.5와 Sonnet 4.5 모델이 동시에 출시되었습니다. 4.5 시리즈는 이전 버전 대비 성능과 정확도가 개선되었습니다.</p>

  <h3>개발자에게 미치는 영향</h3>
  <p>Claude 4.5 시리즈는 코드 생성, 리뷰, 문서화 등 다양한 개발 작업에서 더 나은 성능을 제공합니다. 특히 Opus 4.5는 복잡한 코드베이스 분석이나 아키텍처 설계 같은 고급 작업에 적합합니다.</p>
</div>

<div class="highlight-section" id="이번-주-하이라이트">
  <h2>이번 주 하이라이트</h2>
  
  <h3>가장 주목할 만한 업데이트</h3>
  
  <div style="display: grid; gap: 1.5rem; margin-top: 1.5rem;">
    <div class="info-box">
      <h4>1. Cursor Debug Mode 🐛</h4>
      <p>실제 런타임 데이터를 기반으로 버그를 추적하는 혁신적인 기능. 복잡한 버그를 다룰 때 특히 유용합니다.</p>
    </div>
    
    <div class="info-box">
      <h4>2. GitHub Copilot GPT-5.2 🤖</h4>
      <p>프론트엔드 UI 생성과 긴 컨텍스트에 특화된 최신 모델. 프론트엔드 개발자들에게 큰 도움이 될 것입니다.</p>
    </div>
    
    <div class="info-box">
      <h4>3. JetBrains Junie 통합 🎯</h4>
      <p>AI Chat과 Junie의 통합으로 더욱 일관된 사용자 경험을 제공합니다. 하나의 인터페이스에서 모든 AI 기능을 사용할 수 있습니다.</p>
    </div>
  </div>

  <h3>트렌드 분석</h3>
  <p>이번 주 업데이트들을 보면 몇 가지 트렌드가 보입니다:</p>
  
  <ol>
    <li><strong>통합과 단순화</strong>: JetBrains의 Junie 통합처럼, 여러 인터페이스를 하나로 통합하는 움직임이 계속되고 있습니다.</li>
    <li><strong>실제 데이터 기반 작업</strong>: Cursor의 Debug Mode처럼, 추측이 아닌 실제 런타임 데이터를 활용하는 기능이 강조되고 있습니다.</li>
    <li><strong>모델 다양화</strong>: GitHub Copilot의 GPT-5.2, JetBrains의 Grok Models 추가처럼, 다양한 모델을 제공하여 개발자가 자신의 작업에 맞는 모델을 선택할 수 있게 하는 추세입니다.</li>
    <li><strong>프론트엔드 특화</strong>: GPT-5.2와 Gemini 3 Pro 모두 프론트엔드 개발에 특화된 기능을 강조하고 있어, 프론트엔드 개발 도구로서의 AI 어시스턴트 역할이 강화되고 있습니다.</li>
  </ol>
</div>

<div class="card" id="다음-주-예고">
  <h2>다음 주 예고</h2>
  <p>다음 주에도 각 도구들의 지속적인 개선이 예상됩니다. 특히:</p>
  <ul>
    <li>Cursor의 Debug Mode 사용자 피드백 반영</li>
    <li>GitHub Copilot GPT-5.2의 일반 출시 가능성</li>
    <li>JetBrains Junie 통합의 추가 개선사항</li>
  </ul>
</div>

<div class="card" id="참고-링크">
  <h2>참고 링크</h2>
  <ul>
    <li><a href="https://blog.jetbrains.com/ai/" target="_blank">JetBrains AI</a></li>
    <li><a href="https://www.jetbrains.com/junie/" target="_blank">Junie</a></li>
    <li><a href="https://www.cursor.com/changelog" target="_blank">Cursor Changelog</a></li>
    <li><a href="https://github.blog/changelog/" target="_blank">GitHub Blog - Changelog</a></li>
    <li><a href="https://www.anthropic.com/news" target="_blank">Anthropic News</a></li>
    <li><a href="https://docs.anthropic.com/en/release-notes" target="_blank">Claude Release Notes</a></li>
  </ul>
</div>

<div class="footer">
  <p><em>이 글은 2025년 12월 16일에 작성되었습니다.</em></p>
</div>

</div>

