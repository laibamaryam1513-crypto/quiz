{
  "name": "qa-application",
  "version": "1.0.0",
  "description": "A full-stack Question & Answer application",
  "main": "server.js",
  "scripts": {
    "start": "node server.js",
    "dev": "nodemon server.js"
  },
  "keywords": ["qa", "questions", "answers", "full-stack"],
  "author": "",
  "license": "MIT",
  "dependencies": {
    "express": "^4.18.2",
    "cors": "^2.8.5"
  },
  "devDependencies": {
    "nodemon": "^3.0.1"
  }
}
{
  "tags": [
    {
      "id": 1,
      "name": "javascript",
      "description": "Questions related to JavaScript programming",
      "color": "#F7DF1E"
    },
    {
      "id": 2,
      "name": "react",
      "description": "Questions about React library",
      "color": "#61DAFB"
    },
    {
      "id": 3,
      "name": "node.js",
      "description": "Questions about Node.js backend",
      "color": "#68A063"
    },
    {
      "id": 4,
      "name": "html-css",
      "description": "Questions about HTML and CSS",
      "color": "#E34C26"
    },
    {
      "id": 5,
      "name": "database",
      "description": "Questions about databases",
      "color": "#336791"
    }
  ],
  "questions": [
    {
      "id": 1,
      "title": "How do I center a div in CSS?",
      "description": "I'm trying to center a div element both horizontally and vertically on the page. What are the best approaches?",
      "author": "John Doe",
      "tags": [4],
      "votes": 45,
      "views": 1250,
      "createdAt": "2024-01-15T10:30:00Z",
      "updatedAt": "2024-01-20T14:22:00Z"
    },
    {
      "id": 2,
      "title": "What is the difference between let and const in JavaScript?",
      "description": "I'm confused about when to use let vs const in modern JavaScript. Can someone explain the differences?",
      "author": "Jane Smith",
      "tags": [1],
      "votes": 87,
      "views": 2340,
      "createdAt": "2024-01-10T08:15:00Z",
      "updatedAt": "2024-01-18T11:05:00Z"
    },
    {
      "id": 3,
      "title": "How to manage state in React hooks?",
      "description": "I'm new to React hooks and want to understand how to properly manage component state using useState and useEffect.",
      "author": "Mike Johnson",
      "tags": [2],
      "votes": 92,
      "views": 3100,
      "createdAt": "2024-01-05T16:45:00Z",
      "updatedAt": "2024-01-19T09:30:00Z"
    },
    {
      "id": 4,
      "title": "Best practices for Express middleware",
      "description": "What are the best practices for creating and organizing middleware in Express applications?",
      "author": "Sarah Wilson",
      "tags": [3],
      "votes": 56,
      "views": 1890,
      "createdAt": "2024-01-12T12:20:00Z",
      "updatedAt": "2024-01-17T15:10:00Z"
    },
    {
      "id": 5,
      "title": "How to optimize database queries?",
      "description": "I have a slow application and I think the issue is with my database queries. How can I optimize them?",
      "author": "Robert Brown",
      "tags": [5, 3],
      "votes": 73,
      "views": 2050,
      "createdAt": "2024-01-08T14:00:00Z",
      "updatedAt": "2024-01-16T10:45:00Z"
    }
  ],
  "answers": [
    {
      "id": 1,
      "questionId": 1,
      "author": "Alex Turner",
      "content": "You can use Flexbox to center a div:\n\n```css\n.container {\n  display: flex;\n  justify-content: center;\n  align-items: center;\n  height: 100vh;\n}\n```\n\nAlternatively, you can use CSS Grid:\n\n```css\n.container {\n  display: grid;\n  place-items: center;\n  height: 100vh;\n}\n```",
      "votes": 124,
      "isAccepted": true,
      "createdAt": "2024-01-15T11:45:00Z",
      "updatedAt": "2024-01-15T11:45:00Z"
    },
    {
      "id": 2,
      "questionId": 2,
      "author": "Emma Davis",
      "content": "The main differences are:\n\n**let**: Block-scoped, can be reassigned, cannot be redeclared in the same scope.\n**const**: Block-scoped, cannot be reassigned, cannot be redeclared.\n\nUse `const` by default, `let` when you need to reassign, and avoid `var` in modern JavaScript.",
      "votes": 156,
      "isAccepted": true,
      "createdAt": "2024-01-10T09:20:00Z",
      "updatedAt": "2024-01-10T09:20:00Z"
    },
    {
      "id": 3,
      "questionId": 2,
      "author": "Chris Martin",
      "content": "Here's a practical example:\n\n```javascript\nconst [count, setCount] = useState(0);\n\nuseEffect(() => {\n  console.log('Count changed:', count);\n}, [count]);\n```\n\nThe dependency array tells React when to re-run the effect.",
      "votes": 89,
      "isAccepted": false,
      "createdAt": "2024-01-10T13:30:00Z",
      "updatedAt": "2024-01-10T13:30:00Z"
    },
    {
      "id": 4,
      "questionId": 3,
      "author": "Lisa Wong",
      "content": "In React hooks, `useState` manages state and `useEffect` handles side effects. Here's a pattern:\n\n```javascript\nfunction MyComponent() {\n  const [data, setData] = useState(null);\n  \n  useEffect(() => {\n    // Fetch data\n    fetchData().then(setData);\n  }, []); // Empty dependency array = run once on mount\n  \n  return <div>{data}</div>;\n}\n```",
      "votes": 142,
      "isAccepted": true,
      "createdAt": "2024-01-05T17:15:00Z",
      "updatedAt": "2024-01-05T17:15:00Z"
    },
    {
      "id": 5,
      "questionId": 4,
      "author": "David Lee",
      "content": "Always validate input before processing. Use middleware in the right order:\n\n1. Error handling middleware should be last\n2. Use `app.use()` for global middleware\n3. Use `router.use()` for route-specific middleware\n4. Return responses appropriately",
      "votes": 98,
      "isAccepted": true,
      "createdAt": "2024-01-12T13:45:00Z",
      "updatedAt": "2024-01-12T13:45:00Z"
    }
  ]
}

