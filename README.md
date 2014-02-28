CreatingDocSet-Example
======================

Example app to show how to create a doc set similar to apple doc set in iOS 

Reference Links:

For installation: https://github.com/tomaz/appledoc
Run script details: https://github.com/tomaz/appledoc/blob/master/XcodeIntegrationScript.markdown

Script to execute:

# Start constants
company="xxxxxxxx";
companyID="xxxxxxxx";
companyURL="xxxxxxxx";
target="iphoneos";
#target="macosx";
outputPath="~/Sites/xcode_workspace/_help/${PROJECT_NAME}";
# End constants

/usr/local/bin/appledoc \
--exit-threshold 2 \
--project-name "${PROJECT_NAME}" \
--project-company "${company}" \
--company-id "${companyID}" \
--docset-atom-filename "${company}.atom" \
--docset-feed-url "${companyURL}/docs/%DOCSETATOMFILENAME" \
--docset-package-url "${companyURL}/docs/%DOCSETPACKAGEFILENAME" \
--docset-fallback-url "${companyURL}/docs" \
--docset-platform-family "${target}" \
--keep-intermediate-files \
--keep-undocumented-objects \
--keep-undocumented-members \
--logformat xcode \
--merge-categories \
--no-repeat-first-par \
--no-warn-invalid-crossref \
--no-warn-undocumented-object \
--no-warn-undocumented-member \
--no-warn-empty-description \
--output "${outputPath}" \
--install-docset \
--print-information-block-titles \
--use-code-order \
--verbose 4 \
--ignore "*.m" \
--ignore "LoadableCategory.h" \
--ignore "BuildHeaders" \
--ignore "Igor" \
--ignore "Kiwi" \
--ignore "PublicAutomation" \
--ignore "SDWebImage" \
--ignore "SVProgressHUD" \
--ignore "SVPullToRefresh" \
--ignore "CocoaLumberjack" \
--ignore "Toast" \
--ignore "PonyDebugger" \
--ignore "PonyDebuggerLogger" \
--ignore "SocketRocket" \
"${PROJECT_DIR}"
