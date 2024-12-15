# Translation Guidelines for Immersive Translate

## General Rules

1. SEO Requirements

   - Keep `browser.brandDescription` in English across all language files
   - Maintain product name "Immersive Translate" in English

2. Brand Names and Services

   - Keep all service names in English: DeepL, OpenAI, Claude, Gemini, etc.
   - Keep cloud service names in English: Google Drive, WeChat, Telegram

3. Technical Terms
   - Translate consistently across all UI elements
   - Use standard industry translations when available
   - Avoid mixing English terms unless standard in target language

## Japanese (ja.json)

1. Technical Terms

   - Hover: ホバー (not マウスホバー)
   - Settings: 設定 (not パラメータ)
   - Translation: 翻訳
   - Sync: 同期
   - Cache: キャッシュ
   - Cloud: クラウド

2. UI/UX Conventions

   - Use polite form (です/ます) for user messages
   - Use plain form for short UI labels
   - Success messages: 成功 (not サクセス)
   - Error messages: エラー or 失敗

3. Core Features
   - Bilingual Mode: バイリンガルモード
   - Translation Services: 翻訳サービス
   - Page Rules: ページルール
   - Input Field: 入力フィールド
   - PDF Translation: PDF翻訳
   - Video Subtitles: 動画字幕
   - Hover Translation: ホバー翻訳
   - Translation Theme: 翻訳テーマ
   - Shortcuts: ショートカット

## Korean (ko.json)

1. Technical Terms

   - Hover: 호버 (remove 컴퓨터 annotations)
   - Settings: 설정
   - Translation: 번역
   - Sync: 동기화
   - Cache: 캐시
   - Cloud: 클라우드

2. UI/UX Conventions

   - Use polite form (합니다/습니다) for messages
   - Use standard form for UI labels
   - Remove unnecessary (컴퓨터) annotations
   - Consistent technical translations

3. Core Features
   - Bilingual Mode: 이중 언어 모드
   - Translation Services: 번역 서비스
   - Page Rules: 페이지 규칙
   - Input Field: 입력 필드
   - PDF Translation: PDF 번역
   - Video Subtitles: 동영상 자막
   - Hover Translation: 호버 번역
   - Translation Theme: 번역 테마
   - Shortcuts: 단축키

## French (fr.json)

1. Technical Terms

   - Remove "(informatique)" annotations
   - Settings: Paramètres
   - Translation: Traduction
   - Sync: Synchronisation
   - Cache: Cache
   - Cloud: Cloud

2. UI/UX Conventions

   - Use formal "vous" consistently
   - Maintain formal tone in all messages
   - Use infinitive for action buttons
   - Standardize technical terms

3. Core Features
   - Bilingual Mode: Mode bilingue
   - Translation Services: Services de traduction
   - Page Rules: Règles de page
   - Input Field: Champ de saisie
   - PDF Translation: Traduction PDF
   - Video Subtitles: Sous-titres vidéo
   - Hover Translation: Traduction au survol
   - Translation Theme: Thème de traduction
   - Shortcuts: Raccourcis

## German (de.json)

1. Technical Terms

   - Remove "(Computer)" and "(Berechnung)" annotations
   - Settings: Einstellungen
   - Translation: Übersetzung
   - Sync: Synchronisierung
   - Cache: Cache
   - Cloud: Cloud

2. UI/UX Conventions

   - Use formal "Sie" form consistently
   - Capitalize nouns according to German rules
   - Use consistent compound word formation
   - Standardize technical terminology

3. Core Features
   - Bilingual Mode: Zweisprachiger Modus
   - Translation Services: Übersetzungsdienste
   - Page Rules: Seitenregeln
   - Input Field: Eingabefeld
   - PDF Translation: PDF-Übersetzung
   - Video Subtitles: Videountertitel
   - Hover Translation: Hover-Übersetzung
   - Translation Theme: Übersetzungsthema
   - Shortcuts: Tastenkombinationen

## Error Message Standards

1. Japanese

   - Error format: 「エラー：{message}」
   - Success format: 「成功：{message}」

2. Korean

   - Error format: "오류: {message}"
   - Success format: "성공: {message}"

3. French

   - Error format: "Erreur : {message}"
   - Success format: "Succès : {message}"

4. German
   - Error format: "Fehler: {message}"
   - Success format: "Erfolg: {message}"

## Formality Levels

1. Japanese

   - User messages: です/ます form
   - UI labels: Plain form
   - Documentation: です/ます form

2. Korean

   - User messages: 합니다/습니다 form
   - UI labels: Standard form
   - Documentation: 합니다/습니다 form

3. French

   - All contexts: Formal "vous"
   - Technical terms: Standard industry terms
   - Documentation: Formal style

4. German
   - All contexts: Formal "Sie"
   - Technical terms: Standard industry terms
   - Documentation: Formal style
