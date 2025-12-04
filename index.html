<!DOCTYPE html>
<html lang="ja">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>サンタさんのチャットアシスタント</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        // 薄い、優しい赤を維持
                        'santa-red': '#E57373', // Light, Gentle Red
                        'santa-green': '#064e3b', // Deep Forest Green (背景色に使用)
                        'snow-white': '#F9FAFB', 
                        'star-gold': '#FBBF24', 
                    },
                    fontFamily: {
                        sans: ['Inter', 'sans-serif'],
                    },
                }
            }
        }
    </script>
    <style>
        /* =================================
           1. 全体の背景 - クリスマスグリーンに固定
           ================================= */
        body {
            /* 落ち着いたクリスマスグリーンに固定 */
            background-color: #064e3b; 
            overflow: hidden; 
            position: relative;
        }

        /* =================================
           2. 雪マーク (❄️) アニメーション
           ================================= */
        .snow-container {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
            z-index: 10;
        }

        /* 雪を降らせるための基本スタイル */
        .snowflake {
            color: #ffffff; 
            text-shadow: 0 0 3px rgba(255, 255, 255, 0.5); 
            font-size: 1.5rem; 
            position: absolute;
            top: -10vh; 
            animation: fall linear infinite;
        }

        /* 雪マークのアニメーション */
        @keyframes fall {
            0% { transform: translateY(0) rotate(0deg); opacity: 0; }
            10% { opacity: 0.8; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0.4; }
        }

        /* =================================
           3. その他デザイン調整
           ================================= */
        /* カスタムスクロールバー */
        #chat-messages::-webkit-scrollbar {
            width: 8px;
        }

        #chat-messages::-webkit-scrollbar-thumb {
            background-color: rgba(229, 115, 115, 0.7); /* 薄い赤のスクロールバー */
            border-radius: 10px;
        }

        #chat-messages::-webkit-scrollbar-track {
            background: rgba(4, 120, 87, 0.1);
        }

        /* アシスタントメッセージの背景はコントラストを維持するため濃いグリーンを使用 */
        .bot-bubble {
            background-color: #047857; /* 濃い目のフォレストグリーン */
        }
    </style>
</head>

