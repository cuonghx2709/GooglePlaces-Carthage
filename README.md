This repo is the Google Places API for iOS that you can install using Carthage.  Unfortunately, Google does not natively support Carthage, instead requiring CocoaPods or manual integration, and according to this issue https://issuetracker.google.com/issues/35827791, it seems like official support won't be coming soon.

This repo is up to date as of 2.6.0

In the event that a more recent version is available and not integrated, here's how to do it:

    1. Fork the repo and clone it.
    2. Open the project in Xcode.
    3. Download the desired GooglePlaces distribution from https://developers.google.com/places/ios-api/start as listed in the "Install Manually" tab.
    4. Open up 2 Finder Windows. One focused on the sources folder of your cloned project, the other at the Frameworks folder of the new version of the Places API.
        1. Copy files in the  Headers, Modules, and Resources  into the GooglePlaces (sources) folder of the repo.
        1. Make sure that all headers are added to the project. If you have to add new ones, inspect the header section of the framework's target and make sure that they are added as `public`.
        1. Cop the GooglePlaces binary as well.
    5. Update the version number in GooglePlaces Target.
    6. You may have to read over the GooglePlaces manual installation instructions as required frameworks may have been added.  Compare the requirements with what is specified in the target's `Build Phases`/`Link Binary with Libraries`
    7. (Optional) - Submit a pull request so I can pick up your changes!

This repo was forked from https://github.com/leoneparise/GooglePlaces-Carthage. Unfortunately, it doesn't seem to be updated.


