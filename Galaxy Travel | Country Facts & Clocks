<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>🌍 Galaxy Travel | Country Facts & Clocks</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
      color: #fff;
      padding: 0 20px;
    }

    header {
      text-align: center;
      padding: 40px 20px;
      background: rgba(0, 0, 0, 0.6);
      border-bottom: 2px solid #00ffff44;
      backdrop-filter: blur(5px);
    }

    header h1 {
      font-size: 2.5rem;
      color: #00ffff;
      text-shadow: 0 0 10px #00ffffaa;
    }

    .country-section {
      margin: 40px auto;
      max-width: 800px;
      background: rgba(255, 255, 255, 0.05);
      border: 1px solid #00ffff33;
      border-radius: 12px;
      padding: 20px;
      box-shadow: 0 0 20px #00ffff22;
      overflow: hidden;
    }

    .country-section img {
      width: 100%;
      max-height: 250px;
      object-fit: cover;
      border-radius: 10px;
      margin-bottom: 15px;
    }

    .country-section h2 {
      color: #00ffff;
      text-shadow: 0 0 5px #00ffff88;
      margin-bottom: 10px;
    }

    .clock {
      font-size: 1.2rem;
      color: #00ff99;
      margin-bottom: 10px;
    }

    .facts {
      list-style: square;
      padding-left: 20px;
    }

    .facts li {
      margin-bottom: 8px;
      line-height: 1.6;
    }

    @media (max-width: 600px) {
      header h1 {
        font-size: 1.5rem;
      }

      .country-section {
        padding: 15px;
      }

      .clock {
        font-size: 1rem;
      }
    }
  </style>
