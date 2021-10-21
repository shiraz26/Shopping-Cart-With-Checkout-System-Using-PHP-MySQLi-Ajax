# Shopping-Cart-With-Checkout-System-Using-PHP-MySQLi-Ajax
Shopping-Cart-PHP-AJAX-MYSQLI-
1.  Creating Database & Table

First of all, We'll create a Database and Tables for this project, so for this just open your phpmyadmin in the browser and create a new database with the name "cart_system". After creating the database We'll now create some tables into it, so don't worry I'm giving you the SQL file you just have to import this file into the created database. You can write the code over here for SQL file . 
make Database by the name of cart_system
- Database: `cart_system`
--

-- --------------------------------------------------------

--
-- Table structure for table `cart`
--

CREATE TABLE `cart` (
  `id` int(11) NOT NULL,
  `product_name` varchar(100) NOT NULL,
  `product_price` varchar(50) NOT NULL,
  `product_image` varchar(255) NOT NULL,
  `qty` int(10) NOT NULL,
  `total_price` varchar(100) NOT NULL,
  `product_code` varchar(10) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Table structure for table `orders`
--

CREATE TABLE `orders` (
  `id` int(11) NOT NULL,
  `name` varchar(100) NOT NULL,
  `email` varchar(100) NOT NULL,
  `phone` varchar(20) NOT NULL,
  `address` varchar(255) NOT NULL,
  `pmode` varchar(50) NOT NULL,
  `products` varchar(255) NOT NULL,
  `amount_paid` varchar(100) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

-- --------------------------------------------------------

--
-- Table structure for table `product`
--

CREATE TABLE `product` (
  `id` int(11) NOT NULL,
  `product_name` varchar(255) NOT NULL,
  `product_price` varchar(100) NOT NULL,
  `product_qty` int(11) NOT NULL DEFAULT 1,
  `product_image` varchar(255) NOT NULL,
  `product_code` varchar(50) NOT NULL
) ENGINE=InnoDB DEFAULT CHARSET=latin1;

--
-- Dumping data for table `product`
--

INSERT INTO `product` (`id`, `product_name`, `product_price`, `product_qty`, `product_image`, `product_code`) VALUES
(1, 'Apple iPhone X', '90000', 1, 'image/iphone_x.jpg', 'p1000'),
(2, 'Huawei 10 Pro', '75000', 1, 'image/huawei_mate10_pro.jpg', 'p1001'),
(3, 'LG v30', '65000', 1, 'image/lg_v30.jpg', 'p1002'),
(4, 'MI Note 5 Pro', '15000', 1, 'image/mi_note_5_pro.jpg', 'p1003'),
(5, 'Nokia 7 Plus', '25000', 1, 'image/nokia_7_plus.jpg', 'p1004'),
(6, 'One Plus 6', '35000', 1, 'image/one_plus_6.jpg', 'p1005'),
(7, 'Zenfone Max Pro', '15000', 1, 'image/zenfone_m1.jpg', 'p1006'),
(9, 'Samsung A50', '25000', 1, 'image/samsung_a50.jpg', 'p1007');

--
-- Indexes for dumped tables
--

--
-- Indexes for table `cart`
--
ALTER TABLE `cart`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `orders`
--
ALTER TABLE `orders`
  ADD PRIMARY KEY (`id`);

--
-- Indexes for table `product`
--
ALTER TABLE `product`
  ADD PRIMARY KEY (`id`),
 
