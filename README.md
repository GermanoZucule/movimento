# Movimento

Aplicativo web pessoal de calistenia com três blocos progressivos de quatro semanas.

## Executar

Sem instalação de dependências:

```sh
python3 -m http.server 8080 --directory dist
```

Abre http://localhost:8080. O modo offline requer HTTPS ou localhost. Na primeira visita com ligação, aguarda **Pronto para usar offline**. Depois, abre pelo mesmo endereço ou pelo histórico do mesmo navegador.

## Funcionalidades

- 12 semanas, treinos por dia e marcação por série.
- Ilustrações e instruções dos exercícios.
- Fotos de antes/depois por bloco e avaliação de transição.
- Cache offline com service worker.
- Fotos em IndexedDB e registos em localStorage.
- Exportação e restauro de cópias com fotos.

Não existe sincronização automática com servidor. Limpar os dados do navegador remove os registos locais. As imagens pessoais adicionadas no aplicativo não estão neste repositório.

## Verificar

```sh
node checks/progress.cjs
node checks/offline.cjs
```

Para alojar, serve a pasta dist na raiz do domínio. Os caminhos do service worker são absolutos; GitHub Pages numa subpasta exige adaptação. O endereço actualmente alojado é https://germano-calistenia-guia.djimbitoman.chatgpt.site.
