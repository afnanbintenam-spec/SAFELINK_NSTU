# SafeLink NSTU

SafeLink NSTU is a dedicated mobile-based student safety application. This system ensures faster communication between students and university authorities during emergencies. Students can instantly trigger an SOS alert in critical situations. SafeLink NSTU aims to create a safer campus environment by leveraging technology, ensuring that every student can quickly receive help when they need it most.

## 🚨 Problem Statement
The current system for reporting and responding to student emergencies at Noakhali Science and Technology University (NSTU) is entirely manual, leading to serious inefficiencies and delays in critical situations. When emergencies such as ragging, harassment, or other incidents occur, students have to contact Teachers, Proctor Office or call them directly, a process that is slow and unreliable. There is no centralized platform to collect incident information, verify users, track alerts, or maintain accountability of responses. This lack of a streamlined system creates confusion about who should respond, increases response times, and lowers students’ confidence in campus safety.
SafeLink NSTU solves this by enabling one-tap SOS activation with real-time location and alert updates.

## 💡 Solution Overview
SafeLink NSTU offers a fast and user-friendly safety workflow that allows users to:

- Trigger SOS alerts instantly
- Share live location in real time
- Notify responders through cloud-backed alert flows
- Track and control alert status
- Cancel alerts when the situation is safe
- The system is built for real-time performance and future scalability.

## ✨ Features
- One-tap SOS activation: Instantly send an emergency alert with a single tap.
- Real-time live location sharing: Captures and updates the student's current location.
- Set Pulse feature: For indoor scenarios, students can optionally pre-select building and floor details to accelerate emergency context capture when entering        potentially risky areas. This step is optional and can be skipped.
- Firebase-powered live backend sync: Alert events and status changes are updated instantly.
- Emergency contact escalation support: Supports SMS/call based escalation workflows.
- Alert status monitoring and maintenance: The Proctorial and Security Bodies can monitor and manage active SOS alerts.
- Multi-role dashboard support: Includes role-based flows such as student/proctor/security views.
- Shake-trigger integration: Optional shake-based trigger support for quick emergency activation.
- Volume button emergency trigger: Quick SOS activation using physical volume button press for hands-free operation.
## 🛠️ Technologies Used
- Frontend app development: Flutter (Dart)
- Backend services: Firebase (Cloud Firestore, Authentication, Cloud Functions, Messaging)
- Real-time alert and status updates: Firebase services
- Location services: Geolocator + Geocoding
- Map and location visualization: Google Maps Flutter
- Notification handling: Firebase Messaging + Flutter Local Notifications
## 📊 System Workflow
- User triggers SOS from the app
- System captures current location
- Alert data is sent to Firebase in real time
- Emergency status and location updates are synced instantly
- Responders can process/accept/reject alerts
- User can cancel SOS alert to prevent false alarm.
## Local Development Setup
Prerequisites
- Flutter SDK installed
- Dart SDK 
- Node.js 
- Firebase CLI 
1) Clone and install Flutter dependencies
git clone https://github.com/afnanbintenam-spec/SAFELINK_NSTU.git
cd SAFELINK_NSTU
flutter pub get
2) Run the app

flutter run
Examples:

flutter run -d chrome

3) Setup and run Cloud Functions locally
cd functions
npm install
npm run start
4) Deploy Cloud Functions
cd functions
npm run deploy
Environment and Secrets

## Firebase Safety Notes (Important)
- Keep your existing Firebase project and configuration unchanged unless you intentionally migrate.
- Before deploying functions/rules, always confirm the active project:
	- `firebase login`
	- `firebase use --add` (first time only)
	- `firebase use <your-project-id>`
	- `firebase projects:list` (verify target project)
- Never commit secret files (already protected by `.gitignore`): `serviceAccountKey.json`, `.env`, and local Firebase debug logs.
- Deploy with explicit targets when possible to reduce risk:
	- `firebase deploy --only functions`
	- `firebase deploy --only firestore:rules`

## APK Download & Installation

### Download APK
1. Go to releases page: https://github.com/afnanbintenam-spec/SAFELINK_NSTU/releases
2. Download the latest APK file matching your device:
   - **arm64-v8a** (recommended for most modern devices)
   - **armeabi-v7a** (older Android devices)
   - **x86_64** (emulators, tablets)

### Install APK on Android Device
1. Enable "Unknown Sources" on your phone:
   - Settings → Security → Allow installation from unknown sources
2. Transfer the APK file to your phone
3. Open the APK file and tap "Install"
4. Wait for installation to complete

## How to Use SafeLink NSTU

### Initial Setup
1. **Launch the app** after installation
2. **Sign up/Login**
   - Provide your email and create a password
   - Verify your email address
3. **Complete profile setup**
   - Enter your name, student ID (if applicable)
   - Select your role: Student, Proctor, or Security Staff
4. **Set up optional features**
   - Set Pulse: Mark your frequent locations (building/floor) for faster SOS context
   - Enable shake-detection or volume button triggers (optional)

### For Students: Triggering SOS Alert
1. **Emergency situation?** Single tap the large **SOS button** on home screen
2. **Instant actions triggered:**
   - Your live location is captured
   - Alert sent to nearby proctors and security staff
   - Your emergency contact details shared
3. **Share live location** - System continuously updates your location until alert resolved
4. **Cancel alert** - Tap "Cancel SOS" when situation is resolved
5. **Volume button shortcut** - Press volume buttons simultaneously for quick SOS (if enabled)

### For Proctors/Security Staff: Managing Alerts
1. **View all active alerts** on dashboard
2. **Alert details include:**
   - Student location on map
   - Alert type and severity
   - Student contact information
3. **Actions available:**
   - Accept/Acknowledge the alert
   - View student location on map
   - Contact student directly (call/SMS)
   - Mark alert as resolved
4. **Escalation support** - Automatic SMS/call to additional contacts if needed

### Key Features
- **One-Tap SOS**: Emergency activation with single button press
- **Live Location Tracking**: Real-time location updates for responders
- **Set Pulse**: Pre-marked safe zones and building details for faster response
- **Shake Detection**: Activate SOS by shaking (optional)
- **Volume Button Trigger**: Hands-free SOS using physical buttons
- **Role-Based Views**: Different dashboards for students, proctors, and security
- **Multi-Contact Escalation**: SMS and call alerts to multiple responders
- **Map Integration**: Visual location tracking for emergency response

### Troubleshooting

**App won't open:**
- Uninstall and reinstall the APK
- Check storage space on your device
- Ensure minimum Android version: 5.0+

**Location not updating:**
- Enable GPS on your device
- Grant location permissions in app settings
- Check app has background permission enabled

**Not receiving alerts:**
- Ensure Firebase Messaging permissions are enabled
- Check internet connection (WiFi or mobile data)
- Restart the app

**Can't log in:**
- Verify internet connection
- Reset password via "Forgot Password"
- Contact your administrator

### Support & Feedback
For issues or feature requests, contact NSTU Safety Team or open an issue on GitHub: https://github.com/afnanbintenam-spec/SAFELINK_NSTU/issues