</head>
<body>
  <header>
    <h1>🌍 Galaxy Travel: Fun Facts & Real-Time Clocks</h1>
  </header>

  <div id="countries-container"></div>

  <script>
    const countriesData = [
      {
        name: "🇦🇺 Australia",
        timezone: "Australia/Sydney",
        image: "https://images.unsplash.com/photo-1506976785307-8732e854ad81?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to the Great Barrier Reef, the world's largest coral system.",
          "Contains more kangaroos than people.",
          "Uluru changes color at different times of the day.",
          "Sydney Opera House has over 1 million tiles on its roof.",
          "Australia is the driest inhabited continent."
        ]
      },
      {
        name: "🇲🇽 Mexico",
        timezone: "America/Mexico_City",
        image: "https://images.unsplash.com/photo-1526404428533-4d94a00a44d3?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to 35 UNESCO World Heritage Sites.",
          "Chocolate was first used by ancient Mexicans.",
          "Mexico City sinks about 10 inches every year.",
          "Day of the Dead is a vibrant national holiday.",
          "World’s largest pyramid (by volume) is in Mexico."
        ]
      },
      {
        name: "🇧🇷 Brazil",
        timezone: "America/Sao_Paulo",
        image: "https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "60% of the Amazon rainforest is in Brazil.",
          "Carnival in Rio is the world’s largest festival.",
          "Brazil has more species of primates than any other nation.",
          "Home to Christ the Redeemer, one of the New Seven Wonders.",
          "Portuguese is the official language."
        ]
      },
      {
        name: "🇮🇳 India",
        timezone: "Asia/Kolkata",
        image: "https://images.unsplash.com/photo-1599507593362-72e04f0be3b5?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "India has over 22 official languages.",
          "The concept of zero originated here.",
          "Home to the world's largest democracy.",
          "Houses the world’s highest cricket ground (Chail, Himachal Pradesh).",
          "Hosts the Kumbh Mela, visible from space!"
        ]
      },
      {
        name: "🇺🇸 United States",
        timezone: "America/New_York",
        image: "https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Has 63 national parks covering over 84 million acres.",
          "The US flag has been changed 27 times.",
          "NASA put a man on the moon in 1969.",
          "Known for its cultural exports: film, music, and tech.",
          "Route 66 was the first national highway."
        ]
      },
      {
        name: "🇫🇷 France",
        timezone: "Europe/Paris",
        image: "https://images.unsplash.com/photo-1502602898657-3e91760cbb34?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "The Eiffel Tower was built in 1889 for the World's Fair.",
          "France is the most visited country in the world.",
          "The Louvre is the largest art museum globally.",
          "French fries are actually from Belgium.",
          "The French consume 25,000 tons of snails yearly."
        ]
      },
      {
        name: "🇯🇵 Japan",
        timezone: "Asia/Tokyo",
        image: "https://images.unsplash.com/photo-1554797589-7241bb691973?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Japan has more than 6,800 islands.",
          "Tokyo is the most populous metropolitan area in the world.",
          "Home of Mount Fuji, an active volcano.",
          "Has the world’s oldest company (founded in 578 AD).",
          "Known for its cherry blossoms (sakura)."
        ]
      },
      {
        name: "🇨🇦 Canada",
        timezone: "America/Toronto",
        image: "https://images.unsplash.com/photo-1508264165352-258859e62245?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Canada has the longest coastline in the world.",
          "Has more lakes than the rest of the world combined.",
          "Niagara Falls is on the US-Canada border.",
          "The maple leaf is its national symbol.",
          "Canada is the second largest country by land area."
        ]
      },
      {
        name: "🇪🇬 Egypt",
        timezone: "Africa/Cairo",
        image: "https://images.unsplash.com/photo-1587397398251-04b8f92c37df?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to the Great Pyramid of Giza, the last of the ancient wonders.",
          "The Nile is the longest river in the world.",
          "Ancient Egyptians invented papyrus.",
          "Cleopatra VII was the last active pharaoh.",
          "Egypt has more than 100 pyramids."
        ]
      },
      {
        name: "🇮🇹 Italy",
        timezone: "Europe/Rome",
        image: "https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Rome has a country inside it: Vatican City.",
          "Italy is home to more UNESCO sites than any other country.",
          "Pizza was invented in Naples in the 18th century.",
          "The Leaning Tower of Pisa took 200 years to complete.",
          "Venice has over 150 canals."
        ]
      },
      {
        name: "🇨🇳 China",
        timezone: "Asia/Shanghai",
        image: "https://images.unsplash.com/photo-1524492449090-1a065f2dd417?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "The Great Wall of China is over 13,000 miles long.",
          "China has the world’s largest population.",
          "Paper, gunpowder, and compass were invented here.",
          "Pandas are native to China.",
          "Chinese New Year is the world’s biggest annual celebration."
        ]
      },
      {
        name: "🇬🇧 United Kingdom",
        timezone: "Europe/London",
        image: "https://images.unsplash.com/photo-1528909514045-2fa4ac7a08ba?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "London has the oldest underground railway in the world.",
          "Stonehenge is over 5,000 years old.",
          "The UK has produced famous writers like Shakespeare and Rowling.",
          "Big Ben is actually the bell, not the tower.",
          "Tea is the most popular drink."
        ]
      },
      {
        name: "🇩🇪 Germany",
        timezone: "Europe/Berlin",
        image: "https://images.unsplash.com/photo-1526481280691-3e4a5c8c8f2c?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Germany is home to the Autobahn, with stretches of no speed limit.",
          "Oktoberfest in Munich is the world’s largest beer festival.",
          "Berlin has more bridges than Venice.",
          "Germany is Europe’s largest economy.",
          "The printing press was invented by Johannes Gutenberg."
        ]
      },
      {
        name: "🇿🇦 South Africa",
        timezone: "Africa/Johannesburg",
        image: "https://images.unsplash.com/photo-1517686469429-8bdb88b9f7c7?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to Table Mountain in Cape Town.",
          "Has three capital cities: Pretoria, Cape Town, and Bloemfontein.",
          "Nelson Mandela was its first black president.",
          "Kruger National Park is one of Africa’s largest game reserves.",
          "Hosts the richest gold resources in the world."
        ]
      },
      {
        name: "🇷🇺 Russia",
        timezone: "Europe/Moscow",
        image: "https://images.unsplash.com/photo-1583229216467-9c893475c2c4?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Largest country in the world by land area.",
          "Trans-Siberian Railway is the world’s longest railway.",
          "Lake Baikal holds 20% of the world's fresh water.",
          "Moscow’s Kremlin is the world’s largest medieval fortress.",
          "Home to Siberian tigers and brown bears."
        ]
      },
      {
        name: "🇪🇸 Spain",
        timezone: "Europe/Madrid",
        image: "https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Spain produces more olive oil than any other country.",
          "The Sagrada Família in Barcelona is still unfinished after 140+ years.",
          "Flamenco originated in Andalusia.",
          "Spain has 48 UNESCO World Heritage Sites.",
          "La Tomatina is the world’s biggest food fight."
        ]
      },
      {
        name: "🇹🇷 Turkey",
        timezone: "Europe/Istanbul",
        image: "https://images.unsplash.com/photo-1549899595-9a8d3fba5e4a?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Istanbul is the only city in the world on two continents.",
          "Santa Claus was born in Turkey.",
          "The Grand Bazaar is one of the oldest markets in the world.",
          "Cappadocia is famous for its fairy chimneys.",
          "Home to Troy, the city of Homer’s Iliad."
        ]
      },
      {
        name: "🇦🇷 Argentina",
        timezone: "America/Argentina/Buenos_Aires",
        image: "https://images.unsplash.com/photo-1546539782-f7f4e727ab06?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home of tango dance.",
          "Iguazu Falls is one of the largest waterfalls systems in the world.",
          "Argentina is the 8th largest country by area.",
          "Famous for Patagonia and Andes mountains.",
          "Football legend Diego Maradona was born here."
        ]
      },
      {
        name: "🇹🇭 Thailand",
        timezone: "Asia/Bangkok",
        image: "https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Thailand has never been colonized by a European power.",
          "Bangkok’s full ceremonial name is 169 characters long.",
          "Known as the 'Land of Smiles'.",
          "Home to the world’s largest gold Buddha.",
          "Songkran Festival is the world’s biggest water fight."
        ]
      },
      {
        name: "🇬🇷 Greece",
        timezone: "Europe/Athens",
        image: "https://images.unsplash.com/photo-1549887534-3db1bdbe2840?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Athens is one of the oldest cities in the world.",
          "The Olympic Games originated in Greece in 776 BC.",
          "Has thousands of islands, but only 200 are inhabited.",
          "Greek is the oldest written language still in use.",
          "Feta cheese originates from Greece."
        ]
      },
      {
        name: "🇸🇦 Saudi Arabia",
        timezone: "Asia/Riyadh",
        image: "https://images.unsplash.com/photo-1583324113626-70df0f4deaab?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to Islam’s two holiest cities: Mecca and Medina.",
          "The Rub’ al Khali is the world’s largest sand desert.",
          "Oil was discovered in 1938 and transformed the country.",
          "The Kingdom has no rivers.",
          "Camel racing is a national sport."
        ]
      },
      {
        name: "🇰🇷 South Korea",
        timezone: "Asia/Seoul",
        image: "https://images.unsplash.com/photo-1526481280691-3e4a5c8c8f2c?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "K-pop is a global phenomenon originating here.",
          "Seoul is one of the world’s most high-tech cities.",
          "Taekwondo is a Korean martial art.",
          "Has the fastest average internet speed globally.",
          "Kimchi is eaten at almost every meal."
        ]
      },
      {
        name: "🇵🇹 Portugal",
        timezone: "Europe/Lisbon",
        image: "https://images.unsplash.com/photo-1524492449090-1a065f2dd417?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Lisbon is older than Rome.",
          "Portugal is the world’s largest cork producer.",
          "The world’s oldest bookstore is in Lisbon (1732).",
          "Portuguese is spoken in 9 countries.",
          "Fado is Portugal’s traditional music style."
        ]
      },
      {
        name: "🇳🇱 Netherlands",
        timezone: "Europe/Amsterdam",
        image: "https://images.unsplash.com/photo-1505761671935-60b3a7427bad?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Amsterdam has more bikes than residents.",
          "The Netherlands is famous for tulips and windmills.",
          "Most of the country lies below sea level.",
          "Dutch people are the tallest in the world on average.",
          "Has over 1,200 historic windmills."
        ]
      },
      {
        name: "🇸🇪 Sweden",
        timezone: "Europe/Stockholm",
        image: "https://images.unsplash.com/photo-1549887534-3db1bdbe2840?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Sweden has more than 100,000 lakes.",
          "IKEA was founded here in 1943.",
          "The Nobel Prizes are awarded in Stockholm.",
          "Midnight Sun occurs in the north during summer.",
          "Fika (coffee break) is a daily tradition."
        ]
      },
      {
        name: "🇨🇭 Switzerland",
        timezone: "Europe/Zurich",
        image: "https://images.unsplash.com/photo-1508264165352-258859e62245?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to the Swiss Alps.",
          "Famous for cheese and chocolate.",
          "Has four national languages.",
          "Switzerland has not been in a war since 1815.",
          "Red Cross was founded in Geneva."
        ]
      },
      {
        name: "🇳🇵 Nepal",
        timezone: "Asia/Kathmandu",
        image: "https://images.unsplash.com/photo-1554797589-7241bb691973?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Home to Mount Everest, the world’s tallest peak.",
          "Nepal’s flag is not rectangular, it’s two triangles.",
          "Birthplace of Buddha (Lumbini).",
          "Has 8 of the world’s 14 highest mountains.",
          "Kathmandu is called the ‘City of Temples’."
        ]
      },
      {
        name: "🇮🇩 Indonesia",
        timezone: "Asia/Jakarta",
        image: "https://images.unsplash.com/photo-1506748686214-e9df14d4d9d0?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Indonesia has over 17,000 islands.",
          "World’s largest Muslim-majority nation.",
          "Komodo dragons are native here.",
          "Bali is a world-famous tourist island.",
          "The country sits on the Ring of Fire."
        ]
      },
      {
        name: "🇳🇿 New Zealand",
        timezone: "Pacific/Auckland",
        image: "https://images.unsplash.com/photo-1546539782-f7f4e727ab06?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "First country to grant women the right to vote.",
          "Lord of the Rings was filmed here.",
          "Has more sheep than people.",
          "Home to the flightless kiwi bird.",
          "Rugby is the national sport."
        ]
      },
      {
        name: "🇰🇪 Kenya",
        timezone: "Africa/Nairobi",
        image: "https://images.unsplash.com/photo-1517686469429-8bdb88b9f7c7?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Kenya is famous for its safaris.",
          "The Great Rift Valley runs through the country.",
          "Nairobi is known as the ‘Green City in the Sun’.",
          "Athletes dominate long-distance running.",
          "Mount Kenya is the second-highest peak in Africa."
        ]
      },
      {
        name: "🇦🇪 UAE",
        timezone: "Asia/Dubai",
        image: "https://images.unsplash.com/photo-1549899595-9a8d3fba5e4a?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Dubai is home to Burj Khalifa, the tallest building in the world.",
          "Oil was discovered in the UAE in the 1950s.",
          "Home to man-made islands like Palm Jumeirah.",
          "Abu Dhabi is the capital, not Dubai.",
          "UAE hosts one of the world’s busiest airports."
        ]
      },
      {
        name: "🇵🇪 Peru",
        timezone: "America/Lima",
        image: "https://images.unsplash.com/photo-1526404428533-4d94a00a44d3?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Machu Picchu is one of the New Seven Wonders.",
          "Ceviche is a traditional Peruvian dish.",
          "The Amazon River starts in Peru.",
          "Peru has over 3,000 types of potatoes.",
          "The Nazca Lines are mysterious geoglyphs."
        ]
      },
      {
        name: "🇨🇱 Chile",
        timezone: "America/Santiago",
        image: "https://images.unsplash.com/photo-1524492449090-1a065f2dd417?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Chile is the world’s longest country north to south.",
          "The Atacama Desert is the driest place on Earth.",
          "Easter Island belongs to Chile.",
          "Chile has more than 2,000 volcanoes.",
          "Wine is one of its biggest exports."
        ]
      },
      {
        name: "🇨🇴 Colombia",
        timezone: "America/Bogota",
        image: "https://images.unsplash.com/photo-1554797589-7241bb691973?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Colombia produces some of the world’s best coffee.",
          "Bogotá is one of the highest capitals (2,640 m).",
          "Shakira and Gabriel García Márquez are from here.",
          "Has both Pacific and Caribbean coastlines.",
          "Known for colorful Carnival in Barranquilla."
        ]
      },
      {
        name: "🇳🇬 Nigeria",
        timezone: "Africa/Lagos",
        image: "https://images.unsplash.com/photo-1583229216467-9c893475c2c4?auto=format&fit=crop&w=1200&q=80",
        facts: [
          "Most populous country in Africa.",
          "Nollywood is the 2nd largest film industry by volume.",
          "Lagos is Africa’s largest city.",
          "Nigeria has over 500 languages.",
          "Known for Afrobeat music."
        ]
      }
    ];

    function updateClocks() {
      const now = new Date();
      countriesData.forEach(country => {
        const el = document.getElementById("clock-" + country.name.replace(/[^a-zA-Z]/g, ""));
        if (el) {
          const options = {
            timeZone: country.timezone,
            hour: '2-digit',
            minute: '2-digit',
            second: '2-digit',
            hour12: false
          };
          const timeStr = now.toLocaleTimeString('en-US', options);
          el.textContent = "🕒 " + timeStr;
        }
      });
    }

    function renderCountries() {
      const container = document.getElementById("countries-container");
      countriesData.forEach(country => {
        const section = document.createElement("div");
        section.className = "country-section";

        const img = document.createElement("img");
        img.src = country.image;
        img.alt = country.name + " image";
        section.appendChild(img);

        const h2 = document.createElement("h2");
        h2.textContent = country.name;
        section.appendChild(h2);

        const clock = document.createElement("div");
        clock.className = "clock";
        clock.id = "clock-" + country.name.replace(/[^a-zA-Z]/g, "");
        clock.textContent = "Loading time...";
        section.appendChild(clock);

        const ul = document.createElement("ul");
        ul.className = "facts";
        country.facts.forEach(fact => {
          const li = document.createElement("li");
          li.textContent = fact;
          ul.appendChild(li);
        });
        section.appendChild(ul);

        container.appendChild(section);
      });
    }

    renderCountries();
    updateClocks();
    setInterval(updateClocks, 1000);
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>World Clocks</title>
  <style>
    body {
      background: black;
      color: white;
      font-family: 'Arial', sans-serif;
      padding: 20px;
    }

    h1 {
      color: #00ffff;
      text-align: center;
    }

    .clock {
      background: rgba(0, 255, 255, 0.05);
      border: 1px solid #00ffff55;
      border-radius: 8px;
      padding: 10px 20px;
      margin: 10px auto;
      max-width: 400px;
      font-size: 1.2rem;
    }
  </style>
