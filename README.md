# laravelproject

//Connect this database SQL to run the laravelproject

-- phpMyAdmin SQL Dump
-- version 5.0.1
-- https://www.phpmyadmin.net/
--
-- Host: 127.0.0.1
-- Generation Time: Aug 19, 2020 at 08:26 AM
-- Server version: 10.4.11-MariaDB
-- PHP Version: 7.4.2

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET AUTOCOMMIT = 0;
START TRANSACTION;
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8mb4 */;

--
-- Database: `taskmgnt1`
--

-- --------------------------------------------------------

--
-- Table structure for table `migrations`
--

CREATE TABLE `migrations` (
  `id` int(10) UNSIGNED NOT NULL,
  `migration` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `batch` int(11) NOT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Dumping data for table `migrations`
--

INSERT INTO `migrations` (`id`, `migration`, `batch`) VALUES
(1, '2019_10_23_093311_create_tasks_table', 1);

-- --------------------------------------------------------

--
-- Table structure for table `tasks`
--

CREATE TABLE `tasks` (
  `id` int(10) UNSIGNED NOT NULL,
  `taskname` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `description` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `assigner` varchar(250) COLLATE utf8mb4_unicode_ci NOT NULL,
  `developer` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `complete` enum('No','Yes') COLLATE utf8mb4_unicode_ci NOT NULL DEFAULT 'No',
  `created_at` timestamp NULL DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Dumping data for table `tasks`
--

INSERT INTO `tasks` (`id`, `taskname`, `description`, `assigner`, `developer`, `complete`, `created_at`, `updated_at`) VALUES
(2, 'update', 'taskadd', 'aravinth', 'kayathri', 'No', '2019-11-20 03:37:16', '2020-07-07 11:02:57'),
(3, 'edit task', 'gsgag', 'aravinth', 'amala', 'No', '2019-11-20 03:37:28', '2020-01-17 06:29:49'),
(4, 'asese', 'aa', 'sutha', 'kayathri', 'Yes', '2019-11-21 00:26:02', '2020-02-10 05:11:54'),
(13, 'sss', 'aad', 'sinthu', 'kayathri', 'Yes', '2019-12-12 02:14:34', '2020-02-10 04:39:40'),
(26, 'newtask', 'aa', 'sutha', 'kayathri', 'Yes', '2019-12-20 04:47:01', '2020-02-10 04:53:13'),
(38, 'aaa', 'aa', 'rammya', 'amala', 'No', '2020-01-24 05:31:43', '2020-01-24 05:31:43'),
(39, 'task2', 'des2', 'sinthu', 'kayathri', 'No', '2020-01-30 23:56:09', '2020-02-09 08:47:19'),
(40, 'tqsg', 'dfde', 'aravinth', 'kayathri', 'Yes', '2020-01-30 23:56:23', '2020-02-10 05:11:37'),
(41, 'rereee', 'ererrerer', 'sinthu', 'kayathri', 'Yes', '2020-01-30 23:56:52', '2020-07-07 10:56:48'),
(42, 'task3', 'sesese', 'sathu', 'kayathri', 'Yes', '2020-01-31 05:53:14', '2020-02-10 05:11:26'),
(43, 'addd', 'adddname', 'sathu', 'Anitha', 'No', '2020-01-31 05:53:38', '2020-01-31 05:53:38'),
(44, 'delete', 'grtreyy', 'aravinth', 'kayathri', 'Yes', '2020-01-31 05:53:59', '2020-02-10 05:01:56');

-- --------------------------------------------------------

--
-- Table structure for table `users`
--

CREATE TABLE `users` (
  `id` int(10) UNSIGNED NOT NULL,
  `name` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `email` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `password` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `gender` enum('female','male') COLLATE utf8mb4_unicode_ci NOT NULL,
  `role` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `address` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `phoneno` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `status` varchar(255) COLLATE utf8mb4_unicode_ci NOT NULL,
  `remember_token` varchar(100) COLLATE utf8mb4_unicode_ci DEFAULT NULL,
  `created_at` timestamp NULL DEFAULT NULL,
  `updated_at` timestamp NULL DEFAULT NULL
) ENGINE=MyISAM DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

--
-- Dumping data for table `users`
--

INSERT INTO `users` (`id`, `name`, `email`, `password`, `gender`, `role`, `address`, `phoneno`, `status`, `remember_token`, `created_at`, `updated_at`) VALUES
(47, 'sinthu', 'sithu@aa.aa', '$2y$10$rMGBvwYWrefmk/oZMhUK4OTQFj8OZTUeEK58MZfGGLyPim3ztclA.', 'female', 'Admin', 'trinco', '0749798968', 'Active', NULL, '2020-07-07 11:10:56', '2020-07-07 11:10:56'),
(46, 'aravinth', 'ar@aa.aa', '$2y$10$gFpp9MkMhMoJ0p1Aa4H94uu.wnCp3jJN9oYR9DAgzErrlDNPpscoi', 'male', 'Admin', 'jaffna', '0787878787', 'Active', NULL, '2020-07-07 11:10:12', '2020-07-07 11:10:12'),
(45, 'abi', 'abi@gmail.com', '$2y$10$tDTV/8XUscnQc5UjRut0i.qQWlD68gEW6072.fQOEiqX6UdHXw8Ou', 'male', 'User', 'colombo', '0242252522', 'Active', NULL, '2020-07-07 11:07:29', '2020-07-07 11:07:29'),
(33, 'kayathri', 'kaya@aa.aa', '$2y$10$pcj7GYnfImhLk66nmQNN8ODp/G4FaZFCC1CYsbb/wka9X3P7YVbBG', 'female', 'User', 'colombo', '0454534876', 'Active', NULL, '2019-12-19 05:28:56', '2020-07-07 10:56:41'),
(37, 'sutha', 'sutha@aa.aa', '$2y$10$itJmRLrVeYC0QfSBIHQghOs9GdJIy/kSL3U1aBMYwuD1.UCdgWN9u', 'female', 'Admin', 'trinco', '0454534876', 'Active', NULL, '2020-01-09 05:04:13', '2020-01-17 06:11:20');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `migrations`
--
ALTER TABLE `migrations`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `tasks`
--
ALTER TABLE `tasks`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `users`
--
ALTER TABLE `users`
  ADD PRIMARY KEY (`id`);

--
-- AUTO_INCREMENT for dumped tables
--

--
-- AUTO_INCREMENT for table `migrations`
--
ALTER TABLE `migrations`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=2;

--
-- AUTO_INCREMENT for table `tasks`
--
ALTER TABLE `tasks`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=45;

--
-- AUTO_INCREMENT for table `users`
--
ALTER TABLE `users`
  MODIFY `id` int(10) UNSIGNED NOT NULL AUTO_INCREMENT, AUTO_INCREMENT=48;
COMMIT;

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
