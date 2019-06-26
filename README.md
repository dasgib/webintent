# WebIntent Android Plugin for Cordova

## Why this fork
- Because all other forks did not work

## Installation

    $ cordova plugin add https://github.com/dasgib/webintent

## Usage

See [original repo](https://github.com/cordova-misc/cordova-webintent)

    window.plugins.webintent.startActivity({
      action: window.plugins.webintent.ACTION_VIEW,
      url: 'http://url/to/some/android/package.apk',
      type: 'application/vnd.android.package-archive',
    }, function(success) {
    }, function(error) {
    });
    
Add to AndroidManifest.xml inside &lt;application&gt;:

    <provider android:authorities="${applicationId}.provider" android:exported="false" android:grantUriPermissions="true" android:name="android.support.v4.content.FileProvider">
        <meta-data android:name="android.support.FILE_PROVIDER_PATHS" android:resource="@xml/provider_paths" />
    </provider>

## Licence ##

The MIT License

Copyright (c) 2010-2019 Boris Smus and contributors

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
