---
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Youni Lab Design System
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

name:          Youni Lab Design System
version:       "2.3"
token_source:  Figma Variables
architecture:  ref → sys → comp

changelog:
  "2.3":
    - topbar.height 修正為 56px（原 60px 為筆誤）
    - shadow.md（dropdown）更新為 0 4px 16px rgba(0,0,0,0.08)
    - layout.sidebar.width 統一為 240px（移除舊 220-260px 範圍值）
    - page-types 補全所有 Template 頁型寬度規格
    - page-samples 移除 Error 頁（合併至 Empty State），新增 Login 頁
    - button-conventions 補上 error（outline）variant 說明
    - card-header 新增標準規格區塊
    - search-input / command-palette 補上觸發規則


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Philosophy — 設計理念
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

philosophy:

  - principle:    Human-Centered
    description:  AI is a collaborative partner, not just a tool.
                  The interface should minimize cognitive load.

  - principle:    Natural Interaction
    description:  Reduce learning cost through natural language
                  and clear structure.

  - principle:    Warm Trust
    description:  Deliver a stable, reassuring experience
                  under rigorous information architecture.


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Principles — 設計原則
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

principles:

  - name:  Restraint is Power
    rule:  Brand colors gain impact through scarcity.
           Primary navy appears only at highest-weight interaction points.
           Accent amber ≤5% of screen area.

  - name:  Strong Spatial Contrast
    rule:  Dark navigation + white workspace.
           Sidebar provides spatial orientation.
           Main area stays white for maximum readability.

  - name:  Spacious Immersive
    rule:  Layout density between standard SaaS and marketing sites.
           Generous card gaps (24px), comfortable row heights (48px),
           ample padding (20-24px).

  - name:  Progressive Radius
    rule:  Larger elements get larger radius.
           12px cards > 8px buttons > 6px badges > 4px small elements.
           No 0px sharp corners. No >16px except full.

  - name:  Weight-Driven Hierarchy
    rule:  Hierarchy through font weight first, color second, size last.
           Regular → Medium → Semibold → Bold.
           Max 5 font sizes per page.

  - name:  Minimal Tables
    rule:  Horizontal dividers only. No vertical lines.
           Low-profile headers. 48px row height.
           Hover feedback with subtle gray.

  - name:  Clear Intent
    rule:  "Button pairs: outline cancel + filled confirm (confirm on right).
           Danger = red fill. Add item = dashed border.
           Labels use verb + noun."

  - name:  Tonal Layering over Shadows
    rule:  Depth through color tones and borders, not heavy shadows.
           Shadows only for floating elements
           (modal, drawer, card hover, focus ring).

  - name:  Brand Consistency
    rule:  Logo min height 32px, 2x clearance.
           Dark logo on light bg, white logo on dark bg.
           No logo on complex backgrounds.


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Colors — 色彩系統
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

