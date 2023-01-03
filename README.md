# AndroidAntiRootDetection

AARD is a sandboxing app that performs root detection. Root detection is the best practice of Android security.
By using ptrace to call dlopen on the remote process. The loaded library has a constructor that replaces the code of access with its own.
If you look at the Android source code, File.exists calls access. If an app tries to check the presence of su, Therefore we emulate its absence.
