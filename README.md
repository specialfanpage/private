<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>PrivateSpot | Exclusive World</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
}

html{
    scroll-behavior:smooth;
}

body{
    font-family:Arial, Helvetica, sans-serif;
    background:#111;
    color:#fff;
    min-height:100vh;
}

button,
input,
select{
    font-family:inherit;
}

button{
    cursor:pointer;
}

nav{
    width:100%;
    background:#090909;
    border-bottom:1px solid #292929;
    position:sticky;
    top:0;
    z-index:1000;
}

.nav-inner{
    max-width:1200px;
    margin:auto;
    padding:18px 25px;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.logo{
    font-size:24px;
    font-weight:800;
    color:#ff4d88;
    letter-spacing:.5px;
}

.nav-links{
    list-style:none;
    display:flex;
    gap:25px;
    align-items:center;
}

.nav-links a{
    color:#fff;
    text-decoration:none;
    font-size:15px;
    cursor:pointer;
    transition:.3s;
}

.nav-links a:hover{
    color:#ff4d88;
}

.page{
    display:none;
    min-height:calc(100vh - 75px);
    padding:60px 20px;
}

.page.active{
    display:block;
}

/* HOME */

.home-page{
    background:linear-gradient(135deg,#111,#24111a);
    display:none;
    align-items:center;
    justify-content:center;
    text-align:center;
}

.home-page.active{
    display:flex;
}

.home-content{
    max-width:750px;
}

.home-content h1{
    font-size:58px;
    line-height:1.1;
    margin-bottom:22px;
}

.home-content h1 span{
    color:#ff4d88;
}

.home-content p{
    color:#d6d6d6;
    font-size:18px;
    line-height:1.7;
    margin-bottom:35px;
}

.main-btn{
    border:none;
    background:#ff4d88;
    color:white;
    padding:15px 30px;
    border-radius:10px;
    font-size:16px;
    font-weight:bold;
    transition:.3s;
}

.main-btn:hover{
    transform:translateY(-2px);
    background:#ff286e;
}

/* ABOUT */

.about-page{
    background:#18121a;
}

.content-width{
    max-width:900px;
    margin:auto;
}

.section-title{
    text-align:center;
    font-size:42px;
    margin-bottom:35px;
}

.about-text{
    background:#211a23;
    border:1px solid #3a2935;
    border-radius:18px;
    padding:35px;
    line-height:1.9;
    color:#ddd;
    font-size:17px;
}

.about-text p{
    margin-bottom:20px;
}

/* FORMS */

.form-page{
    background:#151515;
}

.form-box{
    width:100%;
    max-width:500px;
    margin:auto;
    background:#1e1e1e;
    border:1px solid #303030;
    border-radius:18px;
    padding:35px;
    box-shadow:0 15px 50px rgba(0,0,0,.35);
}

.form-box h2{
    text-align:center;
    margin-bottom:10px;
    font-size:30px;
}

.form-box .subtext{
    text-align:center;
    color:#aaa;
    margin-bottom:28px;
}

.form-group{
    margin-bottom:18px;
}

.form-group label{
    display:block;
    margin-bottom:8px;
    color:#ddd;
}

.form-group input,
.form-group select{
    width:100%;
    padding:14px;
    border-radius:9px;
    border:1px solid #444;
    background:#111;
    color:white;
    outline:none;
}

.form-group input:focus,
.form-group select:focus{
    border-color:#ff4d88;
}

.full-btn{
    width:100%;
}

/* WELCOME */

.welcome-page{
    background:linear-gradient(135deg,#160f15,#28131e);
}

.welcome-box{
    max-width:850px;
    margin:50px auto;
    text-align:center;
}

.welcome-box h1{
    font-size:50px;
    margin-bottom:20px;
}

.welcome-box h1 span{
    color:#ff4d88;
}

.welcome-box p{
    color:#d0d0d0;
    line-height:1.8;
    font-size:18px;
    margin-bottom:35px;
}

/* REGISTRATION */

.registration-page{
    background:#131820;
}

.info-grid{
    max-width:1000px;
    margin:40px auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:20px;
}

.info-card{
    background:#1a222c;
    border:1px solid #303d4b;
    padding:30px;
    border-radius:17px;
    text-align:center;
}

.info-card .icon{
    font-size:38px;
    margin-bottom:15px;
}

.info-card h3{
    margin-bottom:10px;
}

.info-card p{
    color:#aaa;
    line-height:1.6;
}

.center{
    text-align:center;
}

/* CONTENT */

.content-page{
    background:#111318;
}

.content-header{
    text-align:center;
    max-width:800px;
    margin:auto auto 35px;
}

.content-header h1{
    font-size:44px;
    margin-bottom:15px;
}

.content-header p{
    color:#aaa;
    line-height:1.7;
}

.tabs{
    display:flex;
    justify-content:center;
    gap:10px;
    flex-wrap:wrap;
    margin-bottom:30px;
}

.tab{
    background:#22252c;
    color:white;
    border:1px solid #353941;
    padding:10px 18px;
    border-radius:30px;
}

.tab:hover{
    background:#ff4d88;
}

.gallery{
    max-width:1100px;
    margin:auto;
    display:grid;
    grid-template-columns:repeat(4,1fr);
    gap:18px;
}

.locked-card{
    min-height:210px;
    background:linear-gradient(145deg,#24242a,#16161a);
    border:1px solid #333;
    border-radius:16px;
    display:flex;
    flex-direction:column;
    align-items:center;
    justify-content:center;
    text-align:center;
    padding:20px;
}

.locked-card .lock{
    font-size:35px;
    margin-bottom:15px;
}

.locked-card h3{
    margin-bottom:8px;
}

.locked-card p{
    color:#999;
    font-size:14px;
}

.video-section{
    max-width:1100px;
    margin:55px auto 0;
}

.video-section h2{
    margin-bottom:20px;
}

/* PLANS */

.plans-page{
    background:linear-gradient(135deg,#120f15,#24131d);
}

.plans-grid{
    max-width:1050px;
    margin:40px auto;
    display:grid;
    grid-template-columns:repeat(3,1fr);
    gap:22px;
}

.plan{
    background:#1b171d;
    border:1px solid #39313a;
    border-radius:18px;
    padding:32px;
    text-align:center;
    position:relative;
}

.plan.popular{
    border:2px solid #ff4d88;
}

.popular-badge{
    position:absolute;
    top:-13px;
    left:50%;
    transform:translateX(-50%);
    background:#ff4d88;
    padding:6px 16px;
    border-radius:30px;
    font-size:12px;
    font-weight:bold;
}

.plan h3{
    font-size:25px;
    margin-bottom:12px;
}

.price{
    font-size:35px;
    color:#ff4d88;
    font-weight:bold;
    margin-bottom:20px;
}

.plan p{
    color:#aaa;
    margin-bottom:25px;
}

/* PAYMENT MODAL */

.modal{
    display:none;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.85);
    z-index:3000;
    padding:20px;
    overflow-y:auto;
}

.modal.active{
    display:flex;
    align-items:center;
    justify-content:center;
}

.modal-box{
    width:100%;
    max-width:650px;
    background:#1b1b1b;
    border:1px solid #393939;
    border-radius:18px;
    padding:30px;
    position:relative;
}

.close-modal{
    position:absolute;
    right:18px;
    top:15px;
    border:none;
    background:none;
    color:#fff;
    font-size:25px;
}

.payment-summary{
    background:#111;
    padding:18px;
    border-radius:10px;
    margin:20px 0;
}

.payment-methods{
    display:grid;
    grid-template-columns:1fr 1fr;
    gap:12px;
    margin-bottom:20px;
}

.payment-method{
    background:#242424;
    color:#fff;
    border:1px solid #3b3b3b;
    padding:15px;
    border-radius:10px;
}

.payment-method.active{
    border-color:#ff4d88;
    background:#291722;
}

.payment-section{
    display:none;
}

.payment-section.active{
    display:block;
}

.wallet-box{
    background:#111;
    padding:15px;
    border-radius:10px;
    margin-bottom:15px;
    word-break:break-all;
}

.wallet-box strong{
    display:block;
    margin-bottom:8px;
    color:#ff4d88;
}

.copy-btn{
    margin-top:10px;
    background:#292929;
    border:1px solid #444;
    color:white;
    padding:8px 12px;
    border-radius:7px;
}

.file-preview{
    margin-top:12px;
}

.file-preview img{
    max-width:180px;
    max-height:180px;
    border-radius:10px;
    border:1px solid #444;
}

.remove-file{
    display:block;
    margin-top:8px;
    background:#333;
    border:none;
    color:#fff;
    padding:7px 10px;
    border-radius:6px;
}

/* CHAT */

.chat-page{
    background:#101116;
    padding:30px 15px;
}

.chat-container{
    max-width:850px;
    height:calc(100vh - 135px);
    min-height:600px;
    margin:auto;
    display:flex;
    flex-direction:column;
    background:#17181e;
    border:1px solid #30313a;
    border-radius:18px;
    overflow:hidden;
    box-shadow:0 20px 70px rgba(0,0,0,.4);
}

.chat-header{
    padding:18px 20px;
    background:#1d1e25;
    border-bottom:1px solid #30313a;
    display:flex;
    align-items:center;
    justify-content:space-between;
}

.chat-profile{
    display:flex;
    align-items:center;
    gap:12px;
}

.chat-avatar{
    width:45px;
    height:45px;
    border-radius:50%;
    background:#ff4d88;
    display:flex;
    align-items:center;
    justify-content:center;
    font-weight:bold;
    font-size:20px;
}

.chat-name h3{
    font-size:16px;
}

.chat-status{
    color:#4de18b;
    font-size:12px;
    margin-top:3px;
}

.chat-private{
    font-size:13px;
    color:#aaa;
}

.chat-messages{
    flex:1;
    overflow-y:auto;
    padding:25px;
    background:
        radial-gradient(circle at top right,rgba(255,77,136,.08),transparent 35%),
        #101116;
}

.chat-welcome{
    text-align:center;
    color:#aaa;
    padding:50px 20px;
}

.chat-lock{
    font-size:42px;
    margin-bottom:12px;
}

.chat-welcome h2{
    color:#fff;
    margin-bottom:10px;
}

.message{
    display:flex;
    margin-bottom:15px;
}

.message.subscriber{
    justify-content:flex-end;
}

.message.creator{
    justify-content:flex-start;
}

.message.ai{
    justify-content:flex-start;
}

.message-bubble{
    max-width:75%;
    padding:12px 15px;
    border-radius:15px;
    line-height:1.5;
    font-size:14px;
}

.message.subscriber .message-bubble{
    background:#ff4d88;
    color:#fff;
    border-bottom-right-radius:4px;
}

.message.creator .message-bubble,
.message.ai .message-bubble{
    background:#292b33;
    color:#eee;
    border-bottom-left-radius:4px;
}

.message-time{
    display:block;
    margin-top:5px;
    font-size:10px;
    opacity:.65;
}

.chat-input-area{
    padding:15px;
    background:#1b1c22;
    border-top:1px solid #30313a;
}

.chat-form{
    display:flex;
    gap:10px;
}

.chat-input{
    flex:1;
    background:#101116;
    border:1px solid #3b3c45;
    color:white;
    padding:14px;
    border-radius:10px;
    outline:none;
}

.chat-input:focus{
    border-color:#ff4d88;
}

.chat-send{
    width:50px;
    border:none;
    background:#ff4d88;
    color:#fff;
    border-radius:10px;
    font-size:20px;
}

.chat-tools{
    display:flex;
    gap:8px;
    margin-top:10px;
    flex-wrap:wrap;
}

.ai-btn{
    background:#292b33;
    color:#fff;
    border:1px solid #41434d;
    padding:9px 13px;
    border-radius:8px;
    font-size:13px;
}

.ai-btn:hover{
    border-color:#ff4d88;
}

.chat-note{
    color:#777;
    font-size:11px;
    margin-top:9px;
}

.message-counter{
    margin-top:10px;
    font-size:11px;
    color:#888;
    text-align:right;
}

.handoff-box{
    background:#211923;
    border:1px solid #5b2940;
    border-radius:12px;
    padding:15px;
    margin:15px 0;
}

.handoff-box strong{
    color:#ff4d88;
}

.telegram-btn{
    display:inline-block;
    margin-top:12px;
    padding:11px 18px;
    background:#229ed9;
    color:#fff;
    border-radius:8px;
    text-decoration:none;
    font-weight:bold;
}

/* X NOTICE */

.followers-notice{
    position:fixed;
    right:20px;
    bottom:20px;
    background:#202027;
    border:1px solid #ff4d88;
    color:#fff;
    padding:14px 18px;
    border-radius:10px;
    box-shadow:0 10px 30px rgba(0,0,0,.4);
    z-index:2000;
    opacity:0;
    transform:translateY(20px);
    pointer-events:none;
    transition:.4s;
}

.followers-notice.show{
    opacity:1;
    transform:translateY(0);
}

/* FOOTER */

footer{
    background:#090909;
    color:#777;
    text-align:center;
    padding:20px;
    font-size:13px;
}

/* RESPONSIVE */

@media(max-width:900px){

    .gallery{
        grid-template-columns:repeat(2,1fr);
    }

    .plans-grid{
        grid-template-columns:1fr;
        max-width:500px;
    }

    .info-grid{
        grid-template-columns:1fr;
        max-width:500px;
    }

    .home-content h1{
        font-size:45px;
    }
}

@media(max-width:650px){

    .nav-inner{
        flex-direction:column;
        gap:15px;
    }

    .nav-links{
        flex-wrap:wrap;
        justify-content:center;
        gap:13px;
    }

    .page{
        padding:40px 15px;
    }

    .home-content h1{
        font-size:38px;
    }

    .section-title{
        font-size:32px;
    }

    .gallery{
        grid-template-columns:1fr;
    }

    .payment-methods{
        grid-template-columns:1fr;
    }

    .chat-container{
        height:calc(100vh - 150px);
        min-height:500px;
    }

    .chat-private{
        display:none;
    }

    .message-bubble{
        max-width:88%;
    }

    .followers-notice{
        left:15px;
        right:15px;
        bottom:15px;
    }
}
</style>
</head>

<body>

<nav>
    <div class="nav-inner">

        <div class="logo">
            PrivateSpot
        </div>

        <ul class="nav-links">

            <li>
                <a onclick="showPage('home')">
                    Home
                </a>
            </li>

            <li>
                <a onclick="showPage('about')">
                    About
                </a>
            </li>

            <li>
                <a onclick="showPage('signup')">
                    Signup
                </a>
            </li>

            <li>
                <a onclick="showPage('login')">
                    Login
                </a>
            </li>

            <li>
                <a onclick="showChat()">
                    💬 Chat
                </a>
            </li>

        </ul>
    </div>
</nav>


<!-- HOME -->

<section id="home" class="page home-page active">

    <div class="home-content">

        <h1>
            Welcome to
            <span>PrivateSpot</span>
        </h1>

        <p>
            Enter my exclusive world and discover private moments,
            special updates, photos, videos, and content created just for you.
        </p>

        <button class="main-btn" onclick="showPage('signup')">
            Join Now
        </button>

    </div>

</section>


<!-- ABOUT -->

<section id="about" class="page about-page">

    <div class="content-width">

        <h2 class="section-title">
            About PrivateSpot
        </h2>

        <div class="about-text">

            <p>
                PrivateSpot is where curiosity gets rewarded and the ordinary
                stays outside. Step a little closer and discover a side of me
                that I don't leave sitting in the public eye.
            </p>

            <p>
                Behind these doors, things become a little more private,
                playful, mysterious, and tempting. Expect irresistible moments,
                exclusive looks, personal updates, intimate little surprises,
                and content made to keep you wondering what might be waiting
                for you next.
            </p>

            <p>
                This is your invitation into my more personal world — a place
                where I can be a little bolder, a little more playful, and give
                my subscribers something they won't find anywhere else.
            </p>

            <p>
                Come curious. Stay for the secrets.
                Your private invitation starts here.
            </p>

        </div>

    </div>

</section>


<!-- SIGNUP -->

<section id="signup" class="page form-page">

    <div class="form-box">

        <h2>Create Your Account</h2>

        <p class="subtext">
            Join PrivateSpot and enter the exclusive world.
        </p>

        <form onsubmit="signup(event)">

            <div class="form-group">
                <label>Full Name</label>
                <input
                    type="text"
                    id="signupName"
                    required
                    placeholder="Enter your full name"
                >
            </div>

            <div class="form-group">
                <label>Email Address</label>
                <input
                    type="email"
                    id="signupEmail"
                    required
                    placeholder="Enter your email"
                >
            </div>

            <div class="form-group">
                <label>Password</label>
                <input
                    type="password"
                    id="signupPassword"
                    required
                    placeholder="Create a password"
                >
            </div>

            <button class="main-btn full-btn" type="submit">
                Sign Up
            </button>

        </form>

    </div>

</section>


<!-- LOGIN -->

<section id="login" class="page form-page">

    <div class="form-box">

        <h2>Login</h2>

        <p class="subtext">
            Welcome back to your private world.
        </p>

        <form onsubmit="login(event)">

            <div class="form-group">
                <label>Email Address</label>
                <input
                    type="email"
                    id="loginEmail"
                    required
                    placeholder="Enter your email"
                >
            </div>

            <div class="form-group">
                <label>Password</label>
                <input
                    type="password"
                    id="loginPassword"
                    required
                    placeholder="Enter your password"
                >
            </div>

            <button class="main-btn full-btn" type="submit">
                Login
            </button>

        </form>

    </div>

</section>


<!-- WELCOME -->

<section id="welcome" class="page welcome-page">

    <div class="welcome-box">

        <h1>
            Welcome,
            <span id="welcomeName">Beautiful</span>
        </h1>

        <p>
            You are now inside PrivateSpot.
            Your private journey starts here.
            Explore exclusive content, personal updates,
            private conversations and more.
        </p>

        <button
            class="main-btn"
            onclick="showPage('registration')"
        >
            Start Exploring
        </button>

    </div>

</section>


<!-- REGISTRATION -->

<section id="registration" class="page registration-page">

    <h2 class="section-title">
        Welcome to My Private World
    </h2>

    <div class="info-grid">

        <div class="info-card">

            <div class="icon">
                🔒
            </div>

            <h3>
                Private Content
            </h3>

            <p>
                Access content created exclusively
                for subscribers.
            </p>

        </div>

        <div class="info-card">

            <div class="icon">
                📸
            </div>

            <h3>
                Exclusive Photos
            </h3>

            <p>
                Discover photos and moments
                unavailable on the public page.
            </p>

        </div>

        <div class="info-card">

            <div class="icon">
                💌
            </div>

            <h3>
                Personal Updates
            </h3>

            <p>
                Stay closer with private updates
                and subscriber conversations.
            </p>

        </div>

    </div>

    <div class="center">

        <button
            class="main-btn"
            onclick="showPage('content')"
        >
            Explore
        </button>

    </div>

</section>


<!-- CONTENT -->

<section id="content" class="page content-page">

    <div class="content-header">

        <h1>
            Welcome to My Exclusive World
        </h1>

        <p>
            Your private collection is waiting.
            Subscribe to unlock exclusive photos,
            videos, personal updates and more.
        </p>

    </div>

    <div class="tabs">

        <button class="tab">
            All Content
        </button>

        <button class="tab">
            Photos
        </button>

        <button class="tab">
            Videos
        </button>

        <button class="tab">
            Updates
        </button>

    </div>

    <div class="gallery">

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Private Photo</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Exclusive Look</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Private Update</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Special Moment</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Private Collection</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Behind The Scenes</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Personal Post</h3>
            <p>Subscribers only</p>
        </div>

        <div class="locked-card">
            <div class="lock">🔒</div>
            <h3>Exclusive Surprise</h3>
            <p>Subscribers only</p>
        </div>

    </div>

    <div class="video-section">

        <h2>
            Exclusive Videos
        </h2>

        <div class="gallery">

            <div class="locked-card">
                <div class="lock">🎥🔒</div>
                <h3>Private Video 01</h3>
                <p>Locked for subscribers</p>
            </div>

            <div class="locked-card">
                <div class="lock">🎥🔒</div>
                <h3>Private Video 02</h3>
                <p>Locked for subscribers</p>
            </div>

            <div class="locked-card">
                <div class="lock">🎥🔒</div>
                <h3>Private Video 03</h3>
                <p>Locked for subscribers</p>
            </div>

            <div class="locked-card">
                <div class="lock">🎥🔒</div>
                <h3>Private Video 04</h3>
                <p>Locked for subscribers</p>
            </div>

        </div>

    </div>

    <div class="center" style="margin-top:45px;">

        <p style="color:#aaa;margin-bottom:15px;">
            Ready to unlock the private side?
        </p>

        <button
            class="main-btn"
            onclick="showPage('plans')"
        >
            View Subscription Plans
        </button>

    </div>

</section>


<!-- PLANS -->

<section id="plans" class="page plans-page">

    <h2 class="section-title">
        Choose Your Subscription
    </h2>

    <div class="plans-grid">

        <div class="plan">

            <h3>
                Regular
            </h3>

            <div class="price">
                $50
            </div>

            <p>
                Monthly subscription
            </p>

            <button
                class="main-btn"
                onclick="selectPlan('Regular',50)"
            >
                Choose Regular
            </button>

        </div>


        <div class="plan popular">

            <div class="popular-badge">
                MOST POPULAR
            </div>

            <h3>
                Premium
            </h3>

            <div class="price">
                $100
            </div>

            <p>
                Monthly subscription
            </p>

            <button
                class="main-btn"
                onclick="selectPlan('Premium',100)"
            >
                Choose Premium
            </button>

        </div>


        <div class="plan">

            <h3>
                VIP
            </h3>

            <div class="price">
                $200
            </div>

            <p>
                Monthly subscription
            </p>

            <button
                class="main-btn"
                onclick="selectPlan('VIP',200)"
            >
                Choose VIP
            </button>

        </div>

    </div>

</section>


<!-- CHAT -->

<section id="chat" class="page chat-page">

    <div class="chat-container">

        <div class="chat-header">

            <div class="chat-profile">

                <div class="chat-avatar">
                    P
                </div>

                <div class="chat-name">

                    <h3>
                        PrivateSpot
                    </h3>

                    <div class="chat-status">
                        ● Online
                    </div>

                </div>

            </div>

            <div class="chat-private">
                🔒 Private Chat
            </div>

        </div>


        <div
            class="chat-messages"
            id="chatMessages"
        >

            <div class="chat-welcome">

                <div class="chat-lock">
                    💬
                </div>

                <h2>
                    Chat With Me
                </h2>

                <p>
                    Welcome to my private chat.
                    Send me a message and start a conversation.
                </p>

            </div>

        </div>


        <div class="chat-input-area">

            <form
                class="chat-form"
                onsubmit="sendMessage(event)"
            >

                <input
                    type="text"
                    id="chatInput"
                    class="chat-input"
                    placeholder="Write a message..."
                    autocomplete="off"
                >

                <button
                    type="submit"
                    class="chat-send"
                    aria-label="Send message"
                >
                    ➤
                </button>

            </form>


            <div class="chat-tools">

                <button
                    type="button"
                    class="ai-btn"
                    onclick="generateAIReply()"
                >
                    ✨ AI Reply
                </button>

                <button
                    type="button"
                    class="ai-btn"
                    onclick="clearChat()"
                >
                    Clear Chat
                </button>

            </div>


            <div class="chat-note">
                ✨ AI Reply creates a suggested response based on the subscriber's latest message.
            </div>

            <div
                class="message-counter"
                id="messageCounter"
            >
                Messages: 0 / 25
            </div>

        </div>

    </div>

</section>


<!-- PAYMENT MODAL -->

<div
    class="modal"
    id="paymentModal"
>

    <div class="modal-box">

        <button
            class="close-modal"
            onclick="closePayment()"
        >
            ×
        </button>

        <h2>
            Complete Your Payment
        </h2>

        <div
            class="payment-summary"
            id="paymentSummary"
        >
            Selected Plan
        </div>

        <div class="payment-methods">

            <button
                class="payment-method active"
                id="cryptoMethod"
                onclick="showPaymentMethod('crypto')"
            >
                ₿ Crypto Payment
            </button>

            <button
                class="payment-method"
                id="giftMethod"
                onclick="showPaymentMethod('gift')"
            >
                🎁 Gift Card Payment
            </button>

        </div>


        <!-- CRYPTO -->

        <div
            id="cryptoSection"
            class="payment-section active"
        >

            <div class="form-group">

                <label>
                    Cryptocurrency
                </label>

                <select id="cryptoType">

                    <option value="BTC">
                        Bitcoin (BTC)
                    </option>

                    <option value="USDT BEP20">
                        USDT BEP20
                    </option>

                    <option value="Ethereum ERC20">
                        Ethereum ERC20
                    </option>

                </select>

            </div>


            <div class="wallet-box">

                <strong>
                    BTC Wallet
                </strong>

                <span>
                    13CVQWXmyHA1YgcH9JDUq7BWkZGfcdKEoN
                </span>

                <br>

                <button
                    class="copy-btn"
                    onclick="copyText('13CVQWXmyHA1YgcH9JDUq7BWkZGfcdKEoN')"
                >
                    Copy
                </button>

            </div>


            <div class="wallet-box">

                <strong>
                    USDT BEP20 / Ethereum ERC20
                </strong>

                <span>
                    0x2d1a039b1b44f2605c055d2cc67a3b08f5127457
                </span>

                <br>

                <button
                    class="copy-btn"
                    onclick="copyText('0x2d1a039b1b44f2605c055d2cc67a3b08f5127457')"
                >
                    Copy
                </button>

            </div>


            <div class="form-group">

                <label>
                    Transaction / Reference ID
                </label>

                <input
                    type="text"
                    id="cryptoReference"
                    placeholder="Enter transaction ID"
                >

            </div>


            <div class="form-group">

                <label>
                    Upload Payment Screenshot
                </label>

                <input
                    type="file"
                    id="cryptoScreenshot"
                    accept="image/*"
                    onchange="previewFile('cryptoScreenshot','cryptoPreview')"
                >

                <div
                    class="file-preview"
                    id="cryptoPreview"
                ></div>

            </div>

        </div>


        <!-- GIFT CARD -->

        <div
            id="giftSection"
            class="payment-section"
        >

            <div class="form-group">

                <label>
                    Gift Card Type
                </label>

                <select id="giftType">

                    <option>
                        Amazon
                    </option>

                    <option>
                        Apple
                    </option>

                    <option>
                        Google Play
                    </option>

                    <option>
                        Steam
                    </option>

                    <option>
                        Other
                    </option>

                </select>

            </div>


            <div class="form-group">

                <label>
                    Gift Card Reference
                </label>

                <input
                    type="text"
                    id="giftReference"
                    placeholder="Enter gift card reference"
                >

            </div>


            <div class="form-group">

                <label>
                    Upload Gift Card Screenshot
                </label>

                <input
                    type="file"
                    id="giftScreenshot"
                    accept="image/*"
                    onchange="previewFile('giftScreenshot','giftPreview')"
                >

                <div
                    class="file-preview"
                    id="giftPreview"
                ></div>

            </div>

        </div>


        <button
            class="main-btn full-btn"
            onclick="submitPayment()"
        >
            Submit Payment
        </button>

    </div>

</div>


<div
    class="followers-notice"
    id="followersNotice"
    aria-live="polite"
>
    🔥 A profile from X just joined
</div>


<footer>
    © 2026 PrivateSpot. All rights reserved.
</footer>


<script>

/* ==========================================
   BASIC PAGE NAVIGATION
========================================== */

function showPage(pageId){

    const pages = document.querySelectorAll(".page");

    pages.forEach(page=>{
        page.classList.remove("active");
    });

    const selected = document.getElementById(pageId);

    if(selected){
        selected.classList.add("active");
    }

    window.scrollTo({
        top:0,
        behavior:"smooth"
    });

}


/* ==========================================
   SIGNUP
========================================== */

function signup(event){

    event.preventDefault();

    const name =
        document.getElementById("signupName").value.trim();

    const email =
        document.getElementById("signupEmail").value.trim();

    const password =
        document.getElementById("signupPassword").value;

    if(!name || !email || !password){
        alert("Please complete all fields.");
        return;
    }

    const user = {
        name:name,
        email:email,
        password:password
    };

    localStorage.setItem(
        "privateSpotUser",
        JSON.stringify(user)
    );

    document.getElementById("welcomeName").textContent = name;

    alert("Your PrivateSpot account has been created.");

    showPage("welcome");

}


/* ==========================================
   LOGIN
========================================== */

function login(event){

    event.preventDefault();

    const email =
        document.getElementById("loginEmail").value.trim();

    const password =
        document.getElementById("loginPassword").value;

    const savedUser =
        JSON.parse(
            localStorage.getItem("privateSpotUser") || "null"
        );

    if(!savedUser){

        alert(
            "No account was found. Please create an account first."
        );

        return;
    }

    if(
        email === savedUser.email &&
        password === savedUser.password
    ){

        document.getElementById("welcomeName").textContent =
            savedUser.name;

        alert("Login successful.");

        showPage("welcome");

    }else{

        alert("Incorrect email or password.");

    }

}


/* ==========================================
   PLAN SELECTION
========================================== */

let selectedPlan = null;
let selectedPrice = null;

function selectPlan(plan,price){

    selectedPlan = plan;
    selectedPrice = price;

    document.getElementById("paymentSummary").innerHTML =
        "<strong>Plan:</strong> " +
        plan +
        "<br><strong>Amount:</strong> $" +
        price +
        " / month";

    document
        .getElementById("paymentModal")
        .classList.add("active");

}


/* ==========================================
   PAYMENT METHOD
========================================== */

function showPaymentMethod(method){

    const cryptoSection =
        document.getElementById("cryptoSection");

    const giftSection =
        document.getElementById("giftSection");

    const cryptoMethod =
        document.getElementById("cryptoMethod");

    const giftMethod =
        document.getElementById("giftMethod");

    if(method === "crypto"){

        cryptoSection.classList.add("active");
        giftSection.classList.remove("active");

        cryptoMethod.classList.add("active");
        giftMethod.classList.remove("active");

    }else{

        giftSection.classList.add("active");
        cryptoSection.classList.remove("active");

        giftMethod.classList.add("active");
        cryptoMethod.classList.remove("active");

    }

}


/* ==========================================
   CLOSE PAYMENT
========================================== */

function closePayment(){

    document
        .getElementById("paymentModal")
        .classList.remove("active");

}


/* ==========================================
   COPY WALLET
========================================== */

function copyText(text){

    navigator.clipboard.writeText(text)
        .then(()=>{
            alert("Wallet address copied.");
        })
        .catch(()=>{
            alert("Unable to copy automatically.");
        });

}


/* ==========================================
   FILE PREVIEW
========================================== */

function previewFile(inputId,previewId){

    const input =
        document.getElementById(inputId);

    const preview =
        document.getElementById(previewId);

    preview.innerHTML = "";

    if(!input.files || !input.files[0]){
        return;
    }

    const file = input.files[0];

    if(!file.type.startsWith("image/")){
        return;
    }

    const reader = new FileReader();

    reader.onload = function(event){

        preview.innerHTML =
            `
            <img src="${event.target.result}" alt="Payment screenshot">

            <button
                class="remove-file"
                type="button"
                onclick="removePreview('${inputId}','${previewId}')"
            >
                Remove
            </button>
            `;

    };

    reader.readAsDataURL(file);

}


/* ==========================================
   REMOVE FILE
========================================== */

function removePreview(inputId,previewId){

    document.getElementById(inputId).value = "";

    document.getElementById(previewId).innerHTML = "";

}


/* ==========================================
   PAYMENT SUBMISSION
========================================== */

function submitPayment(){

    const cryptoActive =
        document
            .getElementById("cryptoSection")
            .classList.contains("active");

    if(cryptoActive){

        const reference =
            document
                .getElementById("cryptoReference")
                .value.trim();

        const screenshot =
            document
                .getElementById("cryptoScreenshot")
                .files.length;

        if(!reference){

            alert(
                "Please enter your transaction/reference ID."
            );

            return;
        }

        if(!screenshot){

            alert(
                "Please upload your payment screenshot."
            );

            return;
        }

    }else{

        const reference =
            document
                .getElementById("giftReference")
                .value.trim();

        const screenshot =
            document
                .getElementById("giftScreenshot")
                .files.length;

        if(!reference){

            alert(
                "Please enter your gift card reference."
            );

            return;
        }

        if(!screenshot){

            alert(
                "Please upload your gift card screenshot."
            );

            return;
        }

    }

    alert(
        "Your payment information has been submitted for review."
    );

    closePayment();

}


/* ==========================================
   CHAT STORAGE
========================================== */

function getChatMessages(){

    return JSON.parse(
        localStorage.getItem("privateSpotChat") || "[]"
    );

}


function saveChatMessages(messages){

    localStorage.setItem(
        "privateSpotChat",
        JSON.stringify(messages)
    );

}


/* ==========================================
   CHAT NAVIGATION
========================================== */

function showChat(){

    showPage("chat");

    loadChatMessages();

}


/* ==========================================
   CHAT MESSAGE COUNTER
========================================== */

function getMessageCount(){

    return parseInt(
        localStorage.getItem("privateSpotMessageCount") || "0",
        10
    );

}


function setMessageCount(count){

    localStorage.setItem(
        "privateSpotMessageCount",
        String(count)
    );

}


function updateMessageCounter(){

    const count = getMessageCount();

    document.getElementById("messageCounter").textContent =
        "Messages: " + count + " / 25";

}


/* ==========================================
   SEND MESSAGE
========================================== */

function sendMessage(event){

    event.preventDefault();

    const input =
        document.getElementById("chatInput");

    const message =
        input.value.trim();

    if(!message){
        return;
    }

    let messages = getChatMessages();

    const currentCount = getMessageCount();

    /*
       Once the 25-message limit is reached,
       direct the subscriber toward Telegram.
    */

    if(currentCount >= 25){

        showTelegramHandoff();

        input.value = "";

        return;
    }


    messages.push({

        sender:"subscriber",

        text:message,

        time:new Date().toLocaleTimeString([],{
            hour:"2-digit",
            minute:"2-digit"
        })

    });


    saveChatMessages(messages);


    setMessageCount(currentCount + 1);


    input.value = "";


    loadChatMessages();


    /*
       Automatically check the subscriber's
       message for complicated topics.
    */

    if(isComplicatedQuestion(message)){

        setTimeout(()=>{

            addAIMessage(
                "This sounds like something that may be easier to handle personally. Would you like me to direct you to a live chat session?"
            );

        },700);

    }

}


/* ==========================================
   LOAD CHAT
========================================== */

function loadChatMessages(){

    const container =
        document.getElementById("chatMessages");

    const messages =
        getChatMessages();

    container.innerHTML = "";


    if(messages.length === 0){

        container.innerHTML = `

            <div class="chat-welcome">

                <div class="chat-lock">
                    💬
                </div>

                <h2>
                    Chat With Me
                </h2>

                <p>
                    Welcome to my private chat.
                    Send me a message and start a conversation.
                </p>

            </div>

        `;

        updateMessageCounter();

        return;

    }


    messages.forEach(message=>{

        addMessageToScreen(
            message.sender,
            message.text,
            message.time
        );

    });


    updateMessageCounter();


    container.scrollTop =
        container.scrollHeight;

}


/* ==========================================
   ADD MESSAGE TO SCREEN
========================================== */

function addMessageToScreen(sender,text,time){

    const container =
        document.getElementById("chatMessages");

    const wrapper =
        document.createElement("div");

    wrapper.className =
        "message " +
        (
            sender === "subscriber"
                ? "subscriber"
                : sender === "ai"
                    ? "ai"
                    : "creator"
        );


    const bubble =
        document.createElement("div");

    bubble.className =
        "message-bubble";


    bubble.textContent = text;


    const timeElement =
        document.createElement("span");

    timeElement.className =
        "message-time";

    timeElement.textContent =
        time || "";


    bubble.appendChild(timeElement);

    wrapper.appendChild(bubble);

    container.appendChild(wrapper);

}


/* ==========================================
   ADD AI MESSAGE
========================================== */

function addAIMessage(text){

    const messages =
        getChatMessages();

    const time =
        new Date().toLocaleTimeString([],{
            hour:"2-digit",
            minute:"2-digit"
        });


    messages.push({

        sender:"ai",

        text:text,

        time:time

    });


    saveChatMessages(messages);

    loadChatMessages();

}


/* ==========================================
   AI REPLY BUTTON
========================================== */

function generateAIReply(){

    const messages =
        getChatMessages();

    if(messages.length === 0){

        alert(
            "There is no subscriber message to reply to yet."
        );

        return;

    }


    let subscriberMessages =
        messages.filter(
            message =>
                message.sender === "subscriber"
        );


    if(subscriberMessages.length === 0){

        alert(
            "There is no subscriber message to reply to yet."
        );

        return;

    }


    const latest =
        subscriberMessages[
            subscriberMessages.length - 1
        ];


    const reply =
        createAIReply(latest.text);


    addAIMessage(reply);

}


/* ==========================================
   DEMO AI REPLY ENGINE
========================================== */

function createAIReply(message){

    const text =
        message.toLowerCase();


    if(isYesResponse(text)){

        return (
            "Please hold while I direct you to a live chat session..."
        );

    }


    if(isComplicatedQuestion(message)){

        return (
            "This sounds like something that may be easier to handle personally. Would you like me to direct you to a live chat session?"
        );

    }


    if(
        text.includes("hello") ||
        text.includes("hi") ||
        text.includes("hey")
    ){

        return (
            "Hey 😊 It's good to hear from you. How are you doing?"
        );

    }


    if(
        text.includes("how are you") ||
        text.includes("how r you")
    ){

        return (
            "I'm doing well 😊 Thanks for asking. How has your day been?"
        );

    }


    if(
        text.includes("miss") ||
        text.includes("thinking about you")
    ){

        return (
            "Aww, that's sweet ❤️ I'm glad you're thinking about me."
        );

    }


    if(
        text.includes("beautiful") ||
        text.includes("pretty") ||
        text.includes("sexy") ||
        text.includes("gorgeous")
    ){

        return (
            "You're making me smile 😊 I appreciate the compliment."
        );

    }


    if(
        text.includes("love") ||
        text.includes("like you")
    ){

        return (
            "That's really sweet of you ❤️ I enjoy having you here."
        );

    }


    if(
        text.includes("photo") ||
        text.includes("picture") ||
        text.includes("pic")
    ){

        return (
            "There are some exclusive moments waiting inside. Stay tuned for more private content 😉"
        );

    }


    if(
        text.includes("video")
    ){

        return (
            "The exclusive section has some private videos available for subscribers 😉"
        );

    }


    if(
        text.includes("subscription") ||
        text.includes("subscribe") ||
        text.includes("plan")
    ){

        return (
            "You can check the available subscription plans and choose the option that works best for you."
        );

    }


    if(
        text.includes("money") ||
        text.includes("payment") ||
        text.includes("pay")
    ){

        return (
            "You can view the available subscription plans and payment options from the subscription section."
        );

    }


    if(
        text.includes("?")
    ){

        return (
            "That's an interesting question 😊 Tell me a little more about what you mean."
        );

    }


    const generalReplies = [

        "I like hearing from you 😊 Tell me more.",

        "That's interesting. What made you think about that?",

        "Hmm, tell me more about that ❤️",

        "I'm listening 😊 Keep going.",

        "I understand. What happened next?",

        "That's something we can definitely talk about. Tell me more."

    ];


    return generalReplies[
        Math.floor(
            Math.random() * generalReplies.length
        )
    ];

}


/* ==========================================
   COMPLICATED QUESTION DETECTION
========================================== */

function isComplicatedQuestion(message){

    const text =
        message.toLowerCase();


    const complicatedKeywords = [

        "legal",

        "lawyer",

        "court",

        "arrest",

        "police",

        "lawsuit",

        "contract",

        "medical",

        "doctor",

        "diagnosis",

        "medicine",

        "prescription",

        "investment",

        "invest",

        "crypto problem",

        "tax",

        "immigration",

        "visa",

        "relationship problem",

        "serious problem",

        "emergency",

        "urgent",

        "help me with",

        "what should i do",

        "what can i do",

        "how do i fix",

        "account problem",

        "technical problem",

        "payment problem"

    ];


    let score = 0;


    complicatedKeywords.forEach(keyword=>{

        if(text.includes(keyword)){
            score++;
        }

    });


    /*
       Long messages are treated as potentially
       complicated in this demo.
    */

    if(message.length > 300){
        score++;
    }


    /*
       Multiple question marks can indicate
       a more involved question.
    */

    const questionMarks =
        (message.match(/\?/g) || []).length;

    if(questionMarks >= 3){
        score++;
    }


    return score >= 1;

}


/* ==========================================
   YES / PROCEED DETECTION
========================================== */

function isYesResponse(message){

    const text =
        message
            .toLowerCase()
            .trim();


    const yesWords = [

        "yes",

        "yeah",

        "yep",

        "yup",

        "sure",

        "okay",

        "ok",

        "alright",

        "all right",

        "fine",

        "please",

        "go ahead",

        "proceed",

        "do it",

        "let's do it",

        "lets do it",

        "continue",

        "continue please",

        "i agree",

        "sounds good",

        "that works",

        "of course",

        "definitely",

        "absolutely"

    ];


    return yesWords.some(word=>{

        return (
            text === word ||
            text.includes(word)
        );

    });

}


/* ==========================================
   TELEGRAM HANDOFF
========================================== */

function showTelegramHandoff(){

    const container =
        document.getElementById("chatMessages");


    const box =
        document.createElement("div");

    box.className =
        "handoff-box";


    box.innerHTML = `

        <strong>
            Live Chat
        </strong>

        <p style="margin-top:7px;color:#ccc;">
            Please hold while I direct you to a live chat session...
        </p>

        <a
            class="telegram-btn"
            href="https://t.me/sexy_sexy_x"
            target="_blank"
            rel="noopener noreferrer"
        >
            Continue to Telegram
        </a>

    `;


    container.appendChild(box);


    container.scrollTop =
        container.scrollHeight;

}


/* ==========================================
   CHECK YES RESPONSE AFTER AI HANDOFF
========================================== */

function checkForLiveChatConfirmation(message){

    if(isYesResponse(message)){

        setTimeout(()=>{

            addAIMessage(
                "Please hold while I direct you to a live chat session..."
            );

            setTimeout(()=>{

                showTelegramHandoff();

            },1200);

        },500);

        return true;

    }

    return false;

}


/* ==========================================
   OVERRIDE SEND FOR YES RESPONSE
========================================== */

const originalSendMessage = sendMessage;

sendMessage = function(event){

    event.preventDefault();

    const input =
        document.getElementById("chatInput");

    const message =
        input.value.trim();

    if(!message){
        return;
    }


    const messages =
        getChatMessages();


    const currentCount =
        getMessageCount();


    if(currentCount >= 25){

        showTelegramHandoff();

        input.value = "";

        return;

    }


    messages.push({

        sender:"subscriber",

        text:message,

        time:new Date().toLocaleTimeString([],{
            hour:"2-digit",
            minute:"2-digit"
        })

    });


    saveChatMessages(messages);

    setMessageCount(currentCount + 1);

    input.value = "";

    loadChatMessages();


    /*
       If the last AI message asked whether
       the subscriber wants live chat, a yes
       response sends them to Telegram.
    */

    const aiMessages =
        messages.filter(
            message =>
                message.sender === "ai"
        );


    const lastAI =
        aiMessages.length
            ? aiMessages[aiMessages.length - 1]
            : null;


    if(
        lastAI &&
        lastAI.text.toLowerCase().includes(
            "would you like me to direct you"
        ) &&
        isYesResponse(message)
    ){

        setTimeout(()=>{

            addAIMessage(
                "Please hold while I direct you to a live chat session..."
            );

            setTimeout(()=>{

                showTelegramHandoff();

            },1200);

        },500);

        return;

    }


    /*
       Normal complicated-question detection.
    */

    if(isComplicatedQuestion(message)){

        setTimeout(()=>{

            addAIMessage(
                "This sounds like something that may be easier to handle personally. Would you like me to direct you to a live chat session?"
            );

        },700);

    }

};


/* ==========================================
   CLEAR CHAT
========================================== */

function clearChat(){

    const confirmClear =
        confirm(
            "Are you sure you want to clear this chat?"
        );

    if(!confirmClear){
        return;
    }

    localStorage.removeItem("privateSpotChat");

    localStorage.removeItem(
        "privateSpotMessageCount"
    );

    loadChatMessages();

}


/* ==========================================
   X NOTICE
========================================== */

function showXNotice(){

    const notice =
        document.getElementById("followersNotice");

    notice.classList.add("show");


    setTimeout(()=>{

        notice.classList.remove("show");

    },5000);

}


/*
   Demo notification only.
   It does not verify actual X activity.
*/

setInterval(
    showXNotice,
    180000
);


/* ==========================================
   INITIALIZE
========================================== */

document.addEventListener(
    "DOMContentLoaded",
    function(){

        updateMessageCounter();

        const savedUser =
            JSON.parse(
                localStorage.getItem(
                    "privateSpotUser"
                ) || "null"
            );


        if(savedUser){

            document.getElementById(
                "welcomeName"
            ).textContent =
                savedUser.name;

        }

    }
);

</script>

</body>
</html>