</head>
<body>

<h1>🌍 Real-Time World Clocks</h1>

<div id="clocks-container">
  <!-- JavaScript will generate clocks here -->
</div>

<script>
  const timezones = {
    "Australia": "Australia/Sydney",
    "Mexico": "America/Mexico_City",
    "Brazil": "America/Sao_Paulo",
    "United States": "America/New_York",
    "China": "Asia/Shanghai",
    "India": "Asia/Kolkata",
    "Canada": "America/Toronto",
    "Indonesia": "Asia/Jakarta",
    "France": "Europe/Paris",
    "Colombia": "America/Bogota",
    "Spain": "Europe/Madrid",
    "Japan": "Asia/Tokyo",
    "South Africa": "Africa/Johannesburg",
    "Thailand": "Asia/Bangkok",
    "Italy": "Europe/Rome",
    "Tanzania": "Africa/Dar_es_Salaam",
    "Peru": "America/Lima",
    "Argentina": "America/Argentina/Buenos_Aires",
    "Venezuela": "America/Caracas",
    "Ecuador": "America/Guayaquil",
    "Malaysia": "Asia/Kuala_Lumpur",
    "Philippines": "Asia/Manila",
    "Costa Rica": "America/Costa_Rica",
    "Vietnam": "Asia/Ho_Chi_Minh",
    "Panama": "America/Panama",
    "Kenya": "Africa/Nairobi",
    "New Zealand": "Pacific/Auckland",
    "Bolivia": "America/La_Paz",
    "United Kingdom": "Europe/London",
    "Croatia": "Europe/Zagreb",
    "Iceland": "Atlantic/Reykjavik",
    "Portugal": "Europe/Lisbon",
    "Chile": "America/Santiago",
    "Namibia": "Africa/Windhoek",
    "Greece": "Europe/Athens",
    "Sri Lanka": "Asia/Colombo",
    "Norway": "Europe/Oslo",
    "Turkey": "Europe/Istanbul",
    "Nepal": "Asia/Kathmandu",
    "Switzerland": "Europe/Zurich"
  };

  const container = document.getElementById('clocks-container');

  for (const country in timezones) {
    const div = document.createElement('div');
    div.className = 'clock';
    div.id = `clock-${country.replace(/ /g, "_")}`;
    div.textContent = `${country}: Loading...`;
    container.appendChild(div);
  }

  function updateClocks() {
    const now = new Date();
    for (const [country, tz] of Object.entries(timezones)) {
      const options = {
        timeZone: tz,
        hour: '2-digit',
        minute: '2-digit',
        second: '2-digit',
        hour12: false
      };
      const localTime = now.toLocaleTimeString('en-US', options);
      const el = document.getElementById(`clock-${country.replace(/ /g, "_")}`);
      if (el) {
        el.textContent = `${country}: ${localTime}`;
      }
    }
  }
  document.getElementById("search-bar").addEventListener("input", (e) => {
      const searchValue = e.target.value.toLowerCase();
      const sections = document.querySelectorAll(".country-section");
  }).
      countriesData.forEach((country, index) => {
        const matches = country.name.toLowerCase().includes(searchValue);
        sections[index].style.display = matches ? "block" : "none";
        });

  updateClocks();
  setInterval(updateClocks, 1000);
</script>

</body>
</html>
