---
marp: true
theme: default
style: |
  @import url('coconala-theme/coconala-pop.css');
---
<!-- markdownlint-disable MD033 -->
<!-- markdownlint-disable MD025 -->

<!-- _class: title-slide -->
<!-- _backgroundImage: url('coconala-theme/assets/images/title_bg.svg') -->

# Marp Coconala Template<br />スライドパターン完全ガイド<br />デザインシステム

<div class="subtitle">
Coconala テンプレート / 2025年版<br/>
すべてのスライドパターンを網羅したサンプル
</div>

---

<!-- _backgroundImage: url('coconala-theme/assets/images/company_introduction.svg') -->

---

<!-- _backgroundImage: url('coconala-theme/assets/images/agenda_bg.svg') -->
<!-- _class: agenda -->

# アジェンダ

- **レイアウトパターン基礎**
- **プロフィール・自己紹介**
- **コンテンツ表示テクニック**
- **データ・効果の可視化**
- **問題解決フレームワーク**
- **まとめ・活用事例**

---

<!-- _class: chapter-intro chapter-intro-01 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_1_bg.svg') -->

# レイアウトパターン基礎

---

<!-- _class: chapter-page chapter-page-01 -->

# レイアウトパターン基礎

<div class="chapter-message">
  3つの基本レイアウトパターンを活用した効果的なスライド構成
</div>

<div class="chapter-content equal">
  <div class="content-left">
    <h3>🎯 Equalレイアウト（5:5）</h3>
    <ul>
      <li><strong>左右対等な情報量</strong>でバランス良く</li>
      <li><strong>比較・対比</strong>に最適</li>
      <li><strong>Before/After</strong>の表現に効果的</li>
      <li><strong>2つの選択肢</strong>を並べる場合</li>
    </ul>
  </div>
  <div class="content-right">
    <h3>📊 その他のレイアウト</h3>
    <p><strong>7:3レイアウト</strong><br/>
    メイン情報とサポート情報の組み合わせ</p>
    <p><strong>Singleレイアウト</strong><br/>
    一つのメッセージに集中したい場合</p>
  </div>
</div>

---

<!-- _class: chapter-intro chapter-intro-02 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_2_bg.svg') -->

# プロフィール・自己紹介

---

<!-- _class: chapter-page chapter-page-02 profile-slide -->

# プロフィール・自己紹介

<div class="chapter-message">
  専用のプロフィールスライドクラスで印象的な自己紹介を演出
</div>

<div class="chapter-content ratio-7-3">
  <div class="content-left">
    <h3>👤 山田 太郎</h3>
    <ul>
      <li><strong>フロントエンドエンジニア</strong></li>
      <li><strong>UI/UXデザイナー</strong></li>
      <li><strong>5年の開発経験</strong></li>
      <li><strong>React・Vue.js専門</strong></li>
      <li><strong>アクセシビリティ重視</strong></li>
    </ul>
  </div>
  <div class="content-right">
    <img src="coconala-theme/assets/images/coconala-icon.png" alt="プロフィール画像">
  </div>
</div>

---

<!-- _class: chapter-intro chapter-intro-03 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_3_bg.svg') -->

# コンテンツ表示テクニック

---

<!-- _class: chapter-page chapter-page-03 -->

# コンテンツ表示テクニック

<div class="chapter-message">
  Single レイアウトで重要なメッセージを中央に集約表示
</div>

<div class="chapter-content single">
  <div class="content-single">
    <h3>🎨 効果的なコンテンツ表示の原則</h3>
    <ul>
      <li><strong>1スライド1メッセージ</strong> → 聞き手の理解度向上</li>
      <li><strong>視覚的なヒエラルキー</strong> → 重要度を色と大きさで表現</li>
      <li><strong>適切な余白活用</strong> → 情報の整理と読みやすさ</li>
      <li><strong>ブランドカラーの統一</strong> → 一貫性のあるデザイン</li>
    </ul>
    <p style="margin-top: 30px; font-size: 1.3rem; color: var(--coco-blue); text-align: center;">
      <strong>💡 重要：視聴者の認知負荷を下げることが最優先</strong>
    </p>
  </div>
</div>

---

<!-- _class: chapter-intro chapter-intro-04 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_4_bg.svg') -->

# データ・効果の可視化

---

<!-- _class: chapter-page chapter-page-04 -->

# データ・効果の可視化

<div class="chapter-message">
  7:3 レイアウトでメイン情報と補足情報を効果的に配置
</div>

