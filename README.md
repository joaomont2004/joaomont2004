Dia 1 – Ambiente

Organizei meu GitHub criando os repositórios estudos-programacao-2026, desafios-logica e clinica-api. Também configurei o Git na máquina (user.name, user.email e a branch padrão main), fiz meu primeiro repositório local com um commit inicial e revisei os comandos básicos do terminal, como pwd, ls, cd, mkdir, touch, cp, mv e rm.

Dia 2 – Git na prática

Treinei o fluxo básico do Git (status, add, commit, push e pull). Criei minha primeira branch (feature-login), comecei a fazer commits menores e mais frequentes e depois fiz o merge dela de volta para a main.

Dia 3 – Conflitos de merge

Simulei um conflito de merge editando a mesma linha em duas branches diferentes. Resolvi o conflito manualmente, entendendo como funcionam as marcações <<<<<<<, ======= e >>>>>>>, e finalizei o processo com um Pull Request no GitHub.

Dia 4 – Revisão de PHP

Percebi que estava apenas copiando código sem entender o motivo de cada linha existir. A partir desse dia, mudei a forma de estudar: primeiro entender a lógica e só depois escrever o código.

Dia 5 – Projeto: Controle de Tarefas

Desenvolvi do zero um sistema simples de controle de tarefas em PHP. Durante o projeto aprendi a usar arrays associativos para representar cada tarefa, percorri listas com foreach, entendi a diferença entre passar parâmetros por valor e por referência, usei operador ternário para simplificar condições e trabalhei com entrada de dados usando fgets(STDIN) e trim().

Também montei um menu interativo com while e if/elseif, salvei os dados em um arquivo JSON usando json_encode e json_decode e consegui resolver sozinho quatro bugs reais: um booleano tratado como string, uma lógica invertida no file_exists(), uma função que não estava sendo chamada e um erro de sintaxe no operador ternário.

No final, publiquei o projeto no GitHub, escrevi um README e resolvi um problema de push rejeitado usando git pull origin main --allow-unrelated-histories.

Dia 6 – Classes e Objetos

Estudei a base da POO em PHP: classes, objetos, atributos, métodos, construtor e os modificadores private, protected, public. Criei a classe Paciente com id, nome, cpf, telefone e dataNascimento, com os métodos atualizarTelefone() e exibirResumo(). No desafio, implementei validaTelefone() pra impedir telefone vazio ou fora do padrão, lançando Exception quando inválido.

Dia 7 – Herança

Modelei uma hierarquia em cadeia: Pessoa → Funcionario → Dentista e Recepcionista, usando extends e parent::__construct() pra reaproveitar atributos e métodos entre as classes. No desafio, cada classe sobrescreveu descricao() encadeando parent::descricao(), o que me fez entender polimorfismo na prática — mesmo método, comportamento diferente dependendo do objeto.

Dia 8 – Interfaces e Traits

Aprendi a diferença entre interface (contrato, só assinatura) e trait (comportamento pronto, compartilhado entre classes sem parentesco). Criei a interface Agendavel com agendarConsulta(), implementada em Dentista, e o trait Logavel com registrarLog(), reutilizado tanto em Dentista quanto em Paciente — classes de ramos diferentes da hierarquia. No desafio, fiz toda ação importante (como atualizar telefone) gerar um log, com cuidado pra registrar só depois da validação passar, evitando logs de ações que na verdade falharam.

Dia 9 – Exceptions

Estudei try/catch/throw e criei exceptions personalizadas: PacienteException como base, e CpfInvalidoException, NomeVazioException e TelefoneInvalidoException estendendo ela. Cada uma já vem com sua própria mensagem padrão, então basta dar throw new sem repetir texto toda vez. Troquei as validações de Paciente pra usar essas exceções específicas em vez de Exception genérica, e testei os 4 cenários (nome vazio, CPF inválido, telefone inválido, paciente válido) com try/catch, sem nenhum die() ou exit() — só Exceptions, como o desafio pedia.
