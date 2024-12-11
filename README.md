# Intermittent Firestore Data Write Failures

This repository demonstrates a bug encountered with Firebase's Firestore. Data writes using the `set()` method are intermittently failing without throwing errors. This behavior is inconsistent and only occurs under certain conditions.  The solution provided addresses the issue by implementing robust error handling and transaction management. 

**Bug:** The original code uses `set()` to update Firestore documents.  Sometimes, data writes succeed, but sometimes they fail silently.  No errors are thrown, and the data doesn't appear in Firestore. 

**Solution:** The solution employs transactions to guarantee atomicity.  The solution also incorporates improved error handling that helps pinpoint when and why the write fails.