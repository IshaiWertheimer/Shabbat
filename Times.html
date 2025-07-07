<!DOCTYPE html>
<html lang="he" dir="rtl">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>זמני השבוע - גבעת שמואל</title>
    <style>
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
            line-height: 1.6;
            background-color: #f4f4f4;
            color: #333;
            max-width: 800px;
            margin: 20px auto;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
        }
        header {
            text-align: center;
            border-bottom: 2px solid #0056b3;
            padding-bottom: 10px;
            margin-bottom: 20px;
        }
        h1 {
            color: #0056b3;
        }
        h2 {
            color: #007bff;
            border-bottom: 1px solid #ddd;
            padding-bottom: 5px;
        }
        #content {
            display: none; /* Hidden by default, shown after loading */
        }
        #loader {
            text-align: center;
            font-size: 1.2em;
            padding: 40px;
        }
        .info-box {
            background-color: #fff;
            padding: 15px;
            margin-bottom: 20px;
            border-radius: 8px;
        }
        .shabbat-times {
            display: flex;
            justify-content: space-around;
            text-align: center;
        }
        .shabbat-times div {
            flex: 1;
        }
        .shabbat-times strong {
            font-size: 1.5em;
            color: #d9534f;
        }
        .week-times table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 10px;
        }
        .week-times th, .week-times td {
            text-align: right;
            padding: 8px;
            border: 1px solid #ddd;
        }
        .week-times th {
            background-color: #e9ecef;
        }
        .parasha {
            text-align: center;
            font-size: 1.8em;
            font-weight: bold;
            color: #28a745;
        }
        footer {
            text-align: center;
            margin-top: 20px;
            font-size: 0.8em;
            color: #666;
        }
    </style>
</head>
<body>

    <header>
        <h1>זמני השבוע והשבת</h1>
        <p>גבעת שמואל</p>
    </header>

    <div id="loader">טוען נתונים... ⏳</div>

    <div id="content">
        <div class="info-box">
            <h2>פרשת השבוע</h2>
            <p id="parasha" class="parasha">טוען...</p>
        </div>

        <div class="info-box">
            <h2>זמני כניסת ויציאת השבת</h2>
            <div class="shabbat-times">
                <div>
                    <h3>🕯️ כניסת השבת</h3>
                    <strong id="shabbat-in">טוען...</strong>
                </div>
                <div>
                    <h3>⭐ יציאת השבת</h3>
                    <strong id="shabbat-out">טוען...</strong>
                </div>
            </div>
        </div>

        <div class="info-box week-times">
            <h2>זמני השבוע הבא (ימות החול)</h2>
            <table>
                <thead>
                    <tr>
                        <th>היום</th>
                        <th>שקיעה</th>
                        <th>צאת הכוכבים</th>
                    </tr>
                </thead>
                <tbody id="week-days">
                    </tbody>
            </table>
        </div>
    </div>
    
    <footer>
        <p>הנתונים מסופקים באדיבות Hebcal API</p>
    </footer>

<script>
document.addEventListener('DOMContentLoaded', function() {
    // קביעת התאריכים הרלוונטיים
    const today = new Date();
    const year = today.getFullYear();
    const month = today.getMonth() + 1;

    // הגדרות עבור גבעת שמואל
    const geonameid = '294862'; // ID גיאוגרפי של גבעת שמואל
    const hebcalUrl = `https://www.hebcal.com/hebcal?v=1&cfg=json&maj=on&min=on&mod=on&nx=on&year=${year}&month=${month}&ss=on&geo=geoname&geonameid=${geonameid}&m=50&s=on`;

    // פונקציה להמרת תאריך לפורמט קריא
    function formatTime(dateString) {
        if (!dateString) return 'לא זמין';
        const date = new Date(dateString);
        return date.toLocaleTimeString('he-IL', {
            hour: '2-digit',
            minute: '2-digit',
            hour12: false
        });
    }

    // פונקציה להמרת תאריך עברי
    function getHebrewDayName(dateString) {
        const date = new Date(dateString);
        const dayIndex = date.getDay();
        const days = ['ראשון', 'שני', 'שלישי', 'רביעי', 'חמישי', 'שישי', 'שבת'];
        return days[dayIndex];
    }
    
    // שליפת הנתונים מהשרת
    fetch(hebcalUrl)
        .then(response => {
            if (!response.ok) {
                throw new Error('Network response was not ok');
            }
            return response.json();
        })
        .then(data => {
            const items = data.items;

            // מציאת פרשת השבוע הקרובה
            const parashaItem = items.find(item => 
                item.category === 'parashat' && new Date(item.date) >= today
            );
            if (parashaItem) {
                document.getElementById('parasha').textContent = parashaItem.hebrew;
            } else {
                document.getElementById('parasha').textContent = 'לא נמצאה פרשה';
            }

            // מציאת זמני השבת הקרובה
            const candleLighting = items.find(item => 
                item.category === 'candles' && new Date(item.date) >= today
            );
            const havdalah = items.find(item => 
                item.category === 'havdalah' && new Date(item.date) >= today
            );

            if (candleLighting) {
                document.getElementById('shabbat-in').textContent = formatTime(candleLighting.date);
            } else {
                 document.getElementById('shabbat-in').textContent = 'לא זמין';
            }
            if (havdalah) {
                document.getElementById('shabbat-out').textContent = formatTime(havdalah.date);
            } else {
                 document.getElementById('shabbat-out').textContent = 'לא זמין';
            }

            // מציאת זמני השקיעה וצאת הכוכבים לשבוע הבא
            const weekDaysTable = document.getElementById('week-days');
            let daysCount = 0;
            
            const sunsetItems = items.filter(item => item.category === 'sunset');
            const tzeitItems = items.filter(item => item.category === 'tzeit');

            for (let i = 0; i < sunsetItems.length && daysCount < 5; i++) {
                const sunset = sunsetItems[i];
                const itemDate = new Date(sunset.date);
                const dayOfWeek = itemDate.getDay(); // 0=Sunday, 6=Saturday

                if (candleLighting && itemDate <= new Date(candleLighting.date)) {
                    continue;
                }
                
                if (dayOfWeek >= 0 && dayOfWeek <= 4) {
                    const tzeit = tzeitItems.find(t => t.date.startsWith(sunset.date.substring(0, 10)));
                    
                    const row = document.createElement('tr');
                    row.innerHTML = `
                        <td>${getHebrewDayName(sunset.date)}</td>
                        <td>${formatTime(sunset.date)}</td>
                        <td>${tzeit ? formatTime(tzeit.date) : 'לא זמין'}</td>
                    `;
                    weekDaysTable.appendChild(row);
                    daysCount++;
                }
            }
            
            document.getElementById('loader').style.display = 'none';
            document.getElementById('content').style.display = 'block';

        })
        .catch(error => {
            console.error('Error fetching data:', error);
            document.getElementById('loader').textContent = 'שגיאה בטעינת הנתונים. אנא נסה לרענן את הדף.';
        });
});
</script>

</body>
</html>