colors:

  # Brand ─────────────────────────────
  primary:          '#0A2B41'
  primary-hover:    '#2E4A5E'
  primary-pressed:  '#061A28'
  primary-light:    '#E7EAEC'

  accent:           '#FDB338'
  accent-hover:     '#FFC861'
  accent-pressed:   '#D68C24'

  # Semantic ──────────────────────────
  info:             '#1677FF'
  info-light:       '#E6F4FF'
  info-text:        '#0958D9'
  info-border:      '#91CAFF'

  success:          '#52C41A'
  success-light:    '#F6FFED'
  success-text:     '#389E0D'
  success-border:   '#B7EB8F'

  warning:          '#FDB338'
  warning-light:    '#FFFCF0'
  warning-text:     '#AD6800'
  warning-border:   '#FFC861'

  error:            '#F5222D'
  error-light:      '#FFF1F0'
  error-text:       '#CF1322'
  error-border:     '#FFA39E'

  # Text ──────────────────────────────
  text-primary:     '#1F1F1F'
  text-secondary:   '#595959'
  text-description: '#8C8C8C'
  text-disabled:    '#BFBFBF'
  text-inverse:     '#FFFFFF'

  # Surface ───────────────────────────
  surface-page:     '#F5F5F5'
  surface-default:  '#FFFFFF'
  surface-secondary:'#FAFAFA'
  surface-tertiary: '#F5F5F5'
  surface-disabled: '#F0F0F0'
  surface-inverse:  '#1F1F1F'

  # Border ────────────────────────────
  border-default:   '#D9D9D9'
  border-strong:    '#BFBFBF'
  border-subtle:    '#F0F0F0'
  overlay:          'rgba(0,0,0,0.4)'

  # Ratio ─────────────────────────────
  color-ratio:
    white-gray:     '70-75%'
    navy:           '15-20%'
    semantic:       '5-8%'
    amber:          '≤5%'

  # Scales (ref) ──────────────────────
  theme-scale:
    - '#E7EAEC'  # 50
    - '#C4CDD3'  # 100
    - '#9AABB7'  # 200
    - '#718491'  # 300
    - '#4D6577'  # 400
    - '#2E4A5E'  # 500
    - '#0A2B41'  # 600 ← primary
    - '#082335'  # 700
    - '#061A28'  # 800
    - '#04111B'  # 900

  blue-scale:
    - '#E6F4FF'  # 50
    - '#BAE0FF'  # 100
    - '#91CAFF'  # 200
    - '#69B1FF'  # 300
    - '#4096FF'  # 400
    - '#1677FF'  # 500
    - '#0958D9'  # 600
    - '#003EB3'  # 700

  green-scale:
    - '#F6FFED'  # 50
    - '#D9F7BE'  # 100
    - '#B7EB8F'  # 200
    - '#95DE64'  # 300
    - '#73D13D'  # 400
    - '#52C41A'  # 500
    - '#389E0D'  # 600

  orange-scale:
    - '#FFFCF0'  # 50
    - '#FFF1B8'  # 100
    - '#FFC861'  # 200
    - '#FDB338'  # 300 ← accent
    - '#F09C20'  # 400
    - '#D68C24'  # 500
    - '#AD6800'  # 600

  red-scale:
    - '#FFF1F0'  # 50
    - '#FFCCC7'  # 100
    - '#FFA39E'  # 200
    - '#FF7875'  # 300
    - '#FF4D4F'  # 400
    - '#F5222D'  # 500
    - '#CF1322'  # 600

  neutral-scale:
    - '#FFFFFF'  # 0
    - '#FAFAFA'  # 50
    - '#F5F5F5'  # 100
    - '#F0F0F0'  # 200
    - '#D9D9D9'  # 300
    - '#BFBFBF'  # 400
    - '#8C8C8C'  # 500
    - '#595959'  # 600
    - '#434343'  # 700
    - '#262626'  # 800
    - '#1F1F1F'  # 900
    - '#000000'  # 1000

  purple-scale:
    - '#F5F3FF'  # 50
    - '#EDE9FE'  # 100
    - '#DDD6FE'  # 200
    - '#C4B5FD'  # 300
    - '#A78BFA'  # 400
    - '#8B5CF6'  # 500
    - '#7C3AED'  # 600
    - '#6D28D9'  # 700


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Typography — 字體排版
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

typography:

  font-family:      "'Inter', 'Noto Sans TC', -apple-system, sans-serif"
  font-family-mono: "'IBM Plex Mono', 'Menlo', monospace"

  #               size    weight  lineHeight
  display:      { size: 36px, weight: 700, lineHeight: 44px }
  h1:           { size: 32px, weight: 700, lineHeight: 40px }   # 頁面主標題
  h2:           { size: 24px, weight: 600, lineHeight: 32px }   # 區塊標題
  h3:           { size: 20px, weight: 600, lineHeight: 28px }   # 卡片標題（Page Header）
  h4:           { size: 16px, weight: 600, lineHeight: 24px }   # 表單區塊標題
  card-header:  { size: 15px, weight: 600, lineHeight: 22px }   # Card header 分區標題（v2.3 新增）
  body-lg:      { size: 16px, weight: 400, lineHeight: 24px }
  body-md:      { size: 14px, weight: 400, lineHeight: 22px }
  body-sm:      { size: 13px, weight: 400, lineHeight: 20px }
  caption:      { size: 12px, weight: 400, lineHeight: 18px }
  overline:     { size: 11px, weight: 500, lineHeight: 16px, letterSpacing: 0.06em }
  label:        { size: 13px, weight: 500, lineHeight: 18px }
  code:         { size: 13px, weight: 400, lineHeight: 20px, family: mono }
  data-lg:      { size: 28px, weight: 600, lineHeight: 36px }
  data-md:      { size: 20px, weight: 600, lineHeight: 28px }


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Spacing / Radius / Border — 間距系統
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

