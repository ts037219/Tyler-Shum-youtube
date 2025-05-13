<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>My YouTube Channel</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            background-color: #f4f4f4;
            padding: 20px;
        }
        .container {
            max-width: 900px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        h1 {
            color: #ff0000;
        }
        a {
            text-decoration: none;
            color: #0073e6;
            font-size: 18px;
        }
        .video-grid {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 10px;
            margin-top: 20px;
        }
        .video-grid iframe {
            width: 100%;
            height: 200px;
            border: none;
        }
        .pagination {
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 20px 0;
        }
        .page-btn {
            background-color: #0073e6;
            color: white;
            border: none;
            padding: 10px 15px;
            margin: 5px;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
        }
        .page-btn.active {
            background-color: #ff0000;
        }
        .channel-list {
            display: flex;
            flex-direction: column;
            align-items: center;
            gap: 15px;
            margin-top: 20px;
        }
        .channel-item {
            display: flex;
            align-items: center;
            background: #fff;
            padding: 15px;
            border-radius: 10px;
            box-shadow: 0 0 5px rgba(0, 0, 0, 0.1);
            width: 80%;
        }
        .channel-item img {
            width: 50px;
            height: 50px;
            border-radius: 50%;
            margin-right: 15px;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Welcome to My YouTube Channel!</h1>
        <p>Check out my most popular videos below and subscribe for more content.</p>

        <div class="video-grid" id="videoContainer">
            <!-- Videos will be dynamically inserted here -->
        </div>

        <div class="channel-list" id="channelContainer" style="display: none;">
            <!-- Channels will be dynamically inserted here -->
        </div>

        <!-- Page Indicator -->
        <div class="pagination">
            <button class="page-btn" onclick="changePage(1)">Page 1</button>
            <button class="page-btn" onclick="changePage(2)">Page 2</button>
            <button class="page-btn" onclick="changePage(3)">Page 3</button>
            <button class="page-btn" onclick="changePage(4)">Page 4</button>
            <button class="page-btn" onclick="changePage(5)">Channels</button>
        </div>

        <p>Visit my channel for more videos:</p>
        <a href="CHANNEL_LINK" target="_blank">Go to My YouTube Channel</a>
    </div>

    <script>
        const videoSets = {
            1: ["VIDEO_ID_1", "VIDEO_ID_2", "VIDEO_ID_3", "VIDEO_ID_4", "VIDEO_ID_5"],
            2: ["VIDEO_ID_6", "VIDEO_ID_7", "VIDEO_ID_8", "VIDEO_ID_9", "VIDEO_ID_10"],
            3: ["VIDEO_ID_11", "VIDEO_ID_12", "VIDEO_ID_13", "VIDEO_ID_14", "VIDEO_ID_15"],
            4: ["VIDEO_ID_16", "VIDEO_ID_17", "VIDEO_ID_18", "VIDEO_ID_19", "VIDEO_ID_20"]
        };

        const channels = [
            { name: "Channel 1", link: "https://www.youtube.com/@Channel1", icon: "https://via.placeholder.com/50" },
            { name: "Channel 2", link: "https://www.youtube.com/@Channel2", icon: "https://via.placeholder.com/50" },
            { name: "Channel 3", link: "https://www.youtube.com/@Channel3", icon: "https://via.placeholder.com/50" },
            { name: "Channel 4", link: "https://www.youtube.com/@Channel4", icon: "https://via.placeholder.com/50" },
            { name: "Channel 5", link: "https://www.youtube.com/@Channel5", icon: "https://via.placeholder.com/50" }
        ];

        function changePage(page) {
            const videoContainer = document.getElementById("videoContainer");
            const channelContainer = document.getElementById("channelContainer");

            if (page === 5) {
                videoContainer.style.display = "none";
                channelContainer.style.display = "flex";
                channelContainer.innerHTML = ""; // Clear previous channels

                channels.forEach(channel => {
                    const div = document.createElement("div");
                    div.classList.add("channel-item");
                    div.innerHTML = `<img src="${channel.icon}" alt="${channel.name}"><a href="${channel.link}" target="_blank">${channel.name}</a>`;
                    channelContainer.appendChild(div);
                });
            } else {
                videoContainer.style.display = "grid";
                channelContainer.style.display = "none";
                videoContainer.innerHTML = ""; // Clear previous videos

                videoSets[page].forEach(videoId => {
                    const iframe = document.createElement("iframe");
                    iframe.src = `https://www.youtube.com/embed/${videoId}`;
                    iframe.allowFullscreen = true;
                    videoContainer.appendChild(iframe);
                });
            }

            document.querySelectorAll(".page-btn").forEach(btn => btn.classList.remove("active"));
            document.querySelectorAll(".page-btn")[page - 1].classList.add("active");
        }

        // Load first page by default
        changePage(1);
    </script>

</body>
</html>
