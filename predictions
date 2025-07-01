const predictions = {
    achievements: [
        "will close the biggest deal in Coder history next quarter - LFG! 🚀",
        "will become the Coderite whisperer, converting every prospect with Blink-level speed ⚡",
        "will hit 150% of quota while simultaneously becoming a TikTok influencer about dev environments",
        "will discover a new sales technique so powerful, it'll be named after them in the Coder playbook",
        "will close deals so fast, Blink will seem slow in comparison 💫",
        "will become the unofficial Coder mascot after their legendary demo performance",
        "will convince a Fortune 500 company to switch to Coder using only interpretive dance",
        "will break the company record for most 'LFG!' messages sent in Slack (currently at 847)"
    ],
    
    officeLife: [
        "will consume exactly 247 cups of coffee while explaining cloud development environments",
        "will attend 73 Zoom calls where someone asks 'Can you see my screen?' at least twice",
        "will become the office expert on which snacks pair best with sales calls",
        "will master the art of looking engaged during budget meetings while mentally planning their next demo",
        "will develop a sixth sense for knowing when prospects are ready to hear about Coder's ROI",
        "will create the most elaborate Slack status messages, becoming a company legend",
        "will accidentally become the office DJ after one too many 'pump up the team' playlists",
        "will perfect the 'confident nod' during technical discussions they don't fully understand"
    ],
    
    market: [
        "will witness the great 'Return to Office vs Remote Development' debate of 2025",
        "will see every company realize that dev environment setup shouldn't take 3 days",
        "will watch as 'Coder' becomes a verb, like 'Google' but for spinning up dev environments",
        "will experience the moment when every developer realizes local development is so 2023",
        "will be part of the cloud development revolution that makes on-premise setups extinct",
        "will see Blink become the new standard for measuring development speed",
        "will witness the birth of a new job title: 'Chief Development Environment Officer'",
        "will watch as every tech conference has at least 5 talks about cloud development environments"
    ],
    
    personal: [
        "will develop an uncanny ability to explain complex technical concepts using food analogies",
        "will become fluent in 'developer speak' and start using terms like 'containerization' at dinner parties",
        "will master the art of the 15-minute demo that feels like a 5-minute conversation",
        "will develop superhuman patience for explaining why cloud development environments matter",
        "will become the family tech support person, but only for development-related questions",
        "will start dreaming in YAML files and wake up with brilliant sales strategies",
        "will develop the ability to spot a frustrated developer from 50 yards away",
        "will become known for their legendary 'elevator pitch' that actually fits in an elevator ride"
    ],
    
    milestones: [
        "will help Coder reach 10,000 happy developers who never have to say 'works on my machine' again",
        "will be part of the team that makes Coder the #1 cloud development platform",
        "will contribute to Coder's IPO by closing deals that make investors say 'LFG!'",
        "will help establish Coder offices on every continent (yes, even Antarctica)",
        "will be featured in a Harvard Business School case study about revolutionary sales techniques",
        "will help Coder become so successful that 'Coderite' becomes an official job title",
        "will witness Coder's valuation hit numbers that require scientific notation",
        "will be part of the legendary sales team that made cloud development environments mainstream"
    ]
};

const categories = {
    achievements: "Next Quarter Achievement",
    officeLife: "Office Life Prediction",
    market: "Market Forecast",
    personal: "Personal Professional Fortune",
    milestones: "Company Milestone Prophecy"
};

function getRandomPrediction() {
    const categoryKeys = Object.keys(predictions);
    const randomCategory = categoryKeys[Math.floor(Math.random() * categoryKeys.length)];
    const categoryPredictions = predictions[randomCategory];
    const randomPrediction = categoryPredictions[Math.floor(Math.random() * categoryPredictions.length)];
    
    return {
        text: randomPrediction,
        category: categories[randomCategory]
    };
}

function personalizePrediction(prediction, name, role) {
    let personalizedText = `${name} ${prediction.text}`;
    
    // Add role-specific touches
    const roleModifiers = {
        "Account Executive": " (and probably close it before lunch)",
        "Sales Development Rep": " (while generating the most qualified leads in company history)",
        "Sales Manager": " (while inspiring the team to new heights of LFG energy)",
        "Customer Success": " (and make every customer feel like a Coderite family member)",
        "Sales Engineer": " (with technical demos so smooth, they'll be used in training videos)",
        "Business Development": " (while opening doors that didn't even know they existed)",
        "Sales Operations": " (with data insights so brilliant, they'll predict the future)"
    };
    
    if (roleModifiers[role]) {
        personalizedText += roleModifiers[role];
    }
    
    return {
        text: personalizedText,
        category: prediction.category
    };
}

// Form handling
document.getElementById('predictionForm').addEventListener('submit', function(e) {
    e.preventDefault();
    
    const name = document.getElementById('name').value.trim();
    const role = document.getElementById('role').value;
    
    if (!name || !role) {
        alert('Please fill in both your name and role!');
        return;
    }
    
    // Show loading
    document.getElementById('predictBtn').disabled = true;
    document.getElementById('loading').style.display = 'block';
    document.getElementById('predictionResult').style.display = 'none';
    
    // Simulate AI thinking time for dramatic effect
    setTimeout(() => {
        const basePrediction = getRandomPrediction();
        const personalizedPrediction = personalizePrediction(basePrediction, name, role);
        
        document.getElementById('predictionText').textContent = personalizedPrediction.text;
        document.getElementById('predictionCategory').textContent = personalizedPrediction.category;
        
        // Hide loading and show result
        document.getElementById('loading').style.display = 'none';
        document.getElementById('predictionResult').style.display = 'block';
        document.getElementById('predictBtn').disabled = false;
        
        // Scroll to result
        document.getElementById('predictionResult').scrollIntoView({ 
            behavior: 'smooth', 
            block: 'center' 
        });
    }, 2000); // 2 second delay for dramatic effect
});

// Add some fun interactions
document.addEventListener('DOMContentLoaded', function() {
    // Add sparkle effect to the crystal ball emoji
    const logo = document.querySelector('.logo');
    logo.addEventListener('click', function() {
        this.style.transform = 'scale(1.2) rotate(360deg)';
        this.style.transition = 'all 0.5s ease';
        setTimeout(() => {
            this.style.transform = 'scale(1) rotate(0deg)';
        }, 500);
    });
    
    // Add LFG easter egg
    let lfgCount = 0;
    document.addEventListener('keydown', function(e) {
        const lfgSequence = ['KeyL', 'KeyF', 'KeyG'];
        if (e.code === lfgSequence[lfgCount]) {
            lfgCount++;
            if (lfgCount === 3) {
                document.body.style.background = 'linear-gradient(135deg, #ff6b6b, #4ecdc4, #45b7d1, #96ceb4, #feca57)';
                setTimeout(() => {
                    document.body.style.background = 'linear-gradient(135deg, #1a1a2e, #16213e, #0f3460)';
                }, 2000);
                lfgCount = 0;
            }
        } else {
            lfgCount = 0;
        }
    });
});