spacing:
  base:   8px
  xs:     2px       # Pill 垂直 padding 等邊緣情境
  sm:     4px
  md:     8px
  lg:     16px
  xl:     24px
  2xl:    32px
  3xl:    48px
  4xl:    64px

rounded:
  none:   0px
  sm:     4px       # small button, checkbox
  md:     8px       # button, input, toast
  lg:     12px      # card, table, modal
  xl:     16px
  full:   9999px    # pill, avatar, switch

border:
  default:  1px
  medium:   1.5px   # checkbox, radio, choicebox
  strong:   2px     # focus indicator, tab underline

scrollbar:                                   # v2.2：全站統一卷軸（細灰、常駐）
  width:        8px
  height:       8px
  thumb:        "#D9D9D9"
  thumb-hover:  "#BFBFBF"
  track:        transparent
  radius:       4px
  firefox:      "scrollbar-width:thin; scrollbar-color:#D9D9D9 transparent"
  note:         "所有卷動容器一致；橫向與縱向同樣式，避免一大一小"


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Shadow / Opacity / Animation
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

shadow:
  xs:           '0 1px 2px rgba(0,0,0,0.05)'
  sm:           '0 1px 3px rgba(0,0,0,0.08)'       # card hover, toggle
  md:           '0 4px 16px rgba(0,0,0,0.08)'      # dropdown、filter panel（v2.3 更新）
  lg:           '0 8px 24px rgba(0,0,0,0.1)'       # drawer
  xl:           '0 20px 60px rgba(0,0,0,0.15)'     # modal、command palette
  focus:        '0 0 0 3px rgba(10,43,65,0.08)'    # focus ring
  error-focus:  '0 0 0 3px rgba(245,34,45,0.08)'   # error focus ring

opacity:
  disabled:     0.4
  hover:        0.85
  overlay:      0.4

z-index:
  base:         0       # 頁面內容
  sticky:       100     # Top Header（sticky）
  popover:      1000    # Dropdown、Select 選單、Date Picker 面板、Filter Panel
  drawer:       1100    # Drawer 與遮罩
  modal:        1200    # Modal 與遮罩、Command Palette
  toast:        1300    # Toast 通知
  tooltip:      1400    # Tooltip（永遠最上層）

animation:
  fast:         150ms     # hover, focus
  normal:       200ms     # switch, transform
  slow:         250ms     # drawer slide
  progress:     400ms     # progress bar fill
  spinner:      1s        # spinner rotation
  easing:       ease


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Layout — 佈局
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

layout:
  sidebar:
    width:      240px     # v2.3 統一（移除舊 220-260px 範圍值）
    bg:         primary
  content:
    maxWidth:   1200px
  density:      spacious-immersive
  card-gap:     24px
  card-padding: 24px
  table-row-height: 48px


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Icon System — 圖示系統（v2.1 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

icon-system:

  library:        Feather Icons            # v2.2 自 Material Symbols 全面遷移
  version:        "4.29"
  npm:            react-feather             # 正式專案用此套件，名稱一一對應（more-vertical ↔ MoreVertical）
  implementation: inline SVG                # 設計系統文件以內聯 SVG 呈現（FI helper / FI_PATHS 字典）
  spec:           "viewBox 24×24, stroke-width 2, round linecap/linejoin, currentColor"

  rules:
    - 全站唯一 icon 庫，禁止混用其他 icon 庫
    - 不使用 emoji 代替功能性圖示
    - 不修改 stroke-width
    - Feather 無合適圖示時才允許自訂，需符合 24×24 / stroke-width 2 / 圓端點，並於 Iconography 頁登記

  # 尺寸對照
  sizes:
    xs:   12px    # 下拉子選單箭頭、快捷操作列
    sm:   14px    # chevron、搜尋框內、輔助圖示、Row Actions
    md:   16px    # 選單項目、按鈕內、inline
    lg:   18px    # Top Header icon 按鈕、Sidebar 收折鈕
    xl:   20px    # Sidebar nav item

  # 顏色規則
  color-rule:
    nav-default:  '#8C8C8C'     # 未選中導覽圖示
    nav-active:   '#0A2B41'     # 選中導覽圖示
    emphasis:     '#595959'     # 強調 / hover
    danger:       '#CF1322'     # 危險動作
    button:       inherit       # 繼承按鈕文字色
    muted:        '#BFBFBF'     # 禁用 / 輔助
    disabled:     'opacity 0.4' # 禁用維持原色、降透明度

  # 常用語意對照
  semantic:
    新增: plus           編輯: edit-2        刪除: trash-2
    查看: eye            複製: copy          分享: share-2
    停用: slash          上傳: upload        下載: download
    搜尋: search         篩選: filter        設定: settings
    更多: more-vertical / more-horizontal
    通知: bell           日期: calendar      關閉: x
    確認: check / check-circle              警告: alert-circle
    資訊: info           外部連結: external-link
    重新整理: refresh-cw  登出: log-out
    # v2.3 移除 help-circle（Top Header v2.2 已移除幫助鈕）


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Admin Layout — 後台佈局規格（v2.1 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

