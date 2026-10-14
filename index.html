<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Escola do Bom Condutor - CGB Energia</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/@supabase/supabase-js@2"></script>
</head>
<body class="bg-slate-50 min-h-screen font-sans">

    <!-- Header / Navbar -->
    <header class="bg-slate-900 text-white shadow-md">
        <div class="max-w-4xl mx-auto px-4 py-4 flex justify-between items-center">
            <h1 class="text-lg font-bold tracking-wide">ESCOLA DO BOM CONDUTOR <span class="text-yellow-400 text-xs block font-normal">CGB Energia - Segurança e Direção Defensiva</span></h1>
            <span class="text-xs bg-slate-800 px-3 py-1 rounded-full text-slate-300">Sistema Oficial</span>
        </div>
    </header>

    <!-- Main Container -->
    <main class="max-w-4xl mx-auto px-4 py-8">
        
        <!-- Etapa 1: Identificação do Colaborador -->
        <section id="step-collab" class="bg-white rounded-xl shadow-sm border border-slate-200 p-6">
            <h2 class="text-xl font-bold text-slate-800 mb-2">Identificação do Colaborador</h2>
            <p class="text-sm text-slate-500 mb-6">Digite seu nome ou matrícula para iniciar a avaliação.</p>
            
            <div class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-slate-700 mb-1">Buscar Colaborador</label>
                    <input type="text" id="search-input" placeholder="Ex: Marcus Vinicius ou Matrícula..." class="w-full px-4 py-3 border border-slate-300 rounded-lg focus:ring-2 focus:ring-slate-900 focus:outline-none text-slate-800">
                </div>

                <div id="results-container" class="hidden bg-slate-50 border border-slate-200 rounded-lg max-h-48 overflow-y-auto divide-y divide-slate-200">
                    <!-- Resultados da busca aparecem aqui -->
                </div>

                <div id="selected-collab" class="hidden bg-yellow-50 border border-yellow-200 p-4 rounded-lg flex justify-between items-center">
                    <div>
                        <p class="text-xs font-semibold text-yellow-800 uppercase">Colaborador Selecionado:</p>
                        <p id="collab-name-display" class="font-bold text-slate-900 text-lg"></p>
                        <p id="collab-info-display" class="text-xs text-slate-600"></p>
                    </div>
                    <button onclick="resetCollab()" class="text-xs text-red-600 hover:underline font-medium">Alterar</button>
                </div>

                <button id="btn-start" onclick="startQuiz()" disabled class="w-full bg-slate-900 text-white py-3 rounded-lg font-medium hover:bg-slate-800 transition disabled:opacity-50 disabled:cursor-not-allowed">
                    Iniciar Avaliação
                </button>
            </div>
        </section>

        <!-- Etapa 2: Quiz / Avaliação (Oculto inicialmente) -->
        <section id="step-quiz" class="hidden bg-white rounded-xl shadow-sm border border-slate-200 p-6">
            <div class="flex justify-between items-center mb-6 pb-4 border-b border-slate-100">
                <span id="quiz-progress" class="text-xs font-bold text-slate-500 uppercase tracking-wider">Questão 1 de 5</span>
                <span id="quiz-timer" class="text-xs font-mono bg-slate-100 px-2 py-1 rounded text-slate-700">⏱️ Tempo Livre</span>
            </div>

            <h3 id="question-text" class="text-lg font-semibold text-slate-800 mb-6"></h3>

            <div id="options-container" class="space-y-3 mb-8">
                <!-- Opções injetadas via JS -->
            </div>

            <button id="btn-next" onclick="nextQuestion()" disabled class="w-full bg-slate-900 text-white py-3 rounded-lg font-medium hover:bg-slate-800 transition disabled:opacity-50 disabled:cursor-not-allowed">
                Próxima Questão
            </button>
        </section>

        <!-- Etapa 3: Resultado (Oculto inicialmente) -->
        <section id="step-result" class="hidden bg-white rounded-xl shadow-sm border border-slate-200 p-8 text-center">
            <div id="result-icon" class="text-5xl mb-4">🏆</div>
            <h2 id="result-title" class="text-2xl font-bold text-slate-900 mb-2">Avaliação Concluída!</h2>
            <p id="result-desc" class="text-slate-600 mb-6">Seu registo foi gravado com sucesso no sistema.</p>
            <div class="bg-slate-50 p-4 rounded-lg max-w-xs mx-auto mb-6">
                <span class="text-xs text-slate-500 block">Pontuação Final</span>
                <span id="result-score" class="text-3xl font-bold text-slate-900">100%</span>
            </div>
            <button onclick="location.reload()" class="bg-slate-900 text-white px-6 py-2.5 rounded-lg text-sm font-medium hover:bg-slate-800 transition">
                Nova Avaliação
            </button>
        </section>

    </main>

    <!-- Script de Integração e Lógica -->
    <script>
        // Configuração do Supabase (Substitua com suas chaves públicas quando desejar conectar direto)
        const SUPABASE_URL = 'https://jwzqjidbhuhutffhslw.supabase.co';
        const SUPABASE_ANON_KEY = 'sua-chave-anon-aqui';
        
        // Simulação de banco local caso queira testes imediatos sem internet, ou integrado com Supabase
        let selectedCollabData = null;
        let currentQuestionIndex = 0;
        let score = 0;

        const questions = [
            {
                text: "Qual é a principal atitude defensiva ao conduzir veículos da frota em vias urbanas e rodovias?",
                options: [
                    "Acelerar para evitar o trânsito intenso.",
                    "Prever situações de risco e manter distância de segurança.",
                    "Ultrapassar sempre pela direita para ganhar tempo.",
                    "Desligar os faróis durante o dia para economizar bateria."
                ],
                correct: 1
            },
            {
                text: "Em caso de pista molhada ou chuva forte, qual procedimento correto o condutor deve adotar?",
                options: [
                    "Manter a velocidade máxima permitida da via.",
                    "Reduzir a velocidade e aumentar a distância do veículo à frente.",
                    "Utilizar o pisca-alerta com o veículo em movimento na rodovia.",
                    "Frear bruscamente em cima das poças d'água."
                ],
                correct: 1
            },
            {
                text: "O uso do cinto de segurança é obrigatório para:",
                options: [
                    "Apenas para o condutor em viagens longas.",
                    "Somente para os passageiros do banco dianteiro.",
                    "Todos os ocupantes do veículo, em qualquer tipo de via.",
                    "Apenas em rodovias federais."
                ],
                correct: 2
            }
        ];

        // Busca simulada/real de colaboradores (já com seu nome incluído para teste imediato)
        const mockColaboradores = [
            { nome: "MARCUS VINICIUS SILVA QUEIROS", matricula: "12375", funcao: "ANALISTA DE QUALIDADE I", base: "BACABAL" },
            { nome: "ABEL RODRIGUES DE ARAUJO", matricula: "14035", funcao: "ELETRICISTA", base: "BACABAL" },
            { nome: "ABRAAO DOS SANTOS SILVA", matricula: "13795", funcao: "ELETRICISTA", base: "BACABAL" }
        ];

        const searchInput = document.getElementById('search-input');
        const resultsContainer = document.getElementById('results-container');

        searchInput.addEventListener('input', (e) => {
            const query = e.target.value.toLowerCase();
            if (query.length < 2) {
                resultsContainer.classList.add('hidden');
                return;
            }

            const filtered = mockColaboradores.filter(c => c.nome.toLowerCase().includes(query) || c.matricula.includes(query));
            
            if (filtered.length > 0) {
                resultsContainer.innerHTML = filtered.map(c => `
                    <div onclick='selectCollab(${JSON.stringify(c)})' class="p-3 hover:bg-slate-100 cursor-pointer text-sm">
                        <p class="font-bold text-slate-800">${c.nome}</p>
                        <p class="text-xs text-slate-500">Mat: ${c.matricula} | Função: ${c.funcao} | Base: ${c.base}</p>
                    </div>
                `).join('');
                resultsContainer.classList.remove('hidden');
            } else {
                resultsContainer.innerHTML = '<div class="p-3 text-xs text-slate-500">Nenhum colaborador encontrado.</div>';
                resultsContainer.classList.remove('hidden');
            }
        });

        function selectCollab(collab) {
            selectedCollabData = collab;
            searchInput.value = '';
            resultsContainer.classList.add('hidden');
            
            document.getElementById('collab-name-display').textContent = collab.nome;
            document.getElementById('collab-info-display').textContent = `Matrícula: ${collab.matricula} • ${collab.funcao} (${collab.base})`;
            
            document.getElementById('selected-collab').classList.remove('hidden');
            document.getElementById('btn-start').disabled = false;
        }

        function resetCollab() {
            selectedCollabData = null;
            document.getElementById('selected-collab').classList.add('hidden');
            document.getElementById('btn-start').disabled = true;
        }

        function startQuiz() {
            if (!selectedCollabData) return;
            document.getElementById('step-collab').classList.add('hidden');
            document.getElementById('step-quiz').classList.remove('hidden');
            loadQuestion();
        }

        function loadQuestion() {
            const q = questions[currentQuestionIndex];
            document.getElementById('quiz-progress').textContent = `Questão ${currentQuestionIndex + 1} de ${questions.length}`;
            document.getElementById('question-text').textContent = q.text;
            
            const optionsHtml = q.options.map((opt, index) => `
                <label class="flex items-center p-3 border border-slate-200 rounded-lg hover:bg-slate-50 cursor-pointer transition">
                    <input type="radio" name="option" value="${index}" onclick="enableNext()" class="mr-3 text-slate-900 focus:ring-slate-900">
                    <span class="text-sm text-slate-700">${opt}</span>
                </label>
            `).join('');
            
            document.getElementById('options-container').innerHTML = optionsHtml;
            document.getElementById('btn-next').disabled = true;
        }

        function enableNext() {
            document.getElementById('btn-next').disabled = false;
        }

        function nextQuestion() {
            const selected = document.querySelector('input[name="option"]:checked');
            if (!selected) return;

            if (parseInt(selected.value) === questions[currentQuestionIndex].correct) {
                score++;
            }

            currentQuestionIndex++;
            if (currentQuestionIndex < questions.length) {
                loadQuestion();
            } else {
                showResult();
            }
        }

        function showResult() {
            document.getElementById('step-quiz').classList.add('hidden');
            document.getElementById('step-result').classList.remove('hidden');
            
            const percentage = Math.round((score / questions.length) * 100);
            document.getElementById('result-score').textContent = `${percentage}%`;
            
            if (percentage >= 70) {
                document.getElementById('result-title').textContent = "Aprovado com Sucesso!";
                document.getElementById('result-desc').textContent = `${selectedCollabData.nome}, você concluiu a avaliação da Escola do Bom Condutor.`;
            } else {
                document.getElementById('result-icon').textContent = "⚠️";
                document.getElementById('result-title').textContent = "Necessita Revisão";
                document.getElementById('result-desc').textContent = `${selectedCollabData.nome}, reveja os conceitos de direção defensiva.`;
            }
        }
    </script>
</body>
</html>
