<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>AchieversHub</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      text-align: center;
      background: #f5f5f5;
      margin: 0;
      padding: 20px;
    }
    h1 {
      color: #2c3e50;
    }
    .button-container {
      margin: 20px;
    }
    button {
      margin: 10px;
      padding: 15px 25px;
      font-size: 16px;
      cursor: pointer;
      border: none;
      border-radius: 5px;
      background-color: #3498db;
      color: white;
    }
    button:hover {
      background-color: #2980b9;
    }
    .tips {
      margin-top: 30px;
      padding: 20px;
      background: #fff;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
      display: none;
      text-align: left;
    }
  </style>
</head>
<body>
  <h1>Welcome to AchieversHub</h1>
  <p>Select a subject to see revision tips:</p>

  <div class="button-container">
    <button onclick="showTips('math')">Math</button>
    <button onclick="showTips('science')">Science</button>
    <button onclick="showTips('english')">English</button>
    <button onclick="showTips('history')">History</button>
    <button onclick="showTips('social')">Social Studies</button>
    <button onclick="showTips('geography')">Geography</button>
    <button onclick="showTips('computers')">Computer Science</button>
  </div>

  <div id="tips" class="tips"></div>

  <script>
    function showTips(subject) {
      let tipsText = "";
      switch(subject) {
        case 'math':
          tipsText = `
            <h2>Math Revision Tips</h2>
            <ul>
              <li>Practice problems daily to build speed and accuracy.</li>
              <li>Review formulas and theorems regularly.</li>
              <li>Break complex problems into smaller steps.</li>
              <li>Use past exam papers to test yourself under timed conditions.</li>
              <li>Create a formula sheet for quick reference.</li>
              <li>Explain solutions aloud — teaching reinforces learning.</li>
            </ul>`;
          break;
        case 'science':
          tipsText = `
            <h2>Science Revision Tips</h2>
            <ul>
              <li>Summarize each chapter in your own words.</li>
              <li>Use diagrams and flowcharts to understand processes.</li>
              <li>Revise definitions and key terms with flashcards.</li>
              <li>Link concepts to real-life examples for better memory.</li>
              <li>Practice labeling diagrams and writing short notes.</li>
              <li>Group topics (physics, chemistry, biology) and rotate revision.</li>
            </ul>`;
          break;
        case 'english':
          tipsText = `
            <h2>English Revision Tips</h2>
            <ul>
              <li>Read sample essays and analyze structure.</li>
              <li>Practice grammar exercises daily.</li>
              <li>Expand vocabulary with daily reading and word lists.</li>
              <li>Summarize stories or poems in your own words.</li>
              <li>Practice comprehension by answering questions on passages.</li>
              <li>Write short essays and get feedback to improve style.</li>
            </ul>`;
          break;
        case 'history':
          tipsText = `
            <h2>History Revision Tips</h2>
            <ul>
              <li>Create timelines of events to visualize chronology.</li>
              <li>Use flashcards for dates, names, and key terms.</li>
              <li>Understand causes and consequences, not just facts.</li>
              <li>Compare different historical periods to spot patterns.</li>
              <li>Practice writing structured answers with introduction, body, and conclusion.</li>
              <li>Revise maps and geography linked to historical events.</li>
            </ul>`;
          break;
        case 'social':
          tipsText = `
            <h2>Social Studies Revision Tips</h2>
            <ul>
              <li>Break down topics into civics, economics, and culture.</li>
              <li>Use case studies to understand concepts.</li>
              <li>Practice writing short notes on key ideas.</li>
              <li>Revise important laws, rights, and responsibilities.</li>
              <li>Discuss topics with peers to gain perspective.</li>
              <li>Use charts and diagrams for social structures.</li>
            </ul>`;
          break;
        case 'geography':
          tipsText = `
            <h2>Geography Revision Tips</h2>
            <ul>
              <li>Memorize maps and practice labeling countries, rivers, and mountains.</li>
              <li>Understand physical processes like erosion, volcanoes, and climate.</li>
              <li>Revise case studies of regions and their features.</li>
              <li>Use diagrams and flowcharts for processes.</li>
              <li>Practice interpreting graphs and data tables.</li>
              <li>Link geography to current events for relevance.</li>
            </ul>`;
          break;
        case 'computers':
          tipsText = `
            <h2>Computer Science Revision Tips</h2>
            <ul>
              <li>Revise programming concepts with small code snippets.</li>
              <li>Understand algorithms and practice writing pseudocode.</li>
              <li>Review data structures like arrays, lists, and trees.</li>
              <li>Summarize theory topics (hardware, software, networks).</li>
              <li>Practice debugging exercises to sharpen skills.</li>
              <li>Use online coding platforms for practice challenges.</li>
            </ul>`;
          break;
      }
      document.getElementById("tips").innerHTML = tipsText;
      document.getElementById("tips").style.display = "block";
    }
  </script>
</body>
</html>
