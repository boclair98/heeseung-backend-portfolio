# OpenUI Design Plan

## Variant 1

### Resolved inputs
- Topic: 이희승 백엔드 개발자 포트폴리오
- Offer: 실제 프로젝트의 설계, 구현 근거, 경력과 이력서를 한 흐름으로 확인
- Audience: 백엔드 개발 역량과 프로젝트의 구현 범위를 검토하는 채용 담당자와 개발자
- Primary user action: 프로젝트 살펴보기: #projects로 이동해 실제 프로젝트 상세를 열기
- Deliverable: 기존 정적 HTML 홈페이지와 별도 CSS; 기존 JavaScript 상세 모달과 필터 유지
- Style direction: 편집물처럼 명확한 타이포그래피 중심의 기술 포트폴리오
- Tonal key: 밝은 쿨 화이트 바탕과 기존 블루 브랜드
- Icon policy: 기존 SVG 소셜 링크와 기술 아이콘 유지
- Proof assets: 기존 실제 프로젝트 이미지와 코드 연결만 유지; 새로운 성과나 후기 없음
- Motion intensity: Minimal; 포커스와 짧은 hover 피드백, reduced-motion 존중

### Composition contract
- Hero archetype: asymmetrical
- First-viewport structure: 상단 탐색 아래 왼쪽 기준선을 맞춘 개발자 이름, 규칙·복구 중심 제목과 본문, 프로젝트와 이력서 링크를 배치한다. 소셜 링크는 뒤에 두고 핵심 역량 섹션의 시작을 화면 아래에서 예고한다.
- Primary visual/proof artifact: none; 타이포그래피 중심. 실제 프로젝트 증거는 기존 프로젝트 목록과 상세에 보존
- Interaction behavior: 프로젝트 CTA는 #projects, 이력서 CTA는 resume.html로 이동. 기존 기술 필터와 dialog의 Escape·닫기·트리거 포커스 복귀 유지
- Reuse boundary: 기존 문서·프로젝트 데이터·상세 템플릿·아이콘을 보존하고 홈페이지 히어로와 탐색·포커스 스타일만 수정

### 서비스와 코드 근거
index.html은 순수 HTML/CSS/JS로 기술·경험·프로젝트·수상·교육을 제공한다. 프로젝트 버튼은 data-project와 template을 연결한 dialog를 열고 기술 필터는 aria-pressed로 상태를 관리한다. resume.html이 실제로 존재한다. 현재 히어로는 인사말 위주이고 핵심 행동 링크가 없으며 중앙 정렬과 긴 상단 여백으로 프로젝트 진입이 늦다. 모바일 탐색은 긴 링크들이 한 줄에 모인다.

### 디자인 기준과 구현 범위
기존 #3182f6 포인트와 #145ac7 링크를 유지한다. 기본 바탕 #f4f6f9와 히어로 #fafbfc, 본문 #202633, 보조문 #526174. 기존 Noto Sans KR와 시스템 대체 폰트를 유지한다. 본문 16~18px/1.75, 제목 desktop clamp 48~76px/1.18, mobile 36~44px/1.24, 중요 링크 15~16px/1.4. 콘텐츠 폭 1120px, PC 좌우 48px 이상, 모바일 20px. 히어로 96~128px 상단 리듬, 섹션 간격 PC 112px/mobile 72px. CTA 높이 48px, 포커스 3px 실선. 탐색은 모바일에서 의도적으로 가로 스크롤하고 각 링크는 최소 44px. 기존 프로젝트 콘텐츠는 변경하지 않는다. 새로운 이미지 다운로드나 가짜 지표를 추가하지 않는다.

### 실행과 검증 계획
정적 HTTP 서버로 실행해 1440×900, 768×1024, 390×844, 360×800을 직접 확인한다. 프로젝트 이동, 이력서 링크, 기술 필터, 프로젝트 상세 열기·Escape 닫기·포커스 복귀와 가로 넘침을 확인한다. 브라우저 콘솔에서 관련 오류를 확인한다.

### Filled generation prompt

Create one high-concept page for 이희승 백엔드 개발자 포트폴리오.

