```javascript
'use client';

import { useState, useEffect } from 'react';

import SearchBar from "./components/SearchBar";

import StockDashboard from "./components/StockDashboard";

  

export default function Home() {

  const [query, setQuery] = useState("");

  const [darkMode, setDarkMode] = useState();

  

  const handleSearch = (searchQuery) => {

    setQuery(searchQuery);

  };

  

  const toggleDarkMode = () => {

    const newMode = !darkMode;

    setDarkMode(newMode);

    if (newMode) {

      document.body.classList.add("dark");

      localStorage.setItem("darkMode", "true");

    } else {

      document.body.classList.remove("dark");

      localStorage.setItem("darkMode", "false");

    }

  };

  
  

  useEffect(() => {

    const storedDarkMode = localStorage.getItem("darkMode");

    if (storedDarkMode) {

      setDarkMode(storedDarkMode === "true");

    }

  }, []);

  

  useEffect(() => {

    if (darkMode) {

      document.body.classList.add('dark');

    } else {

      document.body.classList.remove('dark');

    }

  }, [darkMode]);

  
  
  

  return (

    <div className="relative">

      <header className="fixed top-0 left-0 w-full bg-gray-200 dark:bg-gray-800 z-50 flex justify-between items-center p-4 shadow-md">

        <img src="/logo/logo.png" alt="Company Logo" className="w-24 h-24" />

        <SearchBar onSearch={handleSearch} darkMode={darkMode} />

        <button onClick={toggleDarkMode} className="text-3xl">

          {darkMode ? '☀️' : '🌙'}

        </button>

      </header>

      <div className="pt-32">

        <StockDashboard query={query} />

      </div>

    </div>

  );

}
```

1. 'use client' 제시어를 선언해서 해당 [[컴포넌트]]가 [[클라이언트 컴포넌트]]임을 명시함.
2. [[import]] 문법을 통해서 필요 모듈과 다른 컴포넌트를 가져옴.
3. 함수형 컴포넌트 [[Home]]을 말들고 [[useState]] 를 사용
4. [[Event Handler]] 정의
5. [[useEffect]] 정의
6. [[JSX]]작성
7. 헤더작성
	1. 로고
	2. [[SearchBar]] [[컴포넌트 재사용]]
	3. 라이트/다크 모드 버튼
8. 바디에 해당하는 [[StockDashboard]] 컴포넌트 작성