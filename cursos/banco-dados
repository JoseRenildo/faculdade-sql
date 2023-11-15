create database Faculdade;
use Faculdade;

create table aluno(
idAluno int not null,
matricula varchar (10) not null,
nome varchar (50) not null,
primary key (idAluno)
);

create table disciplina (
idDisciplina int not null,
nome varchar (50) not null,
cargaHoraria int not null,
primary key (idDisciplina)
);

create table curso (
idCurso int not null,
nome varchar (50) not null,
primary key (idCurso));

create table historico (
idAluno int not null,
idDisciplina int not null,
nota float not null,
dataHistorico date not null,
foreign key (idAluno) references aluno (idAluno),
foreign key (idDisciplina) references disciplina (idDisciplina)
);

create table AlunoCurso(
idAluno int not null,
idCurso int not null,
anoEntrada int not null,
foreign key (idAluno) references aluno (idAluno),
foreign key (idCurso) references curso (idCurso)
);

create table grade(
idGrade int not null,
idCurso int not null,
ano int not null,
cargaHorariaTotal int not null,
primary key (idGrade),
foreign key (idCurso) references curso (idCurso)
);

create table GradeDisciplina(
idGrade int not null,
idDisciplina int not null,
foreign key (idGrade) references grade (idGrade),
foreign key (idDisciplina) references disciplina (idDisciplina)
);