#### Inputs
- Topic: 이희승 백엔드 개발자 포트폴리오.
- Offer: 실제 프로젝트의 설계, 구현 근거, 경력과 이력서를 한 흐름으로 확인
- Audience: 백엔드 개발 역량과 프로젝트의 구현 범위를 검토하는 채용 담당자와 개발자
- Primary user action: 프로젝트 살펴보기: #projects로 이동해 실제 프로젝트 상세를 열기
- Deliverable: 기존 정적 HTML 홈페이지와 별도 CSS; 기존 JavaScript 상세 모달과 필터 유지
- Style direction: 편집물처럼 명확한 타이포그래피 중심의 기술 포트폴리오
- Tonal key: 밝은 쿨 화이트 바탕과 기존 블루 브랜드
- Icon policy: 기존 SVG 소셜 링크와 기술 아이콘 유지
- Proof assets: 기존 실제 프로젝트 이미지와 코드 연결만 유지; 새로운 성과나 후기 없음
- Motion intensity: Minimal; 포커스와 짧은 hover 피드백, reduced-motion 존중

#### Objective
Design one premium, memorable page with a dominant hero and one coherent visual world derived from the topic itself.
The result should feel specific, intentional, and action-oriented when the concept calls for action, not like a generic startup or SaaS template.

Choose the strongest clear solution.
Do not collapse the concept into a simpler generic pattern just to make execution easier.

- Treat single-file execution as a packaging constraint, not a creative constraint.
Do not reduce conceptual ambition, visual specificity, interaction richness, or production quality merely because the deliverable is concise.

#### Internal concept choice
Before composing, decide internally:
- one dominant hero archetype: centered / asymmetrical / immersive
- one dominant proof mode: none / embedded gesture / single artifact
- one palette driver derived from the topic
- one tonal key: light / mid / dark / topic-derived
- one motion role: none / minimal / ambient / interactive
- one icon approach: none / minimal / expressive / topic-native
- optionally one secondary accent only if it strengthens the main direction without creating a second visual world
Do not output this planning.

#### Non-negotiables
- Use a strong hero-first composition.
- Headline: 3-12 words, max 3 lines.
- Supporting copy: 1-2 short sentences, concise and specific.
- CTAs are optional. If used, include at most 1 primary and 1 secondary CTA.
- If a clear next step is central to the offer or concept, include a CTA; otherwise CTA omission is allowed.
- CTA labels must be specific to the offer and action, not generic.
- Supporting highlights are optional. If used, show them only once in a single lower support cluster beneath the hero.
- Keep the hero dominant, focused, readable, and uncluttered.
- Proof is optional. Use it only if it clearly strengthens the concept.
- If no real proof assets are provided, do not invent metrics, testimonials, customer logos, screenshots, or fake UI proof.
- Prefer depth inside the hero, proof gesture, CTA behavior, support copy, or background logic rather than adding extra sections by default.

#### Composition
- Choose the clearest structure for the topic; do not default to generic two-column marketing layouts.
- A top navigation bar is optional. When used, make it native to the chosen style direction and subordinate to the hero rather than a generic boxed header.
- The hero may be fully integrated rather than framed.
- The hero does not need to become a panel, dashboard, device mockup, rounded card, or floating showcase unless the topic genuinely demands that artifact.
- Build hierarchy through scale, contrast, spacing, alignment, depth, rhythm, and composition before using frames, dividers, or containers.
- Keep supporting content clearly subordinate to the hero.
- Do not interpret structural restraint as permission to flatten the concept into a generic minimal layout.
- Do not use text-on-text layering, typographic collisions, or overlapping live text as a compositional device.

#### Visual system
- Build one coherent visual world derived from the topic itself.
- Let the topic drive palette, contrast, typography, spacing, geometry, motifs, materials, and motion.
- Even restrained palettes must feel intentional and specific, not generic premium-neutral.
- The background must actively contribute mood, depth, and topic logic.
- If the topic suggests a real system language, physical behavior, or interface grammar, show that directly instead of generic abstract-tech decoration.
- Treat headline typography as part of the concept, not neutral text.
- The headline may use topic-derived color, selective emphasis, multi-tone treatment, or gradient accents when they strengthen the concept and remain readable.
- Do not default the headline to neutral black, white, or near-white unless that is clearly the strongest topic-native choice.

#### Background and tonal diversity
- Premium and atmospheric design may be light, mid-tone, or dark; do not default to dark.
- Choose the tonal key from the topic, offer, audience, and style direction rather than from generic cinematic or tech aesthetics.
- Contrast may come from hue, saturation, temperature, texture, density, or scale, not only darkness.

