# CyberGuard - Interactive Password Security Suite

## Core Interaction Flow

### Page 1: Main Selection Hub (index.html)
**Primary Interface**: Terminal-style selection menu with three main options
- **Option 1**: "Password Strength Analysis" - Leads to strength checker
- **Option 2**: "Encryption Vault" - Direct to encryption/decryption page
- **Option 3**: "Security Dashboard" - Shows saved encrypted passwords

**Interactive Elements**:
- Hacker-style terminal with typing animation
- Glowing button effects on hover
- Matrix-style background with falling code
- Cursor-following neon trail effect

### Page 2: Password Strength Analyzer (strength.html)
**Primary Interface**: Real-time password analysis with visual feedback
- **Input Field**: Password entry with masked/unmasked toggle
- **Strength Meter**: Dynamic progress bar with color coding (red→yellow→green)
- **Criteria Checklist**: Live validation showing:
  - Length requirements (8+ characters)
  - Uppercase/lowercase mix
  - Numbers inclusion
  - Special characters
  - Common password detection
- **Encryption Shortcut**: "Encrypt This Password" button that passes the current password to the encryption page

**Interactive Elements**:
- Real-time strength calculation as user types
- Animated strength meter with particle effects
- Criteria items check off with satisfying animations
- "Copy to Clipboard" functionality
- Quick encrypt button with smooth transition

### Page 3: Encryption/Decryption Vault (vault.html)
**Primary Interface**: Dual-panel system for encryption and decryption
- **Encryption Panel** (Left):
  - Password input field
  - Encryption method selector (AES, Base64, Custom)
  - Generate encrypted hash
  - Save to vault option
  - Copy encrypted result
  
- **Decryption Panel** (Right):
  - Encrypted hash input
  - Password recovery display
  - Delete from vault option
  - History of encrypted passwords

**Interactive Elements**:
- Tab switching between encrypt/decrypt modes
- Animated hash generation with loading effects
- Local storage persistence for saved passwords
- Search functionality in password history
- Delete confirmation modals

### Page 4: Security Dashboard (dashboard.html)
**Primary Interface**: Overview of security status
- **Password Health Score**: Overall security rating
- **Saved Passwords List**: All encrypted passwords with metadata
- **Security Recommendations**: Personalized tips
- **Export/Import**: Backup functionality

## Multi-Page Navigation Flow
1. **Entry Point**: User lands on main selection hub
2. **Strength Check Path**: Index → Strength → (optional) Encrypt
3. **Direct Encrypt Path**: Index → Vault → Encrypt
4. **Recovery Path**: Index → Vault → Decrypt
5. **Dashboard Path**: Index → Dashboard for overview

## Technical Implementation Notes
- **Local Storage**: Encrypted passwords saved with timestamps
- **Encryption**: Client-side JavaScript encryption using Web Crypto API
- **Strength Algorithm**: Custom scoring based on multiple criteria
- **Responsive Design**: Mobile-friendly hacker interface
- **Accessibility**: Keyboard navigation and screen reader support

## User Experience Enhancements
- **Progressive Disclosure**: Advanced features revealed as needed
- **Contextual Help**: Tooltips explaining security concepts
- **Visual Feedback**: Every action has immediate visual response
- **Error Handling**: Graceful failure with helpful messages
- **Performance**: Smooth animations without blocking UI