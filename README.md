# GitHub Agent - AI Developer Agent

Nowoczesna aplikacja webowa, która wykorzystuje GitHub MCP (Model Context Protocol) server do wykonywania operacji na GitHub w imieniu użytkowników.

## Przegląd

Ta aplikacja służy jako centralny orchestrator, który tłumaczy polecenia użytkownika na odpowiednie akcje GitHub poprzez integrację MCP, w tym zarządzanie repozytoriami, operacje na plikach, pull requesty, issues, workflows i wiele więcej.

## Funkcjonalności

### 🔗 Integracja MCP
- Bezpieczna obsługa sesji i autoryzacja OAuth
- Przekazywanie kontekstu i instrukcji do MCP
- Odbieranie odpowiedzi i statusów wykonanych akcji GitHub
- Zaawansowane techniki inżynierii instrukcji systemowych
- Throttling, rate limiting oraz audyt działań

### 📁 Zarządzanie Repozytoriami
- `create_repository`, `fork_repository`
- `star_repository`, `unstar_repository`
- `list_starred_repositories`

### 📝 Operacje na Plikach
- `create_or_update_file`, `delete_file`
- `push_files`, `get_file_contents`

### 🌿 Zarządzanie Gałęziami
- `create_branch`, `list_branches`

### 🎯 Issues
- `create_issue`, `update_issue`, `get_issue`
- `list_issues`, `get_issue_comments`, `add_issue_comment`
- `list_issue_types`, `assign_copilot_to_issue`

### 🔗 Sub-Issues
- `add_sub_issue`, `remove_sub_issue`
- `list_sub_issues`, `reprioritize_sub_issue`

### 🔄 Pull Requests
- `create_pull_request`, `create_pull_request_with_copilot`
- `update_pull_request`, `get_pull_request`
- `list_pull_requests`, `merge_pull_request`
- `get_pull_request_diff`, `get_pull_request_files`
- `get_pull_request_status`, `update_pull_request_branch`

### 👁️ Recenzje PR
- `create_pending_pull_request_review`
- `create_and_submit_pull_request_review`
- `add_comment_to_pending_review`
- `submit_pending_pull_request_review`
- `delete_pending_pull_request_review`
- `get_pull_request_reviews`, `get_pull_request_review_comments`
- `request_copilot_review`

### 📜 Commits i Historia
- `list_commits`, `get_commit`

### ⚙️ Workflows i Actions
- `list_workflows`, `run_workflow`
- `list_workflow_runs`, `get_workflow_run`
- `cancel_workflow_run`, `rerun_workflow_run`
- `rerun_failed_jobs`, `list_workflow_jobs`
- `get_workflow_run_usage`

### 📊 Logi i Artefakty
- `get_job_logs`, `get_workflow_run_logs`
- `delete_workflow_run_logs`
- `list_workflow_run_artifacts`, `download_workflow_run_artifact`

### 🏷️ Release i Tagi
- `list_releases`, `get_latest_release`
- `get_release_by_tag`, `list_tags`, `get_tag`

### 🔍 Wyszukiwanie
- `search_code`, `search_repositories`
- `search_issues`, `search_pull_requests`
- `search_users`, `search_orgs`

### 📬 Powiadomienia
- `list_notifications`, `get_notification_details`
- `dismiss_notification`, `mark_all_notifications_read`
- `manage_notification_subscription`
- `manage_repository_notification_subscription`

### 💬 Dyskusje
- `list_discussions`, `get_discussion`
- `get_discussion_comments`, `list_discussion_categories`

### 🔒 Bezpieczeństwo
- Code/secret scanning alerts
- Dependabot alerts
- Security advisories

### 📝 Gists
- `create_gist`, `update_gist`, `list_gists`

### 👥 Zespoły i Użytkownicy
- `get_me`, `get_teams`, `get_team_members`

## Architektura

### Frontend
- **Framework**: React 18 + TypeScript
- **Styling**: Styled Components/Emotion
- **State Management**: Redux Toolkit
- **Build Tool**: Vite
- **UI Library**: Material-UI v5

### Backend
- **Runtime**: Node.js 18 + NestJS 9
- **Database**: PostgreSQL
- **API**: REST + optional GraphQL
- **Authentication**: OAuth 2.0 (GitHub)
- **MCP Integration**: Dedykowana warstwa pośrednicząca

### Design System
- **Paleta kolorów**: Primary #5B8CFF, Secondary #00C2A8, #F59E0B
- **Typografia**: Inter font stack
- **Responsive**: Mobile-first approach
- **Accessibility**: WCAG 2.1 AA compliance

## Bezpieczeństwo

- OAuth 2.0 z GitHub z minimalnymi wymaganymi uprawnieniami
- Szyfrowanie tokenów i rotacja kluczy
- Audyt wszystkich działań z timestamp i kontekstem
- Throttling i rate limiting dla MCP
- Bezpieczne przechowywanie danych użytkownika

## Rozpoczęcie Pracy

1. Klonowanie repozytorium
2. Instalacja zależności
3. Konfiguracja OAuth z GitHub
4. Uruchomienie środowiska deweloperskiego
5. Integracja z MCP server

Szczegółowe instrukcje setup będą dostępne wkrótce...

## Licencja

MIT License