#### Proof and concept expression
- Prefer the minimum visual evidence needed to make the idea feel specific, credible, and native to the topic.
- If the concept is strongest with typography, atmosphere, and one precise gesture, do that.
- If a stronger proof artifact is justified, use one legible, unified artifact rather than multiple fragmented panels.
- Proof may take the form of a signal, trace, contour, command line, path, specimen, structural mark, scene fragment, or other topic-native evidence.
- Typography itself may carry part of the concept or proof.
- When appropriate, use one precise typographic gesture—such as selective word emphasis, chromatic offset, gradient emphasis, distortion, signal breakup, or structural interruption—to make the concept feel more specific and alive.
- Prefer one strong typographic intervention over many scattered decorative effects.
- Avoid decorative pseudo-proof.
- Avoid turning simple ideas into framed showcases, dashboard fragments, floating panels, softened slabs, or generic marketing geometry.

#### Icons and symbolic language
- Icons are optional.
- Use icons only when they improve scanability, recognition, navigation, proof clarity, or support-cluster legibility.
- Prefer topic-native icon logic over generic startup glyphs.
- Keep icon style consistent in stroke weight, geometry, corner logic, and detail level.
- Use icons primarily in clearly secondary roles unless a single topic-native symbol is central to the concept.
- Do not let icons compete with the hero headline, proof artifact, or CTA hierarchy.

#### Support cluster
- If used, show supporting highlights only once, in a single lower cluster beneath the hero.
- Each highlight should be short, fast to scan, and clearly secondary.
- Supporting highlights may use concise icons or symbolic marks when helpful.
- Support-cluster elements may use subtle motion when it improves scanability, continuity, or atmosphere and remains clearly secondary.
- Card-like grouping is allowed only inside this lower support cluster.
- These modules may use at most one light surface treatment, such as a subtle stroke, tonal fill, or very soft shadow.
- Keep support modules uniform, non-nested, and visually subordinate.
- Do not use card-like structures in the hero, proof, CTA area, or elsewhere on the page.

#### Motion
- Motion is optional.
- Use motion only when it supports hierarchy, continuity, feedback, atmosphere, or topic logic.
- Default to none, minimal, or ambient motion depending on what the concept actually needs.
- Motion may live in typography, background behavior, proof logic, support-cluster behavior, or interaction feedback.
- A single key word or short phrase may use subtle text-based motion such as glitch, flicker, jitter, scanline shift, chromatic split, text scramble, pulse, or reveal if it strengthens the concept.
- Keep motion controlled, readable, non-blocking, and subordinate to clarity.
- Avoid scrolljacking, attention-hijacking loops, and ornamental animation.
- Respect reduced-motion preferences.

#### Accessibility and readability
- Preserve strong readability and clear hierarchy at all viewport sizes.
- Maintain sufficient contrast between text and background.
- Do not place essential text over busy imagery unless readability remains strong.
- Avoid cramped spacing, visual collisions, and weak focal hierarchy.
- Do not place badges, pills, annotations, stickers, or floating interface fragments over essential text.
- If the deliverable is code, use semantic HTML structure, visible focus states, keyboard-friendly interactions, and reduced-motion handling.
- When in doubt, preserve legibility over expressive overlap.

#### Anti-drift rules
- Do not drift into bland corporate SaaS styling.
- Do not default to dashboard aesthetics, feature-grid thinking, boxed-section composition, or template-like modularity.
- Do not use disconnected motifs, random color choices, or interchangeable abstract-tech shapes.
- Do not use card-within-card composition, nested surfaces, floating panels, fake proof, or stock-looking UI.
- Keep one visual world, one dominant hero, and one clear structural logic.
- Do not allow text, labels, or interface elements to overlap, collide, or sit on top of one another.

#### Output
Return only the final 기존 정적 HTML 홈페이지와 별도 CSS; 기존 JavaScript 상세 모달과 필터 유지.

If the deliverable is code:
- Output a complete production-ready file or component.
- Keep dependencies minimal unless explicitly requested.
- Make it responsive.
- Keep support highlights in one lower support cluster only when used.

#### Final self-check
Before returning, verify that the result keeps:
- one dominant hero
- one coherent visual world
- no invented proof
- no cardification outside the lower support cluster
- no generic SaaS drift
- no unnecessary structural fragmentation
- no nested containment
- no floating sub-surfaces
- all text clearly legible and comfortably spaced


### Output target
- Path: index.html
- Path: home-refinement.css
