# SideInstallerReleaseTest

Stand-in for an `altstoreio/AltStore` GitHub release, so the SideInstaller
AltStore prototype (branch `altstore-install`) has a
release to point at.

Each release has one asset, `AltStore.ipa`, so SideInstaller can use
`releases/latest/download/AltStore.ipa` the same way it does for SideStore.

The IPA is AltStore 2.3 (build 70) with its old signing removed:
`embedded.mobileprovision`, `_CodeSignature`, `Extensions/AltMarketplace.appex`,
and the `ALTDeviceID` / `ALTServerID` Info.plist keys. SideInstaller re-signs it
and writes its own `ALTDeviceID` while installing.

This is AltStore's own build, hosted for testing only. It isn't an official
AltStore release channel.
