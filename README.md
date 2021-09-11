- 👋 Hi, I’m @Sangeerththan
- 👀 I’m interested in programming, mathematics and biking
- 🌱 I’m currently learning about microservice architecture
- 💞️ I’m looking to collaborate on projects that can help to solve critical issues of people.

<p  align="left"> 📫 You can ping me through... </p>

-[<img align="left" alt="Sangeerththan" height="22px" src="./icons/Gmail.png" />](mailto:sangeerththan.15@cse.mrt.ac.lk)
-[<img align="left" alt="Sangeerththan" height="22px" src="./icons/LinkedIn.png" />](https://www.linkedin.com/in/sangeerththanbalachandran/)
-[<img align="left" alt="Sangeerththan" height="22px" src="./icons/Medium.png" />](https://www.linkedin.com/in/sangeerththanbalachandran/)
-[<img align="left" alt="Sangeerththan" height="22px" src="./icons/StackOverflow.png" />](https://stackoverflow.com/users/9538584/sangeerththan-b)
-[<img align="left" alt="Sangeerththan" height="22px" src="./icons/Twitter.png" />](https://twitter.com/sangeerth20)

## Medium Blogs
![Medium Blogs](https://api.rss2json.com/v1/api.json?rss_url=https://medium.com/feed/@sangeerththanbalachandran)
<scrpipt>
const username = `sangeerththanbalachandran`
const RSSUrl = `https://medium.com/feed/@${username}`;
const RSSConverter = `https://api.rss2json.com/v1/api.json?rss_url=${RSSUrl}`;

const $text = document.querySelector('.text');
const $textList = document.querySelector('.textList');

const getMediumData = async () => {
    
    try {
    const response = await fetch(RSSConverter);
    const data = await response.json();
    console.log(data);
    return data
    } catch(error){
        console.log(error)
    }
};

const getSingleText = async () => {
    const posts = await getMediumData();
    const post = posts.items[1]; // latest text (0 to 9)
    const title = post.title;
    const pubDate = post.pubDate;
    const link = post.link;
    const author = post.author;
    const content = post.content;

    const newText = document.createElement('div');
    newText.className = 'text';
    newText.innerHTML = `<h1>${title}</h1>
    <a href="${link}"><h2>Published ${pubDate} by ${author}</h2></a>
    ${content}`;

    $text.appendChild(newText)
};

const getLatestTextsList = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        const newItem = document.createElement('li');
        const title = post.title;
        const link = post.link;
        const thumbnail = post.thumbnail;

        newItem.innerHTML = `<img src="${thumbnail}" alt=""><a href="${link}"><h3>${title}</h3></a>`;

        $textList.appendChild(newItem)

    }
};

const getMediumTitles = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        console.log(post.title)
    }
};

const getMediumLinks = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        console.log(post.link)
    }
};

const getMediumThumbnails = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        console.log(post.thumbnail)
    }
};

const getMediumPubDates = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        console.log(post.pubDate)
    }
};

const getMediumTexts = async () => {
    const posts = await getMediumData();
    for (let post of posts.items){
        console.log(post.content)
    }
};
getLatestTextsList();
</scrpipt>

## Profile Statistics

<a href="https://github-readme-stats.vercel.app/api?username=Sangeerththan&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&theme=radical">
<img align="center" alt="Sangeerththan's Github Stats" src="https://github-readme-stats.vercel.app/api?username=Sangeerththan&show_icons=true&hide_border=true&count_private=true&include_all_commits=true&theme=radical" /></a>


<a href="https://github-readme-stats.vercel.app/api/top-langs/?username=Sangeerththan&langs_count=10&layout=compact&theme=radical">
  <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Sangeerththan&langs_count=10&layout=compact&theme=radical" />
</a>

<p align=center>                           
  <img align=center  src="https://visitor-badge.laobi.icu/badge?page_id=sangeerththan" alt="Visitors">                     
</p>