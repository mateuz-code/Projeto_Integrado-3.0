# =====================================================================
# SIMULAÇÃO DE DIRETIVAS DE SEGURANÇA (GPO) - MEDTECH DIGITAL
# TARGET: CONTROLADOR DE DOMÍNIO / WINDOWS SERVER (CONCEITUAL)
# =====================================================================

[Configurações de Password (Domínio 1)]
MinimumPasswordLength = 12          ; Força senhas longas e seguras
PasswordComplexity = 1              ; Exige letras maiúsculas, minúsculas, números e símbolos
PasswordHistoryCount = 24           ; Impede o colaborador de repetir as mesmas senhas
MaximumPasswordAge = 90             ; Obriga a troca de senha a cada 90 dias

[Configurações de Bloqueio de Estação (Domínio 4)]
ScreenSaverActive = 1
ScreenSaverTimeout = 300            ; Bloqueia a tela após 5 minutos de inatividade
ScreenSaverIsSecure = 1             ; Exige credenciais para retornar (Windows + L)

[Configurações de Auditoria e Logs (Domínio 3)]
AuditLogonEvents = Success, Failure ; Registra tentativas de login com sucesso ou falha
AuditAccessPolicy = Success, Failure; Monitora quem acessou ou tentou acessar dados sensíveis
