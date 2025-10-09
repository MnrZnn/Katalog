# Katalog

## Introdução

O **Katalog** é uma plataforma web onde usuários podem **cadastrar, organizar e compartilhar suas coleções de discos** — sejam CDs, vinis, cassetes ou mídias digitais.
O sistema permite inserir múltiplos registros de uma vez, importar planilhas, gerar QR Codes de coleções e acessar os dados em qualquer dispositivo conectado à internet.

## Objetivo

Oferecer uma ferramenta prática e moderna para **colecionadores de música**, permitindo o gerenciamento completo de coleções pessoais com recursos de **importação, backup, busca automática de capas e compartilhamento público**.

## Público-Alvo

Colecionadores de música, tanto amadores quanto profissionais, que desejam **organizar e digitalizar suas coleções** de maneira simples, segura e acessível.

---

## Requisitos do Sistema

### Requisitos Funcionais

1. **Cadastro e Autenticação de Usuários**

   * O sistema deve permitir cadastro, login e logout via Firebase Authentication.
   * O usuário deve poder redefinir senha e excluir sua conta.

2. **Gerenciamento de Coleção**

   * Inserção, edição e exclusão de discos.
   * Suporte a múltiplos formatos: CD, Vinil, Cassete e Digital.
   * Visualização em **grade** ou **lista**.
   * Filtros e busca por nome do artista, álbum ou ano.

3. **Lista de Desejos (Wishlist)**

   * O usuário pode adicionar itens desejados e mover para a coleção quando adquiridos.

4. **Importação e Exportação**

   * Importação de planilhas **Excel (.xlsx)** via **SheetJS**.
   * Exportação da coleção para Excel para backup.

5. **Compartilhamento**

   * Geração de link público e **QR Code** da coleção (com controle de visibilidade).
   * Compartilhamento rápido em redes sociais (Facebook, X/Twitter, Reddit, WhatsApp).

6. **Temas e Personalização**

   * Alternância entre tema claro e escuro.
   * Interface responsiva adaptada a desktop e dispositivos móveis.

7. **Integração com Plataformas Externas**

   * Busca de informações e capas através de APIs e links externos (YouTube, Spotify, Apple Music, RateYourMusic).

---

### Requisitos Não Funcionais

1. **Usabilidade:** Interface intuitiva e responsiva desenvolvida com TailwindCSS e Alpine.js.
2. **Desempenho:** Carregamento assíncrono e lazy loading de imagens.
3. **Portabilidade:** Funciona em navegadores modernos e dispositivos móveis.
4. **Manutenibilidade:** Código modular e documentado.
5. **Disponibilidade:** Armazenamento em nuvem (Firebase Firestore) garantindo acesso remoto e sincronização em tempo real.

---

## Requisitos de Dados

* **Usuários:** informações de login, nome e e-mail.
* **Coleção:** título do álbum, artista, formato, ano, número de catálogo, URL da capa e descrição.
* **Lista de Desejos(Wishlist):** estrutura similar à coleção, porém marcada como “desejada”.
* **Configurações:** tema selecionado, status de visibilidade e link público.

Todos os dados são armazenados no **Firebase Firestore** e associados ao ID do usuário autenticado.

---

## Requisitos de Segurança

1. **Autenticação e Autorização:** controle de acesso via Firebase Auth.
2. **Criptografia:** senhas e tokens protegidos pela camada de segurança do Firebase.
3. **Privacidade:** coleções são privadas por padrão; o usuário escolhe se deseja torná-las públicas.
4. **Backups:** exportação manual dos dados via Excel para segurança adicional.
5. **Verificação de E-mail:** necessária para liberar recursos avançados como importações ilimitadas.

---

## Bibliotecas e Tecnologias Utilizadas

| Categoria                    | Tecnologia / Biblioteca                              |
| ---------------------------- | ---------------------------------------------------- |
| **Frontend**                 | HTML5, TailwindCSS, Alpine.js                        |
| **Banco de Dados / Backend** | Firebase Firestore                                   |
| **Autenticação**             | Firebase Authentication                              |
| **Planilhas**                | SheetJS (xlsx.full.min.js)                           |
| **QR Code**                  | qrcodejs                                             |
| **Ícones**                   | Lucide Icons                                         |
| **Fontes**                   | Google Fonts (Inter)                                 |
| **Hospedagem **              | Github Pages                                         |

---

## Recursos Principais

* Modo claro e escuro automático.
* Layout responsivo (De dispotívos móveis á telas grandes).
* Importação/Exportação em Excel.
* Compartilhamento via link e QR Code.
* Recuperação e exclusão de conta seguras.

---

## Autores

* Luiza Helena Tardelli Marculli Espíndola (Documentação)
* Munir Terranova Abou Zenni (Desenvolvedor e Administrador)
* Renan do Nascimento Martins (Documentação)

---