admin-layout:

  type:           sidebar + topbar + main-content

  sidebar:
    width:        240px
    widthCollapsed: 56px                        # 收折狀態，icon-only
    bg:           '#FFFFFF'
    style:        Light Sidebar                 # 白底深字（參考 Metronic Demo6）
    position:     fixed left                    # 固定左側

    logo:
      height:       56px                        # 與 topbar 同高
      padding:      '0 14px'
      img:          { tag: '<img>', height: 24px, widthAuto: true }
      collapse-btn:
        icon:       sidebar                     # Feather Icons
        size:       18px
        position:   right                       # 展開時靠右，收折時置中
        radius:     6px
        hoverBg:    '#F0F0F0'

    collapsed:
      width:        56px
      logo:         hidden
      nav-label:    hidden
      section-heading: hidden
      nav-badge:    hidden
      search:       hidden
      spaces:       hidden
      user-info:    hidden
      icon:         centered

  topbar:
    height:       56px                          # v2.3 修正（原 60px 為筆誤）
    bg:           '#FFFFFF'
    border:       '1px solid #F0F0F0'
    shadow:       '0 1px 2px rgba(0,0,0,0.04)'
    right:        [search, bell, avatar]        # v2.2：search icon 開 Command Palette
    removed:      help-circle                   # v2.2 移除

  content:
    marginLeft:   240px                      # 對應 sidebar 寬度
    padding:      '24px 32px'
    bg:           '#F5F5F5'                  # surface-page
    maxWidth:     none                       # 全寬，內部 card 自行約束

  # 視窗高度策略（v2.2）：整個 app 固定 100vh、不產生頁面卷軸
  viewport-height:
    app:          'height:100vh; overflow:hidden — 整頁不卷，避免雙卷軸'
    shell-fixed:  'Sidebar / Top Header / Tabs / Toolbar / Pagination 固定不卷'
    scroll-area:  '僅資料區（如表格 table-scroll）以 flex:1 撐滿剩餘高度、內部垂直卷動'
    rationale:    '後台單視窗體驗（如 Gmail/Linear）；使用者只面對一個卷軸，不混淆'
    list-heavy:   '列表頁：content 不卷，表格 flex:1 內部卷 + sticky thead + 固定 Pagination'
    content-heavy:'內容頁（如總覽多區塊）：content 區整體可卷，topbar 固定'

  page-max-width:  1200px                    # 內容區最大寬度

  breakpoints:
    collapse-sidebar: 1024px                 # 以下 sidebar 收折
    mobile:           768px


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Data Visualization — 資料視覺化（v2.2 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

