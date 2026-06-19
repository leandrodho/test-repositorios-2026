```sql
CREATE DATABASE IF NOT EXISTS `bd_nexus` /*!40100 DEFAULT CHARACTER SET utf8mb4 COLLATE utf8mb4_general_ci */;
USE `bd_nexus`;

CREATE TABLE IF NOT EXISTS `accounts` (
  `id_user` int(11) NOT NULL AUTO_INCREMENT,
  `uuid` char(36) NOT NULL COMMENT 'Identificador único universal para los microservicios',
  `name` varchar(100) NOT NULL,
  `email` varchar(150) NOT NULL,
  `password` varchar(255) NOT NULL,
  `role` enum('user','admin') NOT NULL DEFAULT 'user',
  `status` enum('active','inactive') NOT NULL DEFAULT 'inactive',
  `verification_token` varchar(128) DEFAULT NULL,
  `created_at` timestamp NOT NULL DEFAULT current_timestamp(),
  `updated_at` timestamp NOT NULL DEFAULT current_timestamp() ON UPDATE current_timestamp(),
  PRIMARY KEY (`id_user`),
  UNIQUE KEY `uuid` (`uuid`),
  UNIQUE KEY `email` (`email`)
) ENGINE=InnoDB AUTO_INCREMENT=13 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_unicode_ci;

CREATE TABLE IF NOT EXISTS `inventory` (
  `registro` int(11) NOT NULL,
  `codigo` varchar(100) DEFAULT NULL,
  `titulo` text NOT NULL,
  `autor` varchar(255) DEFAULT NULL,
  `biblioteca` varchar(100) DEFAULT NULL,
  `tipo` varchar(50) DEFAULT NULL,
  `procedencia` varchar(50) DEFAULT NULL,
  `fecha` datetime DEFAULT NULL,
  `estado` varchar(20) DEFAULT 'Disponible',
  PRIMARY KEY (`registro`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

CREATE TABLE IF NOT EXISTS `reserved_books` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_uuid` char(36) NOT NULL COMMENT 'UUID proveniente del auth-service',
  `codigo` varchar(100) NOT NULL,
  `registro` int(11) NOT NULL COMMENT 'Registro del ejemplar físico',
  `estado` varchar(50) DEFAULT 'Pendiente',
  `fecha_reserva` datetime DEFAULT current_timestamp(),
  PRIMARY KEY (`id`),
  UNIQUE KEY `unique_user_reserved` (`user_uuid`,`registro`)
) ENGINE=InnoDB AUTO_INCREMENT=11 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

CREATE TABLE IF NOT EXISTS `saved_books` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_uuid` char(36) NOT NULL COMMENT 'UUID proveniente del auth-service',
  `codigo` varchar(100) NOT NULL COMMENT 'Código del libro general',
  `origen` varchar(50) DEFAULT NULL,
  `titulo` varchar(255) DEFAULT NULL,
  `portada_url` varchar(500) DEFAULT NULL,
  `fecha_guardado` datetime DEFAULT current_timestamp(),
  PRIMARY KEY (`id`),
  UNIQUE KEY `unique_user_saved` (`user_uuid`,`codigo`,`origen`)
) ENGINE=InnoDB AUTO_INCREMENT=19 DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

CREATE TABLE IF NOT EXISTS `collections` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `user_uuid` char(36) NOT NULL COMMENT 'UUID del dueño de la colección',
  `name` varchar(150) NOT NULL,
  `created_at` datetime DEFAULT current_timestamp(),
  PRIMARY KEY (`id`),
  KEY `idx_user_collections` (`user_uuid`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;

CREATE TABLE IF NOT EXISTS `collection_items` (
  `id` int(11) NOT NULL AUTO_INCREMENT,
  `collection_id` int(11) NOT NULL,
  `saved_book_id` int(11) NOT NULL COMMENT 'Apunta al id de saved_books',
  `added_at` datetime DEFAULT current_timestamp(),
  PRIMARY KEY (`id`),
  UNIQUE KEY `unique_collection_book` (`collection_id`,`saved_book_id`),
  KEY `idx_collection_id` (`collection_id`),
  KEY `idx_saved_book_id` (`saved_book_id`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8mb4 COLLATE=utf8mb4_general_ci;
```
