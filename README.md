<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>עסק באוטומט</title>
    <link href="https://fonts.googleapis.com/css2?family=Rubik:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Rubik', Arial, sans-serif;
            background-color: #f0f0f0;
            color: #003366;
            line-height: 1.6;
            margin: 0;
            padding: 0;
        }
        .container {
            max-width: 800px;
            margin: 20px auto;
            background-color: #ffffff;
            padding: 20px;
            box-shadow: 0 0 10px rgba(0,0,0,0.1);
            border: 3px solid #a311e9;
        }
        header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        .logo {
            width: 200px;
            height: auto;
        }
        h1 {
            color: #a311e9;
            text-align: center;
            font-size: 2.5em;
            flex-grow: 1;
        }
        .content {
            text-align: center;
            font-size: 1.2em;
            max-width: 600px;
            margin: 0 auto;
        }
        form {
            margin-top: 20px;
            display: flex;
            flex-direction: column;
            align-items: center;
        }
        .form-group {
            width: 100%;
            max-width: 400px;
            margin-bottom: 15px;
        }
        label {
            display: block;
            margin-bottom: 5px;
        }
        input[type="text"],
        input[type="email"],
        input[type="tel"] {
            width: 100%;
            padding: 8px;
            border: 1px solid #003366;
            border-radius: 4px;
            font-size: 16px;
        }
        input[type="submit"] {
            background-color: #a311e9;
            color: #ffffff;
            border: none;
            padding: 10px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 18px;
            transition: background-color 0.3s;
        }
        input[type="submit"]:hover {
            background-color: #8e0fd0;
        }
        .background-element {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            z-index: -1;
            opacity: 0.1;
            background-image: 
                radial-gradient(#a311e9 1px, transparent 1px),
                radial-gradient(#003366 1px, transparent 1px);
            background-size: 50px 50px;
            background-position: 0 0, 25px 25px;
        }
    </style>
</head>
<body>
    <div class="background-element"></div>
    <div class="container">
        <header>
            <img src="data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAAGQAAABkCAYAAABw4pVUAAAACXBIWXMAAAsTAAALEwEAmpwYAAAFLElEQVR4nO2dbWhbZRjHm/l9QT8IgohgZTqdw/rNwbYONms3UvFFYVPxhcy5wdxggiI6RMXNidPWlTTx1LWtnbpN6mZrsxeaplmxr1MZ2kEXK3RltHbr1nQ6dG2avpz4xDxjTy/pSZ6Tc5Lc05z/D/6Qh5PnvPz/9+Scck6aEuUJPgfhKAQBQCAIAAJBABAIAoBAEAAEggAg6QVZNJxBVgYymHnpq0I2+QcBgiAIEARBkP+Ooyd78cJtpHovh4u3zMPezXN14a29HOY4Ml9bzEOQZRtSyHV+EQghHwQQBEEQJIaBjN1n8ujkL+sG1PK8uPlcHp3eiW9dA4Eev1eCpBsQhCPtQI6cmsCn3d9z+dSaX7ge5ZDdOIZ66weQxxp+QUdHb+eGWLrWLSsHkg9EWOt+HkXLfC4bdWMYUE7xHF8M1NlLwrp1E3lw0N4g/JHhME/4V+P4qEfX+wHw9wL5i7dG03wLN90ZdHeMoUuHArYHER4+XCJpvtVtEwm9gBaMOAEELQrCNY3/KEnW+LkF/NNWgACIBUFOr5rQNXwp285dMwAByWQQru7nQqXfnLlC3wIEJKEgv6+dEjd65DCHzMRvs9EjfQsgYAkEGVw/LZm7fvt6mpM8DwABKgjEdz+XFi8nLZ0oB5GmF2RFICoG0ftZrqT5dq/LiO7H8rh+sOGKKPMVHUjLgWn0ypFrPEhP00VZ9+P5kF7x8HzO37SY++3S/LIAKVp6QRoCI0xT7eKaP31HSnBGdZ9B76udH5E0P+/lsAA4WEAyEkQGLm/dK6XzAAYEKgHPWD6UhYxfVd6yY+6hLGZbMpxgPBkNIgE/s+oKFwv0Uw8OrDmHPGGI7xEGIEeB5EPpu+dPrlcpb9r9oAvNMJBCANIJuDHME/6w0Mj09PkXM5jvpDXw0k86XtA2F8KF3nSBIOdvuMx1UZ20B14OQ64HS6CbAKKCYx5/K02BlwPB+lk3RrY9Q8lhSS6I4EjXzlFKCh7MxN/UNMc/4U4BRE0i6OmhHq3zQX6uK8ndSCiNzuaHg/g7o5rHPcSJzh5ASGVABoYGpwdj0zHFegxACgE5tWWLuNvLCWS9cOCgTRGD8A8/ycnVI7+ZAAiQAiDD25eJuz11OTLCvCXhCITRjGtRZ5inqE5TH+T6SoO5h3/Qwz8BEFQIBKM1OEcKgeCZ4QIQBGlK/mLbQzFFIQYQBMlIEIAgKQdyaO8mAAEIQNISBKOwULEwCgFJSxCMwr7FwigEJC1BMAoDkEwHwSgMQDIdBKMwAMl0EIzCACTTQTAKA5BVAv4OpTdaAMLHGoFSFqMQkExqWRiFgaQjCEZhIJkOglEYSApAlD4LmxuFRbkb6JiB49m58b8AkhYgCELtlECQtANBEARBEARBEARBEARBEARBEARBEARBEARBEARBNAgfcAW42vMGgu+nsfr54G4R4kCG58/yXOCBGMcZiULwcBQCgEAQAASCACCWApGGAISPewTC8L4oRCIQ5QGEjx/I+iYUYgMQ5ewf6gOEj38UcixKIz+aAUQoZEeGq+5xRIJhHoAkAYLfY3AKgOi9bH0HAEkGCL+X3QZAEpzhuwFI0kLcbZoKMQ0Eo1DTQfB7GccBsGKA4PdmeA8AUUnxQPhtGU4CYNUEvsnILgBWzQGQKg7+U7BkToDc/ATAbGBnBq0LuZ4FwCYHv5U5O6IBCA0OfjOzVQDSnAQAgSAACAQBQCAIAJLG+Remrxk1VNF26wAAAABJRU5ErkJggg==" alt="Logo" class="logo">
            <h1>עסק באוטומט</h1>
        </header>
        <div class="content">
            <h2>ברוכים הבאים לעולם האוטומציות!</h2>
            <p>הגעתם למקום שבו אנחנו הופכים את החיים שלכם לפשוטים ויעילים יותר. כאן תמצאו פתרונות טכנולוגיים מותאמים אישית לעסק שלכם.</p>
            <p>בואו להכיר את הפתרונות המתקדמים שלנו – אוטומציות ובוטים שיביאו את העסק שלכם למקום החדשני ביותר!</p>
        </div>
        
        <form id="contactForm">
            <div class="form-group">
                <label for="fullName">שם מלא:</label>
                <input type="text" id="fullName" name="fullName" required>
            </div>
            
            <div class="form-group">
                <label for="email">אימייל:</label>
                <input type="email" id="email" name="email" required>
            </div>
            
            <div class="form-group">
                <label for="phone">מספר טלפון:</label>
                <input type="tel" id="phone" name="phone" pattern="^05\d{8}$" placeholder="05xxxxxxxx" required>
            </div>
            
            <input type="submit" value="שלח">
        </form>
    </div>

    <script>
        document.getElementById('contactForm').addEventListener('submit', function(e) {
            e.preventDefault();
            // כאן נוסיף קוד לשליחת הנתונים ל-Google Script
            fetch('https://script.google.com/macros/s/AKfycbzvlOovFT1UaSb5WXvduPcQ4-epqjytY76EmUkVIIMKUPTOIV7hjSkFqaVXhEI0p0nMTQ/exec', {
                method: 'POST',
                mode: 'no-cors',
                cache: 'no-cache',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({
                    fullName: document.getElementById('fullName').value,
                    email: document.getElementById('email').value,
                    phone: document.getElementById('phone').value
                })
            }).then(() => {
                alert('הטופס נשלח בהצלחה!');
                document.getElementById('contactForm').reset();
            }).catch((error) => {
                console.error('Error:', error);
                alert('הייתה שגיאה בשליחת הטופס. נסו שוב מאוחר יותר.');
            });
        });
    </script>
</body>
</html>