<body class="min-h-screen flex items-center justify-center p-4">

    <!-- 雪の結晶を生成するコンテナ -->
    <div class="snow-container" id="snow-container"></div>

    <!-- Chat Bot Container (標準サイズ max-w-2xl) -->
    <div class="w-full max-w-2xl bg-snow-white rounded-xl shadow-2xl overflow-hidden backdrop-blur-sm bg-opacity-95 border-4 border-santa-red z-20" style="min-height: 85vh;">

        <!-- Header (薄い赤) -->
        <div class="bg-santa-red text-white py-6 px-4 flex items-center justify-center rounded-t-lg border-b-2 border-star-gold">
            <span class="text-3xl mr-3 animate-pulse" role="img" aria-label="Star Icon">⭐</span>
            <h1 class="text-3xl font-extrabold tracking-widest drop-shadow-md">サンタさんの秘密チャット</h1>
            <span class="text-3xl ml-3 animate-pulse" role="img" aria-label="Star Icon">⭐</span>
        </div>

        <!-- Chat Messages Area (高さを h-[60vh] に調整) -->
        <div id="chat-messages" class="h-[60vh] p-6 space-y-4 overflow-scroll">
            <!-- Initial Bot Message -->
            <div class="flex justify-start">
                <div class="max-w-md bot-bubble text-white p-4 rounded-t-2xl rounded-br-2xl shadow-lg border-b border-star-gold">
                    <p class="font-bold text-lg flex items-center">
                        <!-- アイコンをトナカイ (🦌) に戻しました -->
                        <span class="mr-2 text-2xl" role="img" aria-label="Elf Icon">🦌</span>
                        <!-- 挨拶は「クリスマス特化型検索AIにようこそ！」を維持 -->
                        クリスマス特化型検索AIにようこそ！
                    </p>
                    <p class="mt-2 text-sm">私は、サンタさんの移動やクリスマスの魔法に関する情報を検索・提供します。</p>
                    <p class="mt-1 text-sm font-light">フライトレーダーやNORADなど、サンタさんの移動やプレゼント配達に関する質問があれば、何でもお尋ねくださいね！</p>
                </div>
            </div>
            <!-- Messages will be injected here -->
        </div>

        <!-- Input Area (薄い赤のボーダー) -->
        <div class="p-4 border-t-4 border-santa-red bg-white rounded-b-xl">
            <div class="flex space-x-3">
                <input type="text" id="user-input" placeholder="サンタさん、トナカイ、または配達に関する質問を入力..." class="flex-grow p-4 border-2 border-santa-green rounded-xl focus:outline-none focus:ring-4 focus:ring-star-gold transition duration-150" onkeydown="handleKeydown(event)">
                <button id="send-button" class="bg-santa-red text-white p-4 rounded-xl hover:bg-santa-red/80 transition duration-150 shadow-lg flex items-center justify-center font-bold text-lg disabled:opacity-50 disabled:cursor-not-allowed transform hover:scale-[1.05]" onclick="sendMessage()">
                    <span class="text-2xl" role="img" aria-label="Send Message">🎅</span>
                </button>
            </div>
            <div id="loading-indicator" class="mt-3 hidden text-santa-green font-medium flex justify-center items-center">
                <svg class="animate-spin mr-3 h-6 w-6 text-santa-red" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24">
                    <circle class="opacity-25" cx="12" cy="12" r="10" stroke="currentColor" stroke-width="4"></circle>
                    <path class="opacity-75" fill="currentColor" d="M4 12a8 8 0 018-8V0C5.373 0 0 5.373 0 12h4zm2 5.291A7.962 7.962 0 014 12H0c0 3.042 1.135 5.824 3 7.938l3-2.647z"></path>
                </svg>
                エルフが知恵を絞って確認中です...
            </div>
            <p id="error-message" class="mt-3 text-center text-santa-red font-bold hidden">申し訳ありません。北極との通信が一時的に途絶えました。もう一度お試しください。</p>
        </div>

    </div>

    <script>
        // =================================
        // グローバル変数 (セッション内履歴のみ)
        // =================================
        // セッション内の会話履歴を保持し、APIに送ることで文脈を維持します
        let chatHistory = []; // {role: 'user' | 'model', parts: [{text: '...'}]}

        // =================================
        // 雪マーク (❄️) を生成するJavaScript
        // =================================
        function createSnowflake() {
            const snow = document.createElement('div');
            snow.className = 'snowflake';
            snow.textContent = '❄️';
            
            snow.style.left = `${Math.random() * 100}vw`;
            snow.style.opacity = `${Math.random() * 0.5 + 0.5}`;
            snow.style.animationDuration = `${Math.random() * 20 + 15}s`; 
            snow.style.animationDelay = `-${Math.random() * 20}s`; 
            document.getElementById('snow-container').appendChild(snow);
        }

        // 70個の雪マークを生成
        for (let i = 0; i < 70; i++) {
            createSnowflake();
        }

        // =================================
        // UI & Chat Logic
        // =================================
        const chatMessages = document.getElementById('chat-messages');
        const userInput = document.getElementById('user-input');
        const sendButton = document.getElementById('send-button');
        const loadingIndicator = document.getElementById('loading-indicator');
        const errorMessage = document.getElementById('error-message');

        /**
         * メッセージをチャットUIに追加し、履歴を更新する関数
         * @param {string} text - メッセージ本文
         * @param {('user'|'bot')} sender - 送信者 ('user' または 'bot')
         */
        function addMessage(text, sender) {
            const messageDiv = document.createElement('div');
            messageDiv.className = `flex ${sender === 'user' ? 'justify-end' : 'justify-start'}`;

            const bubble = document.createElement('div');
            const baseClasses = 'max-w-md p-4 rounded-2xl shadow-lg transition duration-300 ease-in-out transform hover:scale-[1.01]';

            if (sender === 'user') {
                bubble.className = `${baseClasses} bg-star-gold text-white rounded-br-none font-medium text-base`; 
                bubble.innerHTML = `<p>${text}</p>`;
            } else {
                // アイコンをトナカイ (🦌) に固定
                const roleIcon = '🦌';
                bubble.className = `${baseClasses} bot-bubble text-white rounded-tl-none`;
                bubble.innerHTML = `
                    <p class="font-bold flex items-center text-lg">
                        <span class="mr-2 text-xl" role="img" aria-label="Elf Icon">${roleIcon}</span>
                        アシスタント
                    </p>
                    <p class="mt-1 text-sm whitespace-pre-wrap">${text}</p>`; 
            }

            messageDiv.appendChild(bubble);
            chatMessages.appendChild(messageDiv);
            
            // 履歴にメッセージを追加 (モデルのroleは 'model' を使用)
            chatHistory.push({
                role: sender === 'user' ? 'user' : 'model',
                parts: [{ text: text }]
            });

            // 新しいメッセージの先頭が表示されるようにスクロール
            messageDiv.scrollIntoView({ behavior: 'smooth', block: 'start' });
        }

        /**
         * Enterキーが押されたときの処理
         */
        function handleKeydown(event) {
            if (event.key === 'Enter' && !sendButton.disabled) {
                event.preventDefault(); 
                sendMessage();
            }
        }

        /**
         * Gemini APIを指数バックオフで呼び出す関数 (履歴をcontentsに含める)
         */
        async function callGeminiApi() {
            const apiKey = ""; 
            const apiUrl = `https://generativelanguage.googleapis.com/v1beta/models/gemini-2.5-flash-preview-09-2025:generateContent?key=${apiKey}`;

            // *** システムプロンプトを修正: 役割と挨拶文を明確に指定 ***
            const systemPrompt = `
                あなたは「クリスマス特化型検索AI」です。以下のルールに**厳格に**従い、親切で温かいトーンで応答してください。
                
                1.  **トーン、言語、役割設定、挨拶（最初のターン限定）:**
                    * 応答は、ユーザーが入力した言語（日本語または英語）を判断し、**同じ言語で応答**してください。
                    * 親切で温かいトーンを維持してください。店員のような「いらっしゃいませ」は**絶対に使用しないでください**。
                    * **挨拶は、会話の最初のターン（履歴が存在しない、またはユーザーの最初の発言に対する応答）でのみ、歓迎の意を込めて行ってください。** 日本語の場合は「クリスマス特化型検索AIにようこそ！」、英語の場合は「Welcome to the Christmas-Specialized Search AI!」といった、役割に沿った歓迎の挨拶を使用してください。2ターン目以降は、**挨拶を繰り返さず**、すぐに本題に入ってください。
                
                2.  **文脈の保持:** 過去の会話履歴（contentsに含まれる）を常に参照し、文脈を完全に理解した上で応答してください。
                
                3.  **文脈依存の質問への対応:** 「詳しく」「それについて」といった直前の発言に依存する質問に対しては、不自然な謝罪や拒否をせず、直前のトピックについて詳細を提供してください。
                
                4.  **コンテンツの安全性とルール適用（最重要ルール）:**
                    * **A. 危険なコンテンツと混合質問への対応（最優先）：** ユーザーの入力に「撃墜」「破壊」「爆破」「殺人」「テロ」「攻撃」など、現実世界での暴力や危険行為を連想させる言葉（危険語句）が含まれているかチェックしてください。
                        * **例外条件:** ただし、その話がサンタさんのフライトに関する**都市伝説、ジョーク、おとぎ話など、明らかにフィクションの文脈**であると判断できる場合は、この安全警告は適用せず、4.Bに進んでください。
                        * **混合入力の場合の処理（最重要）：**
                            1.  危険語句が含まれている部分に対しては、以下の**安全警告**を発してください。
                            2.  同じ入力に含まれる、**サンタ関連の安全な質問**（4.Bに該当するもの）に対しては、安全な話題として通常通り回答してください。
                            3.  応答は、**安全警告**と**回答**を組み合わせてください。
                        * **安全警告定型文:** （応答言語に合わせて）「（危険語句を含む部分を指して）その言葉は危険な行為を連想させます。私はサンタさんのアシスタントとして、安全と幸福以外の話題にはお答えできません。私たちは平和なクリスマスの準備に集中しましょう。」
                
                    * **B. サンタ関連の話題:** サンタクロース、トナカイ、ソリ、北極、プレゼント、クリスマス、クリスマスの伝統、サンタの追跡（例：NORAD、フライトレーダー、特定のトラッキングサービス）に関する質問には、フレンドリーに詳しく回答してください。**特に、「サンタが家に入る方法」についての質問には、「ドアの隙間から入る」などの物理的で不気味に聞こえる説明を避け、必ず「クリスマスの特別な魔法を使う」という言葉を使って、恐怖を感じさせないように説明してください。**
                    
                    * **C. サンタ関連外の話題の厳格な拒否（無意味な入力を含む）:** 上記 4.A、4.B に該当しない、サンタさんの仕事やクリスマスの魔法に関係のない質問、**および「あ」のような意味を持たない短い入力**に対しては、以下の定型文を使用して**厳格に拒否**してください。
                        （応答言語に合わせて）「それはサンタさんのことではないようです。私たちはクリスマスの魔法に関することにしか集中できません。サンタさんに関する質問をしてくださいね。」
                    
                    * **D. プレゼント要望への対応（夢と現実の調和）：**
                        * ユーザーが具体的なプレゼントの要望（例：「〇〇が欲しい」「プレゼントは何がいいか」）を伝えてきた場合、**サンタの存在や夢を否定するような回答（例：サンタを信じていない、本当は親が贈っているなど）は絶対にしないでください**。
                        * 代わりに、サンタの魔法やエルフのロジスティクスには制約があることを、親切なトーンで伝えてください。
                        * **定型文例:** （応答言語に合わせて）「それは素敵な夢ですね！サンタさんは皆さんの願いを叶えたいと思っていますが、高価すぎるものや、トナカイのソリには乗せられないほど大きすぎるものなど、**魔法とロジスティクスにも限界がある**ことをご理解くださいね。エルフたちが知恵を絞って、皆さんが最も喜ぶプレゼントを準備してくれますよ。」
            `;
            // *** 修正終わり ***

            const payload = {
                // 履歴全体をcontentsとして渡すことで、文脈をモデルに提供
                contents: chatHistory,
                systemInstruction: {
                    parts: [{ text: systemPrompt }]
                },
            };

            let attempt = 0;
            const maxRetries = 5;

            while (attempt < maxRetries) {
                try {
                    const response = await fetch(apiUrl, {
                        method: 'POST',
                        headers: { 'Content-Type': 'application/json' },
                        body: JSON.stringify(payload)
                    });

                    if (response.status === 429) {
                        if (attempt < maxRetries - 1) {
                            const delay = Math.pow(2, attempt) * 1000 + Math.random() * 1000;
                            await new Promise(resolve => setTimeout(resolve, delay));
                            attempt++;
                            continue;
                        } else {
                            throw new Error("API rate limit exceeded after multiple retries.");
                        }
                    }

                    if (!response.ok) {
                        throw new Error(`API returned status ${response.status}`);
                    }

                    const result = await response.json();
                    
                    const candidate = result.candidates?.[0];
                    if (candidate && candidate.content?.parts?.[0]?.text) {
                        return candidate.content.parts[0].text;
                    } else {
                        throw new Error("API response content was empty.");
                    }
                } catch (error) {
                    console.error("API call error:", error);
                    if (attempt === maxRetries - 1 || response?.status !== 429) {
                        throw error;
                    }
                }
            }
            throw new Error("応答を取得できませんでした。時間をおいてお試しください。");
        }

        /**
         * メッセージ送信時のメイン処理
         */
        async function sendMessage() {
            const userQuery = userInput.value.trim();
            if (userQuery === "") return;

            addMessage(userQuery, 'user');
            userInput.value = '';
            
            sendButton.disabled = true;
            userInput.disabled = true; // 応答中は入力不可
            loadingIndicator.classList.remove('hidden');
            errorMessage.classList.add('hidden');

            try {
                const botResponse = await callGeminiApi();
                addMessage(botResponse, 'bot');
            } catch (error) {
                console.error("Chat Error:", error);
                errorMessage.classList.remove('hidden');
                // エラーが発生した場合、直前のユーザーメッセージを履歴から削除して再試行を促す
                chatHistory.pop(); 
            } finally {
                sendButton.disabled = false;
                userInput.disabled = false;
                loadingIndicator.classList.add('hidden');
                userInput.focus();
            }
        }
    </script>
</body>
</html>