data-viz:

  approach:   single-hue            # 同色系深淺，取 Blue 色階

  # 多系列取色順序（Blue 色階由深至淺）
  palette:
    - '#003EB3'  # Blue 700 · 最深
    - '#0958D9'  # Blue 600
    - '#1677FF'  # Blue 500 · 主藍
    - '#4096FF'  # Blue 400
    - '#69B1FF'  # Blue 300
    - '#91CAFF'  # Blue 200 · 最淺

  strategy:
    single-series:   "主藍 Blue 500 #1677FF（折線、直條、階段橫條、Progress）"
    multi-series:    "Blue 色階由深至淺依序取（上方 palette 順序）"
    dual-compare:    "Blue 700 + Blue 300，同色系拉開明度"
    strong-distinct: "類別差異大且需一眼分辨，才改用其他色階輔助；預設不混色系"
    magnitude:       "色階深淺對應數值高低（熱力圖 Blue 200→700）"

  charts:           [line, bar, pie/donut, stage-bar, ranking-bar, segmented-bar]
  warning-color:    '#F5222D'        # 排行條超標等語意警示，不屬資料系列配色
  implementation:   inline SVG       # 無外部圖表庫依賴
  states:
    empty:    "置中『尚無資料』13px #BFBFBF，不畫空座標軸"
    loading:  "Spinner 置中"
    tooltip:  "深色 #1F1F1F / 圓角 6 / 白字"


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Button Conventions — 按鈕列慣例（v2.2 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

button-conventions:

  alignment:    right            # 三類容器一致：靠右、主按鈕在最右
  rationale:    "符合由左到右閱讀、右為前進；跨容器一致"

  containers:
    page-form:   "取消 → 儲存（主按鈕在右）"
    modal:       "取消 → 確認（主按鈕在右）"
    wizard:      "上一步 → 下一步／完成（精靈，靠右）"

  # variant 對應情境（v2.3 補全）
  variants:
    primary:     "主要操作（儲存、確認、建立）— 深藍填色"
    secondary:   "次要操作（取消、返回）— 白底灰框"
    error:       "危險操作 outline 版（刪除帳號等設定頁危險區）— 白底紅字紅框；與 danger（紅填色）區分：danger 用於 Modal 確認刪除，error 用於設定頁行內危險動作"
    danger:      "Modal 內不可逆確認（永久刪除）— 紅色填色"
    ghost:       "低權重輔助操作 — 透明底"
    warning:     "警告性操作 — 琥珀色填色"

  danger:       "危險操作（如刪除帳號）與主按鈕列分離，置於獨立危險卡片（border #FFA39E）"
  gap:          8px


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Card Header — 卡片標題規格（v2.3 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

card-header:
  # 所有含分區標題的 Card 統一規格
  # 適用：表單頁、詳情頁、設定頁、個人中心、步驟表單頁的各群組卡片
  fontSize:     15px
  fontWeight:   600
  color:        '#1F1F1F'
  padding:      '16px 24px'
  borderBottom: '1px solid #F0F0F0'
  card:         'overflow: hidden（確保圓角正確裁切 header 背景）'

  # 危險操作卡片的 header
  danger-card:
    color:        '#CF1322'
    borderBottom: '1px solid #FFF1F0'
    card-border:  '1px solid #FFA39E'


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Search Input / Command Palette
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

search-input:
  height:       40px
  radius:       8px
  icon:         '14px search, left 12px, color #BFBFBF'
  clear-btn:    '24×24, right 8px, bg #F0F0F0, icon 12px ×'
  shortcut-kbd: '20px height, radius 4, border #E7EAEC, bg #FAFAFA'
  focus:        'border #0A2B41 + shadow 0 0 0 3px rgba(10,43,65,0.08)'
  escape:       '清除輸入內容'

  # Top Header 的搜尋觸發方式（v2.3 新增）
  top-header-trigger:
    type:       'icon-button（非常駐輸入框）'
    size:       '32×32 / radius 6 / icon 18px #595959'
    shortcut:   '⌘K / Ctrl+K'
    opens:      'Command Palette（詳見 COMPONENTS.md command-palette）'
    rule:       'Top Header 不放常駐搜尋框；搜尋框僅出現在 Table Toolbar 中'

command-palette:
  trigger:      'Top Header search icon 或 ⌘K / Ctrl+K'
  overlay:      'rgba(0,0,0,0.4) 全屏遮罩'
  z-index:      1200                          # 同 modal 層級
  position:     '水平置中，距頂 120px'
  panel:
    width:      560px
    max-width:  '90vw'
    radius:     12px
    shadow:     '0 20px 60px rgba(0,0,0,0.15)'
  input:
    padding:    '14px 16px'
    icon:       'search 18px #8C8C8C'
    fontSize:   15px
    esc-hint:   '右側 Esc 標籤（11px / border pill）'
  sections:
    recent:     '未輸入時顯示最近瀏覽（3–5 筆）'
    results:    '輸入後依類別分組（公司 / 任務 / 功能）'
    shortcuts:  '底部常駐快捷操作（新增公司、設定…）'
  list-item:
    padding:    '9px 16px'
    icon-badge: '28×28 / radius 7 / bg #F5F5F5 / icon 14px'
    hover:      '#F5F7F8'
    max-height: '400px（超出捲動）'
  close:        '點遮罩 / Esc / 選取項目'
  keyboard:     '↑↓ 切換 / Enter 選取 / Esc 關閉'


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Responsive — 元件級 RWD（v2.2 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

