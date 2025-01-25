




# 👋 Hi, I'm Abhijeet Kumar Singh

### 🌐 Full-Stack Developer | Open Source Contributor

![Typing SVG](https://readme-typing-svg.herokuapp.com?font=Roboto&color=%2336BCF7&size=24&center=true&vCenter=true&width=450&lines=Welcome+to+my+GitHub!+I'm+Abhijeet)

I'm a dedicated developer who strongly focuses on building impactful and scalable software solutions.

### 💻 Tech Stack & Expertise

- **Languages:** ![TypeScript](https://img.shields.io/badge/-TypeScript-007ACC?logo=typescript&logoColor=white) ![JavaScript](https://img.shields.io/badge/-JavaScript-F7DF1E?logo=javascript&logoColor=black) ![Java](https://img.shields.io/badge/-Java-007396?logo=java&logoColor=white)
- **Frameworks & Libraries:** ![NestJS](https://img.shields.io/badge/-NestJS-E0234E?logo=nestjs&logoColor=white) ![React](https://img.shields.io/badge/-React-61DAFB?logo=react&logoColor=white) ![Express.js](https://img.shields.io/badge/-Express.js-000000?logo=express&logoColor=white) ![Spring](https://img.shields.io/badge/-Spring-6DB33F?logo=spring&logoColor=white) ![Next.js](https://img.shields.io/badge/-Next.js-000000?logo=next.js&logoColor=white)
- **Databases:** ![MySQL](https://img.shields.io/badge/-MySQL-4479A1?logo=mysql&logoColor=white) ![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-4169E1?logo=postgresql&logoColor=white) ![MongoDB](https://img.shields.io/badge/-MongoDB-47A248?logo=mongodb&logoColor=white)
- **DevOps & Tools:** ![Docker](https://img.shields.io/badge/-Docker-2496ED?logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/-Kubernetes-326CE5?logo=kubernetes&logoColor=white) ![AWS](https://img.shields.io/badge/-AWS-232F3E?logo=amazon-aws&logoColor=white) ![Git](https://img.shields.io/badge/-Git-F05032?logo=git&logoColor=white)
- **Focus Areas:** Full-Stack Development, Open Source, System Design

### 👨‍💻 Work :-

- **ZenStreet.ai:** Developing the backend for a SaaS platform using TypeScript and Nest.js, focusing on creating reliable and efficient systems.
- **Open Source:** Contributing to projects like WebPack and Neutralinojs.
- **Hackathons:** Continuously refining my skills by generating and executing innovative ideas in competitive environments.

### 🌱 Beyond the Code

When I'm not coding, I’m likely engaged in MMA 🥋 or playing football ⚽. My interest in complex systems extends from software engineering to understanding intricate natural systems.

### 📫 Let's Connect

- **Email:** [abhijeet6419@gmail.com](mailto:abhijeet6419@gmail.com)
- **LinkedIn:** [![LinkedIn](https://img.shields.io/badge/-LinkedIn-0077B5?logo=linkedin&logoColor=white)](https://www.linkedin.com/in/abhijeet-kumar-singh-softwaredeveloper/)


I'm always open to connecting with professionals and like-minded individuals. Let's collaborate and create something extraordinary together!

import React, { useState, useEffect } from 'react';
import { 
  GitHubLogoIcon, 
  CodeIcon, 
  RocketIcon, 
  EyeOpenIcon, 
  CommitIcon 
} from '@radix-ui/react-icons';

const GitHubProfileStats = () => {
  const [profileStats, setProfileStats] = useState({
    totalVisitors: 0,
    privateRepoPushes: 0,
    openSourceContributions: 0,
    dailyCommits: 0
  });

  // Simulated data fetch (in a real implementation, you'd use GitHub API)
  useEffect(() => {
    // Mock data generation
    const generateMockStats = () => {
      return {
        totalVisitors: Math.floor(Math.random() * 10000),
        privateRepoPushes: Math.floor(Math.random() * 500),
        openSourceContributions: Math.floor(Math.random() * 200),
        dailyCommits: Math.floor(Math.random() * 50)
      };
    };

    setProfileStats(generateMockStats());
  }, []);

  return (
    <div className="grid grid-cols-2 gap-4 p-4 bg-gray-50 rounded-lg shadow-md">
      <div className="flex items-center bg-white p-3 rounded-lg shadow">
        <EyeOpenIcon className="w-8 h-8 text-blue-500 mr-3" />
        <div>
          <p className="text-gray-600">Profile Visitors</p>
          <h3 className="text-2xl font-bold text-blue-600">
            {profileStats.totalVisitors.toLocaleString()}
          </h3>
        </div>
      </div>

      <div className="flex items-center bg-white p-3 rounded-lg shadow">
        <CodeIcon className="w-8 h-8 text-green-500 mr-3" />
        <div>
          <p className="text-gray-600">Private Repo Pushes</p>
          <h3 className="text-2xl font-bold text-green-600">
            {profileStats.privateRepoPushes.toLocaleString()}
          </h3>
        </div>
      </div>

      <div className="flex items-center bg-white p-3 rounded-lg shadow">
        <RocketIcon className="w-8 h-8 text-purple-500 mr-3" />
        <div>
          <p className="text-gray-600">Open Source Contributions</p>
          <h3 className="text-2xl font-bold text-purple-600">
            {profileStats.openSourceContributions.toLocaleString()}
          </h3>
        </div>
      </div>

      <div className="flex items-center bg-white p-3 rounded-lg shadow">
        <CommitIcon className="w-8 h-8 text-red-500 mr-3" />
        <div>
          <p className="text-gray-600">Daily Commits</p>
          <h3 className="text-2xl font-bold text-red-600">
            {profileStats.dailyCommits.toLocaleString()}
          </h3>
        </div>
      </div>

      <div className="col-span-2 mt-4 text-center text-xs text-gray-500">
        * Statistics are randomly generated for demonstration
      </div>
    </div>
  );
};

export default GitHubProfileStats;
