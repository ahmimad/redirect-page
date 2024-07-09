# redirect-page
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Redirect</title>
    <script>
        function redirectBasedOnOS() {
            var userAgent = navigator.userAgent || navigator.vendor || window.opera;

            // Detect Android
            if (/android/i.test(userAgent)) {
                window.location.href = "https://play.google.com/store/apps/details?id=com.sonicboom.hastelock&hl=en";
            }
            // Detect iOS
            else if (/iPad|iPhone|iPod/.test(userAgent) && !window.MSStream) {
                window.location.href = "https://apps.apple.com/my/app/hastelock/id6520386383";
            }
            // Other devices
            else {
                window.location.href = "https://qr.codes/qxBSIE";
            }
        }

        window.onload = redirectBasedOnOS;
    </script>
</head>
<body>
    <p>Redirecting...</p>
</body>
</html>