<div class="chapter-content ratio-7-3">
  <div class="content-left">
    <h3>📈 プロジェクト成果指標</h3>
    <div class="card" style="background: linear-gradient(135deg, rgba(0,133,255,0.1), rgba(0,196,143,0.1)); margin-bottom: 15px;">
      <h4>開発効率の向上</h4>
      <p><strong>作業時間：8時間 → 2時間（75%削減）</strong></p>
    </div>
    <div class="card" style="background: linear-gradient(135deg, rgba(0,196,143,0.1), rgba(255,204,0,0.1)); margin-bottom: 15px;">
      <h4>品質向上</h4>
      <p><strong>バグ検出率：30% → 80%（50%向上）</strong></p>
    </div>
    <div class="card" style="background: linear-gradient(135deg, rgba(255,204,0,0.1), rgba(255,155,53,0.1));">
      <h4>チーム満足度</h4>
      <p><strong>満足度スコア：6.2 → 8.7（2.5ポイント向上）</strong></p>
    </div>
  </div>
  <div class="content-right">
    <h3>🎯 付加効果</h3>
    <p><strong>Before:</strong><br/>手作業でのチェック<br/>属人化した品質管理</p>
    <p><strong>After:</strong><br/>自動化による一貫性<br/>標準化されたプロセス</p>
  </div>
</div>

---

<!-- _class: chapter-intro chapter-intro-05 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_5_bg.svg') -->

# 問題解決フレームワーク

---

<!-- _class: chapter-page chapter-page-05 -->

# 問題解決フレームワーク

<div class="chapter-message">
  テーブル表示とカード表示を組み合わせた包括的な情報整理
</div>

<div class="chapter-content single">
  <div class="content-single">
    <h3>🔄 Problem → Solution → Result の流れ</h3>
    <table style="width: 100%; font-size: 0.85rem; margin-bottom: 20px;">
      <tr style="background: linear-gradient(135deg, var(--coco-pink), var(--coco-purple)); color: white;">
        <th style="padding: 12px;">Problem（課題）</th>
        <th style="padding: 12px;">Solution（解決策）</th>
        <th style="padding: 12px;">Result（結果）</th>
      </tr>
      <tr>
        <td style="padding: 12px; background: rgba(255,74,140,0.1);">手動作業が多く効率が悪い</td>
        <td style="padding: 12px; background: rgba(255,204,0,0.1);">自動化ツールの導入</td>
        <td style="padding: 12px; background: rgba(0,196,143,0.1);"><strong>75%の時間削減</strong></td>
      </tr>
      <tr>
        <td style="padding: 12px; background: rgba(255,74,140,0.1);">品質にばらつきがある</td>
        <td style="padding: 12px; background: rgba(255,204,0,0.1);">チェックリスト標準化</td>
        <td style="padding: 12px; background: rgba(0,196,143,0.1);"><strong>品質安定性向上</strong></td>
      </tr>
    </table>
    <p style="text-align: center; color: var(--coco-blue); font-size: 1.1rem;">
      <strong>継続的改善により、チーム全体のパフォーマンスが向上しました</strong>
    </p>
  </div>
</div>

---

<!-- _class: chapter-intro chapter-intro-06 -->
<!-- _backgroundImage: url('coconala-theme/assets/images/chapter_6_bg.svg') -->

# まとめ・活用事例

---

<!-- _class: chapter-page chapter-page-06 -->

# まとめ・活用事例

<div class="chapter-message">
  すべてのパターンを活用した実践的なプレゼンテーション作成のポイント
</div>

<div class="chapter-content equal">
  <div class="content-left">
    <h3>🎯 レイアウト活用のコツ</h3>
    <ul>
      <li><strong>Equal:</strong> 比較・対比に最適</li>
      <li><strong>7:3:</strong> 詳細説明+サポート情報</li>
      <li><strong>Single:</strong> 重要メッセージの強調</li>
      <li><strong>Profile:</strong> 自己紹介専用デザイン</li>
    </ul>
    <p style="color: var(--coco-green); margin-top: 15px;">
      <strong>適切なレイアウト選択で伝達効果が格段に向上</strong>
    </p>
  </div>
  <div class="content-right">
    <h3>📊 テンプレート活用効果</h3>
    <ul>
      <li><strong>デザイン統一:</strong> ブランド認知向上</li>
      <li><strong>作成時間:</strong> 50%以上の短縮</li>
      <li><strong>視認性:</strong> 情報の整理と理解促進</li>
      <li><strong>再利用性:</strong> 一度作成すれば継続活用可能</li>
    </ul>
  </div>
</div>

---

<!-- _class: closing-page -->
<!-- _backgroundImage: url('coconala-theme/assets/images/closing_page_bg.svg') -->

# ご清聴ありがとうございました

## このテンプレートで素晴らしいプレゼンを！

<div class="subtitle">
すべてのパターンを活用して<br/>
効果的なプレゼンテーションを作成しましょう
</div>

<div class="contact-info">
  <strong>テンプレート:</strong> <a href="https://github.com/your-repo/marp-coconala-template">GitHub Repository</a><br/>
  <strong>サポート:</strong> <a href="mailto:support@example.com">support@example.com</a><br/>
  <strong>ドキュメント:</strong> <a href="https://docs.example.com">使い方ガイド</a>
</div>

