# Mood360 - Professional Mental Health Tracking

<div align="center">

**🧠 Evidence-based mood tracking with clinical-grade assessments**

*Track your mental wellbeing with validated questionnaires used by healthcare professionals worldwide*

[![React Native](https://img.shields.io/badge/React_Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-1B1F23?style=for-the-badge&logo=expo&logoColor=white)](https://expo.dev/)
[![i18next](https://img.shields.io/badge/i18next-26A69A?style=for-the-badge&logo=i18next&logoColor=white)](https://www.i18next.com/)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](LICENSE)

</div>

## 🌟 Overview

Mood360 is a comprehensive mental health tracking application that combines daily mood monitoring with evidence-based clinical assessments. Unlike typical mood trackers, Mood360 integrates validated psychological instruments used by healthcare professionals, making it suitable for both personal wellness and clinical environments.

### ✨ Key Features

- **🏥 Clinical-Grade Assessments**: PHQ-9 (Depression), GAD-7 (Anxiety), and Wellbeing scales with daily auto-prompts
- **📊 Comprehensive Mood Tracking**: Daily mood, activities, sleep quality, and personalized notes
- **💊 Smart Medication Management**: Precise reminders, intake tracking, and delay monitoring
- **📈 Advanced Analytics**: Mood trends, clinical progress tracking, and weekly scoring summaries
- **📋 Professional Data Export**: CSV/PDF export with clinical scores for healthcare providers
- **🌍 Multi-Language Support**: English, Dutch, German, Italian, and Turkish with medical terminology
- **🔒 Privacy-First**: AES-256 encrypted local storage with optional PIN lock screen
- **📱 Cross-Platform**: iOS and Android with portrait-locked professional interface
- **⚙️ Smart Notifications**: Medication reminders, mood check-ins, and motivational content
- **🎯 User Control**: Toggle clinical features on/off, customize notification preferences

## 🎯 Target Audience

### Personal Users
- Individuals managing mental health conditions
- People interested in wellness and self-improvement
- Users recovering from depression, anxiety, or other mental health challenges

### Healthcare Professionals
- Therapists and counselors tracking patient progress
- Psychiatrists monitoring medication effectiveness
- Mental health clinics requiring standardized assessments
- Research institutions studying mood patterns

### Educational Institutions
- Psychology students learning about validated assessment tools
- Universities conducting mental health research
- Medical schools teaching clinical assessment methods

## 🔬 Evidence-Based Approach

### Validated Clinical Instruments

#### PHQ-9 (Patient Health Questionnaire-9)
- **Purpose**: Depression screening and severity assessment
- **Validation**: FDA-approved, used globally by healthcare providers
- **Scoring**: 0-27 scale with clinical interpretation
- **Implementation**: 9 questions rotating daily, complete assessment weekly

#### GAD-7 (Generalized Anxiety Disorder-7)
- **Purpose**: Anxiety disorder screening and monitoring
- **Validation**: Standard clinical tool with extensive research backing
- **Scoring**: 0-21 scale with severity categorization
- **Implementation**: 7 questions integrated into daily rotation

#### Wellbeing Assessment
- **Purpose**: Positive psychology and resilience measurement
- **Basis**: PERMA-W model and validated wellbeing research
- **Scoring**: 1-5 Likert scale measuring life satisfaction
- **Implementation**: 5 questions balancing clinical assessments

### Smart Rotation System
- **Daily Questions**: 3 questions per day (1 from each scale)
- **Weekly Coverage**: Complete all assessments over 7 days
- **Consistent Scheduling**: Same questions on same weekdays
- **Progress Tracking**: Longitudinal analysis of scores over time

## 🏗 Technical Architecture

### Technology Stack
- **Frontend**: React Native with Expo SDK 54
- **Navigation**: React Navigation v6
- **Notifications**: Notifee (cross-platform local notifications)
- **Storage**: AsyncStorage with encrypted SecureKV wrapper
- **Internationalization**: i18next with dynamic language switching
- **Charts**: React Native Chart Kit for mood visualizations

### Core Services

#### `EvidenceBasedQuestionnaireService`
Manages clinical assessments with proper scoring algorithms and data validation.

```javascript
// Get today's 3 questions (1 PHQ-9, 1 GAD-7, 1 Wellbeing)
const questions = EvidenceBasedQuestionnaireService.getTodaysQuestions(t);

// Calculate clinical scores
const scores = EvidenceBasedQuestionnaireService.calculateScores(responses);
// Returns: { phq9: {score: 12, severity: 'moderate'}, gad7: {...}, wellbeing: {...} }
```

#### `DailyMotivationService`
Provides evidence-based motivational content with four types:
- **Personalized Insights**: Data-driven observations about mood patterns
- **Science-Backed Content**: Research-supported wellness tips
- **Reflection Prompts**: Questions encouraging self-awareness
- **Parasympathetic Exercises**: Breathing and mindfulness techniques

#### `NotificationService`
Comprehensive notification system supporting:
- Medication reminders with interactive actions
- Daily mood tracking prompts
- Motivational content delivery
- Background scheduling up to 30 days


## 📱 App Features Deep Dive

### Onboarding Wizard
Multi-step setup process:
1. **Language Selection**: Choose from 5 supported languages
2. **Profile Creation**: Name, gender, birthday for personalization
3. **Medication Setup**: Configure medicines with precise timing
4. **Notification Preferences**: Customize reminder types
5. **PIN Security**: Optional 4-digit PIN for privacy

### Dashboard Analytics
- **KPI Cards**: 7-day averages, trend analysis, entry counts
- **Interactive Charts**: Mood trends with customizable date ranges
- **Sleep Overview**: Quality tracking and pattern analysis
- **Medication Monitoring**: 24-hour intake tracking with delay alerts
- **Activity Correlations**: AI-powered insights linking activities to mood

### Evidence-Based Assessments
- **Professional Modal Interface**: Clean, clinical presentation
- **Progress Indicators**: Visual feedback on completion
- **Skip Options**: Voluntary participation maintaining clinical validity
- **Score Calculations**: Real-time clinical interpretation
- **Historical Tracking**: Longitudinal progress monitoring

### Wellness Features
- **Motivational Content**: 4 types of science-backed content
- **Breathing Exercises**: Guided techniques for parasympathetic activation
- **Mindfulness Practices**: Body scans and grounding exercises
- **Reflection Prompts**: Questions promoting self-awareness

## 🧪 Clinical Features in Action

### Accessing Professional Questionnaires

1. **Daily Prompts**: Questions automatically appear once daily via modal
2. **User Control**: Can be enabled/disabled in Settings → Clinical Questionnaires
3. **Daily Rotation**: Questions change based on day of week (3 questions per day)
4. **Progress Tracking**: Dashboard shows completion statistics and weekly scores

### Validating Assessments

The questionnaires implement official scoring algorithms:

- **PHQ-9**: 0-4 (minimal), 5-9 (mild), 10-14 (moderate), 15-19 (moderately severe), 20+ (severe)
- **GAD-7**: 0-4 (minimal), 5-9 (mild), 10-14 (moderate), 15+ (severe)
- **Wellbeing**: 1-2 (low), 3-3.9 (moderate), 4+ (high)

## 🌍 Internationalization

### Supported Languages
- **English** (en) - Primary language, complete translations
- **Dutch** (nl) - Full medical terminology, professional translations
- **German** (de) - Complete localization
- **Italian** (it) - Full translation coverage
- **Turkish** (tr) - Complete language support

### Medical Terminology
All clinical assessments professionally translated with appropriate medical terminology for each language, ensuring clinical validity across cultures.

## 🔐 Privacy & Security

### Data Protection
- **Local Storage**: All data stored on device using AsyncStorage
- **No Cloud Sync**: Zero external data transmission
- **Encryption**: SecureKV wrapper for sensitive information
- **PIN Protection**: Optional 4-digit security
- **GDPR Compliant**: Privacy-by-design architecture

## 🏥 Clinical Implementation

### For Healthcare Providers

1. **Patient Onboarding**: Guide patients through app setup
2. **Assessment Scheduling**: Recommend daily 3-question completion
3. **Progress Monitoring**: Review weekly assessment completion
4. **Data Export**: Use export features for clinical records
5. **Interpretation**: Apply clinical cut-off scores appropriately

### For Researchers

1. **Data Collection**: Longitudinal mood and clinical data
2. **Standardized Measures**: Validated instruments ensure research validity
3. **Compliance Tracking**: Monitor assessment completion rates
4. **Export Capabilities**: CSV export for statistical analysis

## 🤝 Contributing

### Development Guidelines
- Follow React Native and Expo best practices
- Maintain clinical accuracy in assessment implementations
- Ensure accessibility compliance (screen readers, contrast)
- Add appropriate unit tests for clinical calculations
- Follow semantic versioning for releases

### Clinical Contributions
- Validate any new assessment instruments
- Ensure proper scoring algorithm implementation
- Maintain professional translation quality
- Document any changes to clinical features

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🏆 Recognition

Mood360 incorporates validated clinical instruments developed by:
- **PHQ-9**: Drs. Robert L. Spitzer, Janet B.W. Williams, Kurt Kroenke, et al.
- **GAD-7**: Drs. Robert L. Spitzer, Kurt Kroenke, Janet B.W. Williams, and Bernd Löwe
- **Wellbeing Research**: Based on PERMA-W model and positive psychology research

## 📞 Support

For technical support, clinical questions, or professional implementation:

- **GitHub Issues**: [Report bugs or request features](https://github.com/BigFatherJesus/mood360/issues)
- **Clinical Inquiries**: For healthcare provider implementation support
- **Academic Partnerships**: Research collaboration opportunities

---

<div align="center">

**Mood360 - Where Clinical Science Meets Personal Wellness**

*Empowering individuals and healthcare providers with evidence-based mental health tracking*

[📱 Download](#) • [📖 Documentation](#)

</div>