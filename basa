-- phpMyAdmin SQL Dump
-- version 5.1.0
-- https://www.phpmyadmin.net/
--
-- Хост: 127.0.0.1:3306
-- Время создания: Апр 23 2022 г., 09:48
-- Версия сервера: 8.0.24
-- Версия PHP: 8.0.8

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- База данных: `children_entertainment`
--

-- --------------------------------------------------------

--
-- Структура таблицы `entertainers`
--

CREATE TABLE `entertainers` (
  `ID` int NOT NULL COMMENT 'Идентификатор',
  `surname` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Фамилия',
  `name` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Имя',
  `patronymic` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Отчество',
  `passport` varchar(150) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Паспортные данные',
  `contact` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT 'Контактные данные',
  `birthday` date NOT NULL COMMENT 'Дата рождения',
  `address` varchar(100) DEFAULT NULL COMMENT 'Адрес',
  `education` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `specialization` varchar(50) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `enabled` tinyint(1) NOT NULL DEFAULT '1' COMMENT 'Включена/Выключена',
  `createddate` datetime DEFAULT NULL COMMENT 'Дата/Время создания',
  `author` int DEFAULT NULL COMMENT 'Автор',
  `editdate` datetime DEFAULT NULL COMMENT 'Дата/Время изменения',
  `editor` int DEFAULT NULL COMMENT 'Кто изменил',
  `disabledate` datetime DEFAULT NULL COMMENT 'Дата/Время выключения',
  `disabler` int DEFAULT NULL COMMENT 'Кто включил'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

-- --------------------------------------------------------

--
-- Структура таблицы `events`
--

CREATE TABLE `events` (
  `ID` int NOT NULL COMMENT 'Идентификатор',
  `surname` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Фамилия',
  `name` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Имя',
  `patronymic` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Отчество',
  `contact` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT 'Контактные данные',
  `childcount` int NOT NULL,
  `childage` varchar(5) CHARACTER SET utf8mb4 COLLATE utf8mb4_0900_ai_ci NOT NULL,
  `startdate` datetime NOT NULL,
  `enddate` datetime NOT NULL,
  `entertainer` int NOT NULL,
  `cashier` int NOT NULL,
  `enabled` tinyint(1) NOT NULL DEFAULT '1' COMMENT 'Включена/Выключена',
  `createddate` datetime DEFAULT NULL COMMENT 'Дата/Время создания',
  `author` int DEFAULT NULL COMMENT 'Автор',
  `editdate` datetime DEFAULT NULL COMMENT 'Дата/Время изменения',
  `editor` int DEFAULT NULL COMMENT 'Кто изменил',
  `disabledate` datetime DEFAULT NULL COMMENT 'Дата/Время выключения',
  `disabler` int DEFAULT NULL COMMENT 'Кто включил'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

-- --------------------------------------------------------

--
-- Структура таблицы `users`
--

CREATE TABLE `users` (
  `ID` int NOT NULL COMMENT 'Идентификатор',
  `role` set('Руководитель','Бухгалтер','Кассир') CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL DEFAULT 'Кассир' COMMENT 'Должность',
  `surname` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Фамилия',
  `name` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Имя',
  `patronymic` varchar(25) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Отчество',
  `login` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Логин',
  `password` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Пароль',
  `passport` varchar(150) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci NOT NULL COMMENT 'Паспортные данные',
  `contact` varchar(100) CHARACTER SET utf8mb4 COLLATE utf8mb4_unicode_ci DEFAULT NULL COMMENT 'Контактные данные',
  `birthday` date NOT NULL COMMENT 'Дата рождения',
  `address` varchar(100) DEFAULT NULL COMMENT 'Адрес',
  `isActive` tinyint(1) NOT NULL DEFAULT '0' COMMENT 'Активен в данный момент',
  `lastAction` datetime DEFAULT NULL COMMENT 'Время последнего действия',
  `enabled` tinyint(1) NOT NULL DEFAULT '1' COMMENT 'Включена/Выключена',
  `createddate` datetime DEFAULT NULL COMMENT 'Дата/Время создания',
  `author` int DEFAULT NULL COMMENT 'Автор',
  `editdate` datetime DEFAULT NULL COMMENT 'Дата/Время изменения',
  `editor` int DEFAULT NULL COMMENT 'Кто изменил',
  `disabledate` datetime DEFAULT NULL COMMENT 'Дата/Время выключения',
  `disabler` int DEFAULT NULL COMMENT 'Кто включил'
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_0900_ai_ci;

--
-- Индексы сохранённых таблиц
--

--
-- Индексы таблицы `entertainers`
--
ALTER TABLE `entertainers`
  ADD PRIMARY KEY (`ID`),
  ADD UNIQUE KEY `author` (`author`),
  ADD UNIQUE KEY `editor` (`editor`);

--
-- Индексы таблицы `events`
--
ALTER TABLE `events`
  ADD PRIMARY KEY (`ID`),
  ADD UNIQUE KEY `entertainer` (`entertainer`),
  ADD UNIQUE KEY `cashier` (`cashier`),
  ADD UNIQUE KEY `author` (`author`),
  ADD UNIQUE KEY `editor` (`editor`),
  ADD UNIQUE KEY `disabler` (`disabler`);

--
-- Индексы таблицы `users`
--
ALTER TABLE `users`
  ADD PRIMARY KEY (`ID`) USING BTREE,
  ADD UNIQUE KEY `login` (`login`),
  ADD UNIQUE KEY `author` (`author`),
  ADD UNIQUE KEY `editdate` (`editdate`),
  ADD UNIQUE KEY `disabler` (`disabler`);

--
-- AUTO_INCREMENT для сохранённых таблиц
--

--
-- AUTO_INCREMENT для таблицы `users`
--
ALTER TABLE `users`
  MODIFY `ID` int NOT NULL AUTO_INCREMENT COMMENT 'Идентификатор';
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
