# Smart-Expense-Tracker

A feature-rich Flutter expense tracker featuring intelligent voice input, OCR processing, interactive analytics, and reactive state management.

## 🚀 Overview

Built with scalability and user experience in mind, this application goes far beyond basic CRUD operations. It acts as a comprehensive personal finance dashboard, offering intelligent data entry methods and deep analytics to help users maintain total control over their economy.

## ✨ Key Features

* **🤖 Intelligent Data Entry:** Speech-to-text recognition with customizable processing rules and ticket scanning via OCR.
* **📊 Advanced Analytics Dashboard:** Interactive comparative bar charts (monthly and weekly). Long-press reveals dynamic daily breakdowns via line charts.
* **🔍 Deep Filtering:** Global search across concepts and notes, combined with custom category tags and date range filters.
* **⚙️ High Customization:** Management of custom concepts, setting monthly spending limits, and defining global budget alerts.
* **🛡️ Security & Reliability:** Built-in password protection, data export options, and a 7-day recovery recycle bin for secure management.

## 🛠️ Tech Stack & Development Flow

* **Framework:** Flutter (Dart)
* **Local Storage:** [Hive](https://pub.dev/packages/hive) (Lightweight NoSQL database).
* **State Management:** Native and reactive `ValueListenableBuilder` tied to Hive database mutations.
* **AI & Hardware Integration:**
  * `google_mlkit_text_recognition`: On-device machine learning for OCR.
  * `speech_to_text`: Microphone hardware access.
  * Complex Regex algorithms for natural language processing (entities, dates, amounts).
* **Custom UI & Charts:** Analytical charts natively implemented using `CustomPainter` and `InteractiveViewer` for horizontal scrolling.
* **Security & Data Export:** `crypto` (local SHA-256 hashing), `file_saver`, and `share_plus` for CSV generation.
* **🤖 Development Approach:** Designed and coded in VS Code using **GitHub Copilot** as an AI assistant to accelerate the implementation of complex logic (such as Canvas math and Regex patterns) and increase overall productivity.

## 📱 App Showcase & Key Interactions

### 1. Intelligent Data Entry (OCR & Voice)

The app leverages on-device AI to eliminate friction from manual data entry.

<table width="100%" cellspacing="0" cellpadding="0">
  <tr>
    <td width="50%" align="center" valign="top">
      <b>📷 OCR Ticket Scanner</b>
    </td>
    <td width="50%" align="center" valign="top">
      <b>🎙️ Voice Input (NLP)</b>
    </td>
  </tr>
  <tr>
    <td valign="top" align="center">
      <p align="center"><i>Automatically extracts totals and dates from physical receipts using Google ML Kit.</i></p>
      <img src="assets/videos/video_demo_ocr_scan_0.gif" width="90%">
    </td>
    <td valign="top" align="center">
      <p align="center"><i>Analyzes amounts, dates, and context to automatically assign categories and concepts.</i></p>
      <img src="assets/videos/video_demo_voice_input_0.gif" width="90%">
    </td>
  </tr>
</table>

> **Note:** Voice-to-text recognition and receipt OCR scanning are considered experimental features. Accuracy may vary depending on environmental factors, camera quality, and voice clarity. Continuous optimization of the parsing algorithms is currently underway.

<br>

### 2. Advanced Analytics & Custom Charts

A dedicated dashboard built entirely with custom rendering (`CustomPainter`) for high-performance financial tracking.

<table width="100%" cellspacing="0" cellpadding="0">
  <tr>
    <td width="50%" align="center" valign="top">
      <b>📊 Quick Navigation & Filters</b>
    </td>
    <td width="50%" align="center" valign="top">
      <b>📈 Interaction & Daily Detail</b>
    </td>
  </tr>
  <tr>
    <td valign="top" align="center">
      <p align="center"><i>Instantly toggle between monthly and weekly comparative views.</i></p>
      <img src="assets/videos/video_demo_analytics_nav.gif" width="90%">
    </td>
    <td valign="top" align="center">
      <p align="center"><i>Long press to reveal a line chart with daily breakdowns and dynamic scaling.</i></p>
      <img src="assets/videos/video_demo_analytics_interaction.gif" width="90%">
    </td>
  </tr>
</table>

<br>

### 3. Comprehensive Management, Settings & Security

Built to be robust, highly customizable, and safe against user error, including encrypted password protection, CSV export, and a preventive deletion system.

<table width="100%" cellspacing="0" cellpadding="0">
  <tr>
    <td width="33.3%" align="center" valign="top">
      <b>Swipe</b><br>
      <img src="assets/images/demo_delete_flow_1.jpeg" width="95%">
    </td>
    <td width="33.3%" align="center" valign="top">
      <b>Confirm</b><br>
      <img src="assets/images/demo_delete_flow_2.jpeg" width="95%">
    </td>
    <td width="33.3%" align="center" valign="top">
      <b>Undo</b><br>
      <img src="assets/images/demo_info_buner_opcion_deshacer.jpeg" width="95%">
    </td>
  </tr>
  <tr>
    <td width="33.3%" align="center" valign="top">
      <br><b>Settings</b><br>
      <img src="assets/images/demo_settings_management_0.jpeg" width="95%">
    </td>
    <td width="33.3%" align="center" valign="top">
      <br><b>Trash Bin</b><br>
      <img src="assets/images/demo_trash_0.jpeg" width="95%">
    </td>
    <td width="33.3%" align="center" valign="top">
      <!-- Empty cell to maintain formatting -->
    </td>
  </tr>
</table>