responsive-rules:

  # ── 斷點定義 ──────────────────────────
  breakpoints:
    desktop:  '≥1280px  — 完整版型'
    laptop:   '1024–1279px — Sidebar 可手動收合，Stat Card 視寬度 2–4 欄'
    tablet:   '768–1023px  — Sidebar 預設收合為 icon-only（56px）'
    mobile:   '<768px      — Sidebar 收起為抽屜（drawer，漢堡鈕開關），內容單欄'

  # ── 版型級 RWD（整頁骨架）──────────────
  layout-level:
    sidebar:
      ">=1024":  '展開 240px / 可手動收合 56px'
      "768-1023": '預設收合 56px（icon-only）'
      "<768":     'drawer：預設隱藏，topbar 出現漢堡鈕，點擊滑出覆蓋層 + 遮罩'
    content-padding:
      ">=1024":  '24px 32px'
      "768-1023": '20px 24px'
      "<768":     '16px'
    topbar-search:
      ">=768":   '顯示'
      "<768":    '收為放大鏡 icon，點擊展開全寬搜尋'

  # ── 元件級 RWD（區塊內部）──────────────
  header-action-rows:
    rule:      'flex-wrap：標題區 flex:1 min-width:240px、操作區 flex-shrink:0'
    behavior:  '寬度不足時操作按鈕整組換行至標題下方、靠左（換行堆疊，方案 A）'
    applies-to: [Page Header, Table Toolbar, Panel 標題列]
  grids:
    stat-card-row:  '≥1440 五欄、1024–1440 兩三欄、<1024 單欄堆疊'
    card-list-grid: '≥1280 三欄、1024–1280 兩欄、<768 單欄'
    dashboard-grid: '主/次網格 1:1；<1024 降為單欄堆疊'
    description-list: '網格式 <1200 降 2 欄、<768 降 1 欄'
  table:
    rule:  '欄位過多時 overflow-x:auto 橫向卷動，操作欄 sticky 固定右側；不擠壓換行'
    row-actions: 'position:sticky right:0 / box-shadow: -4px 0 8px rgba(0,0,0,0.06)'
  charts:
    rule:  '圖表寬度 100% 自適應；圖例在窄寬時移至圖表下方'
  filter-panel:
    ">=1280":   '篩選 Dropdown Panel 向下展開（300px），Toolbar 篩選按鈕觸發'
    "<1024":    '收為 Drawer（從右滑入）'
    usage:      '篩選維度 ≥ 3 個時使用 Panel；1–2 個維度直接用 Select / Tab'

  # 註：本區為單一 RWD 真實來源；工程實作與 AI 生成皆以此為準


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Page-Type Widths — 頁型寬度與對齊（v2.3 補全）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

page-types:

  principle:  "輸入／單一任務型窄而置中；瀏覽／資料密集型寬而滿版"

  # 寬度對照表
  #                     內容寬度              對齊      說明
  dashboard:          { width: "撐滿（上限 1200）",    align: left,   reason: "卡片網格鋪滿可用寬度" }
  list:               { width: "撐滿（上限 1200）",    align: left,   reason: "表格欄位多需寬度" }
  card-list:          { width: "撐滿（上限 1200）",    align: left,   reason: "卡片網格，三欄鋪滿" }
  detail:             { width: "撐滿（雙欄 1:1.6）",   align: left,   reason: "資訊密集多區塊" }
  form:               { width: "720px 置中（卡片填滿）", align: center, reason: "輸入型；720 兩欄舒適" }
  step-form:          { width: "720px 置中（卡片填滿）", align: center, reason: "同表單頁；Steps 條同寬" }
  settings:           { width: "左側導覽 200px + 內容 720px 置中", align: left, reason: "設定頁左 Nav + 右內容，內容同輸入型寬度" }
  profile:            { width: "720px 置中",           align: center, reason: "個人資料為輸入型頁面" }
  login:              { width: "獨立頁面（無 Sidebar）/ 右側表單 360px 置中", align: center, reason: "Auth 頁，左品牌區 + 右表單" }

  # 表單頁卡片結構（v2.2 更新，v2.3 確認）
  form-page-structure:
    width:       'content max-width 720，水平置中；卡片填滿此寬'
    page-header: '36×36 返回方鈕（白底灰框 + chevron-left）+ 標題 20px + 描述 13px'
    card:        'Card 三區 header（15px/600）/ body（24px padding）/ footer（灰底按鈕列）'
    multi-card:  '一頁可堆疊多張 Card；每張同寬 720，間距 16px'
    actions:     '按鈕置於 Card footer（#FAFAFA + 頂線），靠右、主按鈕在右'


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Login Page — 登入頁（v2.3 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

