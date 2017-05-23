# ProjeroPedro
Esse projeto visa a livramento da AVF
-- phpMyAdmin SQL Dump
-- version 4.1.4
-- http://www.phpmyadmin.net
--
-- Host: 127.0.0.1
-- Generation Time: 22-Maio-2017 às 20:09
-- Versão do servidor: 5.6.15-log
-- PHP Version: 5.4.24

SET SQL_MODE = "NO_AUTO_VALUE_ON_ZERO";
SET time_zone = "+00:00";


/*!40101 SET @OLD_CHARACTER_SET_CLIENT=@@CHARACTER_SET_CLIENT */;
/*!40101 SET @OLD_CHARACTER_SET_RESULTS=@@CHARACTER_SET_RESULTS */;
/*!40101 SET @OLD_COLLATION_CONNECTION=@@COLLATION_CONNECTION */;
/*!40101 SET NAMES utf8 */;

--
-- Database: `escola`
--

-- --------------------------------------------------------

--
-- Estrutura da tabela `aluno`
--

CREATE TABLE IF NOT EXISTS `aluno` (
  `idAluno` int(11) NOT NULL AUTO_INCREMENT,
  `nomeAluno` varchar(250) NOT NULL,
  `matriculaAluno` double NOT NULL,
  `Contato_idContato` int(11) NOT NULL,
  `Endereco_idEndereco` int(11) NOT NULL,
  `Responsavel_idResponsavel` int(11) NOT NULL,
  PRIMARY KEY (`idAluno`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=11 ;

--
-- Extraindo dados da tabela `aluno`
--

INSERT INTO `aluno` (`idAluno`, `nomeAluno`, `matriculaAluno`, `Contato_idContato`, `Endereco_idEndereco`, `Responsavel_idResponsavel`) VALUES
(1, 'sada', 22, 17, 11, 4),
(2, 'dfsfs', 453, 19, 12, 5),
(4, 'Valdcleison', 11111, 36, 28, 7),
(5, 'val', 1111111, 40, 31, 8),
(10, 'Val', 123456, 68, 59, 22);

-- --------------------------------------------------------

--
-- Estrutura da tabela `contato`
--

CREATE TABLE IF NOT EXISTS `contato` (
  `idContato` int(11) NOT NULL AUTO_INCREMENT,
  `fone` varchar(20) NOT NULL,
  `email` varchar(200) DEFAULT NULL,
  PRIMARY KEY (`idContato`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=70 ;

--
-- Extraindo dados da tabela `contato`
--

INSERT INTO `contato` (`idContato`, `fone`, `email`) VALUES
(60, '(56) 5465-4654', 'gcgfhg'),
(61, '(65) 4646-5464', 'rfhg'),
(62, '(87) 6876-8768', 'ggjh'),
(63, '(78) 6876-8768', 'hjg'),
(64, '(76) 8768-7687', 'ghjhgjh'),
(65, '(76) 8687-6876', 'gfhgfh'),
(66, '(65) 7657-6576', 'hgjhg'),
(67, '(65) 7576-5765', 'fhgf'),
(68, '(22) 2222-2222', 'fffff'),
(69, '(22) 2222-2222', 'sss');

-- --------------------------------------------------------

--
-- Estrutura da tabela `endereco`
--

CREATE TABLE IF NOT EXISTS `endereco` (
  `idEndereco` int(11) NOT NULL AUTO_INCREMENT,
  `cidade` varchar(50) NOT NULL,
  `bairro` varchar(50) NOT NULL,
  `rua` varchar(150) NOT NULL,
  `numero` int(11) NOT NULL,
  `uf` varchar(2) NOT NULL,
  PRIMARY KEY (`idEndereco`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=61 ;

--
-- Extraindo dados da tabela `endereco`
--

INSERT INTO `endereco` (`idEndereco`, `cidade`, `bairro`, `rua`, `numero`, `uf`) VALUES
(1, 'gjhbjhb', 'hbjb', 'bbbbb', 7876, 'hh'),
(2, 'bcvbvcbc', 'dtdtd', 'tdtt', 54, 'jj'),
(3, 'bcvbvcbc', 'cbcvbcvb', 'fgdgfd', 43, 'cv'),
(4, 'bcvbvcbc', 'dtdtd', 'tdtt', 54, 'jj'),
(5, 'bcvbvcbc', 'cbcvbcvb', 'fgdgfd', 43, 'cv'),
(6, 'gvhvhv', 'hbjhbjb', 'bjhbjh', 76, 'bh'),
(7, 'gvhvhv', 'ghvhv', 'gvjbnv', 87, 'ff'),
(8, 'chcgcbv', 'vcbcb', 'gfhfh', 657, 'gg'),
(9, 'chcgcbv', 'vcbcb', 'gfhfh', 657, 'gg'),
(10, 'xxxx', 'xxx', 'ccc', 33, 'xx'),
(11, 'sss', 's', 'sss', 2, 'ss'),
(12, 'gvhvghvh', 'vghvh', 'hvhgv', 33, 'vg'),
(13, 'aaaaaaaaaaa', 'ssss', 'ssssssssss', 22, 'ss'),
(14, 'aaaaaaaaaaa', 'aaaaaaaaa', 'aaaaaaaaaa', 11, 'aa'),
(15, 'vhvghvh', 'gvhgvh', 'vhvhvh', 765, 'gv'),
(16, 'cfgcg', 'cgc', 'vghv', 65, 'fc'),
(17, 'hgfc', 'fcfgtc', 'gfcgfcg', 7, 'cf'),
(18, 'gfhgfhf', 'fhgfh', 'jhgjgj', 77, 'gf'),
(19, 'xsfdsfxfd', 'fxdfxf', 'zdszdsz', 32, 'tt'),
(20, 'cgfcgfc', 'gfcgc', 'cgcgfcg', 65, 'fc'),
(21, 'cgfcgc', 'fcg', 'cggcgf', 56, 'cc'),
(22, 'cfgcgc', 'cgfcg', 'vcgc', 5, 'dd'),
(23, 'cggfcgcgf', 'fgcg', 'gcgfcg', 67, 'cc'),
(24, 'ghgfhgf', 'fhfhf', 'ghgf', 6, 'hh'),
(25, 'ghbghg', 'ggjhg', 'gghg', 79, 'gg'),
(26, 'hgfhf', 'f', 'gfhf', 6, 'aa'),
(27, 'hgfhf', 'f', 'gfhf', 6, 'aa'),
(28, 'bbbbbbbb', 'aaaaaaa', 'aaaa', 11, 'aa'),
(29, 'bbbbbbbb', 'bbbbbb', 'bbbbb', 22, 'bb'),
(30, 'bbbb', 'aaaaa', 'aaaaaa', 11, 'aa'),
(31, 'bbbb', 'aaaaa', 'aaaaaa', 11, 'aa'),
(32, 'bbbb', 'bbb', 'bbbb', 22, 'bb'),
(33, 'aaaa', 'aaa', 'aaaaa', 111, 'aa'),
(34, 'aaaa', 'aaaa', 'aaa', 11, 'aa'),
(35, 'vchgcgfc', 'vghvhgv', 'ghghg', 7, 'vv'),
(36, 'vchgcgfc', 'fcgfcg', 'fghghg', 65, 'cc'),
(37, 'hgvhvgh', 'gvhgv', 'fghfhgf', 6, 'vv'),
(38, 'gvchvhg', 'vhgvh', 'cchgh', 66, 'gg'),
(39, 'gfvhgvh', 'vhgvhgv', 'ghvghv', 78, 'gg'),
(40, 'gcvhgvgh', 'vhgvhg', 'hgvghv', 77, 'vv'),
(41, 'gvhgvh', 'gvhgv', 'jhghjg', 768, 'vv'),
(42, 'cgfcgfc', 'fcgc', 'gvhgvh', 888, 'aa'),
(43, 'gfhgfhg', 'fgfhgf', 'fhgf', 66, 'ff'),
(44, 'gchgcfg', 'gfcg', 'fhgfhg', 66, 'aa'),
(45, 'hgjbjg', 'ygjhg', 'hjhg', 7, 'yy'),
(46, 'hjhgjh', 'ghjgjh', 'gjhg', 76, 'gg'),
(47, 'hbjhbhj', 'bjhbj', 'hkjh', 87, 'bb'),
(48, 'ygygu', 'guygu', 'hhkjh', 66, 'gg'),
(49, 'hgjghjg', 'jgjhg', 'gjhghg', 76, 'gg'),
(50, 'gjhgj', 'gjghg', 'gjg', 77, 'aa'),
(51, 'gfdgfdgd', 'fgdgf', 'thgfhg', 545, 'dd'),
(52, 'gdretrd', 'reeetr', 'geere', 44, 'ee'),
(53, 'gjhgjh', 'hgjhg', 'gjhg', 22, 'gg'),
(54, 'hghjghg', 'gjhgh', 'hjgjhg', 22, 'gg'),
(55, 'hgfhgfh', 'fhgfhg', 'gghf', 76, 'ff'),
(56, 'fhgfhgf', 'ghfhgf', 'gfhgf', 22, 'aa'),
(57, 'gfhgfhg', 'fghfhgf', 'fhfgf', 65, 'ff'),
(58, 'gjhg', 'ghjhg', 'gfhgfh', 2, 'gg'),
(59, 'ws', 'ss', 'wwwwww', 22, 'ss'),
(60, 'aaaa', 'aaaa', 'aaa', 33, 'aa');

-- --------------------------------------------------------

--
-- Estrutura da tabela `frequencia`
--

CREATE TABLE IF NOT EXISTS `frequencia` (
  `idFrequencia` int(11) NOT NULL AUTO_INCREMENT,
  `horaEntrada` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  `horaSaida` timestamp NULL DEFAULT NULL,
  `data` date NOT NULL,
  `status` int(11) NOT NULL,
  `Aluno_idAluno` int(11) NOT NULL,
  `ocorrencia_idOcorrencia` int(11) NOT NULL,
  PRIMARY KEY (`idFrequencia`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=3 ;

--
-- Extraindo dados da tabela `frequencia`
--

INSERT INTO `frequencia` (`idFrequencia`, `horaEntrada`, `horaSaida`, `data`, `status`, `Aluno_idAluno`, `ocorrencia_idOcorrencia`) VALUES
(1, '2017-05-15 12:07:35', NULL, '2017-05-15', 1, 3, 0),
(2, '2017-05-15 12:20:29', '2017-05-15 12:20:30', '2017-05-15', 1, 2, 0);

-- --------------------------------------------------------

--
-- Estrutura da tabela `frequenciaaluno`
--

CREATE TABLE IF NOT EXISTS `frequenciaaluno` (
  `idFrequenciaAluno` int(11) NOT NULL AUTO_INCREMENT,
  `data` date NOT NULL,
  `horaInicio` timestamp NOT NULL DEFAULT CURRENT_TIMESTAMP,
  `horaTermino` timestamp NOT NULL DEFAULT '0000-00-00 00:00:00',
  `alunosPresentes` int(255) NOT NULL,
  `alunosAusentes` int(255) NOT NULL,
  PRIMARY KEY (`idFrequenciaAluno`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;

-- --------------------------------------------------------

--
-- Estrutura da tabela `funcionario`
--

CREATE TABLE IF NOT EXISTS `funcionario` (
  `idResponsavel` int(11) NOT NULL AUTO_INCREMENT,
  `nomeFuncionario` varchar(150) NOT NULL,
  `matriculaFuncionario` varchar(20) NOT NULL,
  `areaFuncionario` varchar(50) NOT NULL,
  `cpfFuncionario` varchar(20) NOT NULL,
  `Endereco_idEndereco` int(11) NOT NULL,
  `Contato_idContato` int(11) NOT NULL,
  `contatoidContato` int(11) NOT NULL,
  `enderecoidEndereco` int(11) NOT NULL,
  PRIMARY KEY (`idResponsavel`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=2 ;

--
-- Extraindo dados da tabela `funcionario`
--

INSERT INTO `funcionario` (`idResponsavel`, `nomeFuncionario`, `matriculaFuncionario`, `areaFuncionario`, `cpfFuncionario`, `Endereco_idEndereco`, `Contato_idContato`, `contatoidContato`, `enderecoidEndereco`) VALUES
(1, 'vgvhgv', '6868', 'vhgvhgv', '675.765.757-65', 0, 35, 0, 0);

-- --------------------------------------------------------

--
-- Estrutura da tabela `ocorrencia`
--

CREATE TABLE IF NOT EXISTS `ocorrencia` (
  `idOcorrencia` int(11) NOT NULL AUTO_INCREMENT,
  `ocorrencia` longtext NOT NULL,
  `Aluno_idAluno` int(11) NOT NULL,
  PRIMARY KEY (`idOcorrencia`)
) ENGINE=InnoDB DEFAULT CHARSET=utf8 AUTO_INCREMENT=1 ;

-- --------------------------------------------------------

--
-- Estrutura da tabela `responsavel`
--

CREATE TABLE IF NOT EXISTS `responsavel` (
  `idResponsavel` int(11) NOT NULL AUTO_INCREMENT,
  `nomeResponsavel` varchar(250) NOT NULL,
  `cpfResponsavel` varchar(20) NOT NULL,
  `Contato_idContato` int(11) NOT NULL,
  `Endereco_idEndereco` int(11) NOT NULL,
  PRIMARY KEY (`idResponsavel`)
) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=23 ;

--
-- Extraindo dados da tabela `responsavel`
--

INSERT INTO `responsavel` (`idResponsavel`, `nomeResponsavel`, `cpfResponsavel`, `Contato_idContato`, `Endereco_idEndereco`) VALUES
(1, 'fhgfh', '675.757.575-75', 12, 8),
(2, 'fhgfh', '675.757.575-75', 14, 9),
(3, 'xxxxxxxx', '222.222.222-22', 16, 10),
(4, 'ssss', '222.222.222-22', 18, 11),
(5, 'gvhvghv', '657.657.576-57', 20, 12),
(6, 'aaaaaaa', '111.111.111-11', 22, 14),
(7, 'bbbbbb', '222.222.222-22', 37, 29),
(8, 'bbbbb', '222.222.222-22', 41, 32),
(9, 'aaaa', '111.111.111-11', 0, 34),
(10, 'gvhgvhgv', '675.765.765-76', 0, 0),
(11, 'gvhgvh', '657.576.576-57', 47, 38),
(12, 'gvhvhvh', '678.768.768-76', 49, 40),
(13, 'gvhgvh', '765.757.657-65', 51, 42),
(14, 'gfhgf', '675.765.765-76', 53, 44),
(15, 'hgjhg', '786.876.876-87', 55, 46),
(16, 'hbjhbjh', '876.868.768-76', 57, 48),
(17, 'hgjhg', '786.876.876-87', 59, 50),
(18, 'gfdgfdg', '546.464.654-65', 61, 52),
(19, 'jhgjhg', '768.768.768-76', 63, 54),
(20, 'gfhgf', '868.768.768-76', 65, 56),
(21, 'fhgf', '765.765.765-76', 67, 58),
(22, 'sss', '222.222.222-22', 69, 60);

/*!40101 SET CHARACTER_SET_CLIENT=@OLD_CHARACTER_SET_CLIENT */;
/*!40101 SET CHARACTER_SET_RESULTS=@OLD_CHARACTER_SET_RESULTS */;
/*!40101 SET COLLATION_CONNECTION=@OLD_COLLATION_CONNECTION */;
