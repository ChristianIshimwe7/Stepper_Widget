# Flutter Stepper Form Application

A Flutter application demonstrating a multi-step form using the Stepper widget. This app guides users through a registration process with three distinct steps: Account creation, Address information, and Confirmation.

## Features

- **Multi-step Form**: Three-step registration process
- **Horizontal Stepper**: Clean horizontal navigation between steps
- **Form Validation**: Input fields for user data collection
- **Step Navigation**: Forward, backward, and direct step access
- **Real-time Updates**: Dynamic step state management
- **Confirmation Screen**: Review all entered information before submission

## App Structure

### Step 1: Account Information
- Full Name input field
- Email address input field
- Password input field (obscured text)

### Step 2: Address Information
- Full house address input field
- Pin code input field

### Step 3: Confirmation
- Displays all entered information for review
- Shows: Name, Email, Password, Address, and Pin Code

## Screenshots

The app features a clean Material Design interface with:
- Green app bar with "GeeksforGeeks" branding
- Horizontal stepper navigation
- Outlined input fields
- Continue/Cancel navigation buttons

## Code Structure

```
lib/
├── main.dart          # Main application entry point
├── MyApp              # Root widget with Material app configuration
├── MyHomePage         # Stateful widget containing the stepper logic
└── _MyHomePageState   # State management for the stepper form
```

## Key Components

### Text Controllers
- `name`: Controls the full name input
- `email`: Controls the email input
- `pass`: Controls the password input
- `address`: Controls the address input
- `pincode`: Controls the pin code input

### Stepper Configuration
- **Type**: `StepperType.horizontal`
- **Current Step**: Tracked by `_activeCurrentStep`
- **Navigation**: Continue, Cancel, and Tap navigation enabled

## Getting Started

### Prerequisites
- Flutter SDK (latest stable version)
- Dart SDK
- IDE (VS Code, Android Studio, or IntelliJ)
- Android/iOS emulator or physical device

### Installation

1. **Clone or create the project:**
   ```bash
   flutter create stepper_form_app
   cd stepper_form_app
   ```

2. **Replace the contents of `lib/main.dart` with the provided code**

3. **Get dependencies:**
   ```bash
   flutter pub get
   ```

4. **Run the application:**
   ```bash
   flutter run
   ```

## Usage

1. **Start the App**: Launch the application to see the first step (Account)

2. **Fill Account Information**:
   - Enter your full name
   - Provide email address
   - Set a password

3. **Navigate to Address Step**:
   - Tap "Continue" or click on the "Address" step
   - Enter your full house address
   - Provide pin code

4. **Review Information**:
   - Navigate to the "Confirm" step
   - Review all entered information
   - All data will be displayed for verification

5. **Navigation Options**:
   - Use "Continue" button to move forward
   - Use "Cancel" button to go back
   - Tap directly on any step to jump to it

## Customization Options

### Styling
- Modify `AppBar` colors by changing `backgroundColor` and `foregroundColor`
- Customize input field appearance through `InputDecoration`
- Adjust step icons and colors through `StepState` properties

### Functionality
- Add form validation by implementing validators
- Include data persistence using SharedPreferences or database
- Add submission functionality to send data to a server
- Implement custom step transitions and animations

### Additional Features
- Add loading states during form submission
- Implement error handling and user feedback
- Include form reset functionality
- Add progress indicators

## Dependencies

This application uses only the core Flutter framework:

```yaml
dependencies:
  flutter:
    sdk: flutter
```

No additional packages are required for basic functionality.

## Technical Details

### State Management
- Uses `StatefulWidget` for managing form state
- `TextEditingController` instances for input management
- `setState()` for updating the current active step

### Step States
- `StepState.editing`: Current step being edited
- `StepState.complete`: Completed steps
- Dynamic state assignment based on `_activeCurrentStep`

### Navigation Logic
- Forward navigation: Increment `_activeCurrentStep` 
- Backward navigation: Decrement `_activeCurrentStep`
- Direct navigation: Set `_activeCurrentStep` to tapped index

## Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/new-feature`)
3. Commit your changes (`git commit -am 'Add new feature'`)
4. Push to the branch (`git push origin feature/new-feature`)
5. Create a Pull Request

## License

This project is open source and available under the [MIT License](LICENSE).

## Support

For questions or support, please open an issue in the repository or contact the development team.

---

**Note**: This is a demo application for learning purposes. For production use, consider adding proper form validation, error handling, and data security measures.