login-page:
  type:         '獨立頁面，無 Sidebar / Top Header'
  layout:       '左右分割：左側品牌區（<900px 隱藏）+ 右側表單區'

  left-panel:
    bg:         'linear-gradient(135deg, #0A2B41 0%, #04111B 100%)'
    content:    '品牌 Logo + 系統名稱 + tagline + 幾何裝飾圖'
    breakpoint: '<900px 隱藏，表單區撐滿全寬'

  right-panel:
    width:      '50vw（<900px 100vw）'
    form-width: '360px 置中'
    bg:         '#FFFFFF'

  form-structure:
    - Logo（小）
    - 標題「歡迎回來」+ 副標
    - Google OAuth 按鈕（白底灰框）
    - OR 分隔線
    - Email 輸入框
    - 密碼輸入框（右側 eye-off toggle）
    - 記住我 checkbox + 忘記密碼連結
    - 登入按鈕（primary lg）
    - 申請試用連結

  footer:
    content:    '系統狀態 + 版本號'
    position:   '右側面板底部 fixed'


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Empty State — 空狀態（v2.3 補全）
# 已在元件頁定義；此處補充與頁面整合規則
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

empty-state-integration:
  # 三種情境
  variants:
    default:     '初始無資料（首次使用）— 主 CTA 引導新增'
    search:      '搜尋 / 篩選無結果 — 清除條件 CTA；Toolbar 保留（讓使用者可調整篩選）'
    permission:  '無存取權限 — 聯絡管理員 CTA（含 403 情境）'

  # 與 Error 頁的關係
  error-note:   '404 / 403 HTTP 錯誤頁以 Empty State 組合實作，不設獨立 Template；
                 403 對應 permission variant；404 對應 default variant（加說明文字）'

  placement:    '置於表格 Card 內垂直置中，Toolbar 是否保留視情境決定（見 search variant）'
  icon-size:    '48px（來自 Empty State 元件規格）'
  title:        '16px 600 #1F1F1F'
  description:  '14px #8C8C8C，最多兩行'


# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━
# Page Samples — 高保真頁面樣板（v2.2 新增）
# ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━

page-samples:

  purpose:   "全尺寸擬真頁面，供工程團隊直接對照開發；嚴格套用本設計系統規範"
  note:      "與設計系統文件中的 Template（縮小示意 + 規格說明）不同，樣板為 1:1 可互動成品頁"

  design-spec:
    file:        younilab-設計規範.html
    version:     "2.3"
    status:      完成（設計規範 · 元件 + Template 全覽）
    templates:
      - Dashboard
      - 列表頁（含 Checkbox 批次選取 + 篩選展開態 Demo）
      - 卡片列表頁（網格 ↔ 列表視圖切換）
      - 詳情頁
      - 表單頁
      - 步驟表單頁
      - 設定頁
      - 個人中心
      - 登入頁（獨立頁面 / 無 Sidebar）
    removed:
      - Error 頁（403/404）→ 合併至 Empty State permission variant

  menu:          # 後台選單結構
    - 總覽（Dashboard）
    - { 列表頁: [一般列表頁, 卡片列表頁] }
    - { 表單頁: [一般表單頁, 步驟表單頁] }
    - 詳情頁
    - 設定頁
    - 個人中心
    # Login 頁為獨立 Auth 頁面，不在後台選單內


---