const express = require('express');
const cors = require('cors');
const path = require('path');
const fs = require('fs');

const app = express();
const PORT = process.env.PORT || 3000;

// Middleware
app.use(cors());
app.use(express.json());
app.use(express.static(path.join(__dirname, 'public')));

// Load mock data
const mockDataPath = path.join(__dirname, 'data', 'mock-data.json');
const mockData = JSON.parse(fs.readFileSync(mockDataPath, 'utf8'));

// Routes

// Get all questions
app.get('/api/questions', (req, res) => {
  try {
    res.json(mockData.questions);
  } catch (error) {
    res.status(500).json({ error: 'Failed to fetch questions' });
  }
});

// Get single question with answers
app.get('/api/questions/:id', (req, res) => {
  try {
    const question = mockData.questions.find(q => q.id === parseInt(req.params.id));
    if (!question) {
      return res.status(404).json({ error: 'Question not found' });
    }
    
    const answers = mockData.answers.filter(a => a.questionId === question.id);
    res.json({ ...question, answers });
  } catch (error) {
    res.status(500).json({ error: 'Failed to fetch question' });
  }
});

// Get all tags
app.get('/api/tags', (req, res) => {
  try {
    res.json(mockData.tags);
  } catch (error) {
    res.status(500).json({ error: 'Failed to fetch tags' });
  }
});

// Get questions by tag
app.get('/api/tags/:tagId/questions', (req, res) => {
  try {
    const tagId = parseInt(req.params.tagId);
    const questions = mockData.questions.filter(q => q.tags.includes(tagId));
    res.json(questions);
  } catch (error) {
    res.status(500).json({ error: 'Failed to fetch questions by tag' });
  }
});

// Get all answers
app.get('/api/answers', (req, res) => {
  try {
    res.json(mockData.answers);
  } catch (error) {
    res.status(500).json({ error: 'Failed to fetch answers' });
  }
});

// Search questions
app.get('/api/search', (req, res) => {
  try {
    const query = req.query.q?.toLowerCase() || '';
    if (!query) {
      return res.json([]);
    }

    const results = mockData.questions.filter(q =>
      q.title.toLowerCase().includes(query) ||
      q.description.toLowerCase().includes(query)
    );
    res.json(results);
  } catch (error) {
    res.status(500).json({ error: 'Failed to search questions' });
  }
});

// Health check
app.get('/api/health', (req, res) => {
  res.json({ status: 'Server is running' });
});

// Serve index.html for all other routes (SPA)
app.get('*', (req, res) => {
  res.sendFile(path.join(__dirname, 'public', 'index.html'));
});

// Start server
app.listen(PORT, () => {
  console.log(`Server running at http://localhost:${PORT}`);
  console.log('API endpoints available at http://localhost:' + PORT + '/api/');
});

