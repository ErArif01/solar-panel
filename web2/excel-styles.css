document.addEventListener('DOMContentLoaded', function () {
    const appContainer = document.getElementById('app');
    const articlesContainer = document.getElementById('articles-container');
    const menuItems = document.querySelectorAll('nav ul li a');
    const subscribeButton = document.getElementById('subscribe');
    const newsForm = document.getElementById('news-form');

    // Sample data for demonstration purposes
    const articles = [
        { title: 'Solar Energy Advancements', content: 'Lorem ipsum dolor sit amet, consectetur adipiscing elit.', videoUrl: 'https://www.example.com/solar-video' },
        { title: 'New Solar Technologies', content: 'Pellentesque habitant morbi tristique senectus et netus et malesuada fames ac turpis egestas.', videoUrl: 'https://www.example.com/new-solar-tech' },
        // Add more articles as needed
    ];

    function renderArticles(category) {
        articlesContainer.innerHTML = '';
        const filteredArticles = category ? articles.filter(article => article.category === category) : articles;
        filteredArticles.forEach(article => {
            const articleElement = document.createElement('article');
            articleElement.innerHTML = `<h2>${article.title}</h2><p>${article.content}</p>`;
            articlesContainer.appendChild(articleElement);
        });
    }

    function handleMenuItemClick(event) {
        event.preventDefault();
        const selectedCategory = event.target.id;
        renderArticles(selectedCategory);
    }

    function handleSubscribeButtonClick() {
        // Add your subscribe functionality here
        alert('Thank you for subscribing!');
    }

    function handleNewsFormSubmit(event) {
        event.preventDefault();
        const title = document.getElementById('title').value;
        const content = document.getElementById('content').value;
        const videoUrl = document.getElementById('video-url').value;

        // Add the new post to the articles array
        articles.push({ title, content, videoUrl });

        // Re-render the articles
        renderArticles();

        // Clear the form
        newsForm.reset();

        // Display uploaded data
        displayUploadedData();
    }

    function displayUploadedData() {
        const dataTable = document.getElementById('data-table').getElementsByTagName('tbody')[0];

        // Clear existing table rows
        dataTable.innerHTML = '';

        // Iterate over articles and add rows to the table
        articles.forEach(article => {
            const row = dataTable.insertRow();
            const cell1 = row.insertCell(0);
            const cell2 = row.insertCell(1);
            const cell3 = row.insertCell(2);
            cell1.textContent = article.title;
            cell2.textContent = article.content;
            cell3.textContent = article.videoUrl;
        });
    }

    menuItems.forEach(item => item.addEventListener('click', handleMenuItemClick));
    subscribeButton.addEventListener('click', handleSubscribeButtonClick);
    newsForm.addEventListener('submit', handleNewsFormSubmit);

    renderArticles(); // Initially render all articles
});
