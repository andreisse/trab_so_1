# trab_so_1
Desenvolva um programa utilitário baseado em linha de comando. O seu programa deverá realizar algumas ações sobre o sistema operacional. O programa deverá receber por parâmetro as opções para as ações que pode realizar. Além disso, deverá ter as opções help e version. Documente o seu programa de linha de comando em um arquivo README.md.

@echo off
cls
:menu
cls

date /t
  
## Menu 
```
echo            MENU DE TAREFAS
echo  +++++++++++++++++++++++++++++++++++
echo * 1. Backup                  	*
echo * 2. Scan de Disco Local           *
echo * 3. Sair                          * 
echo * 4. Versao             		* 
echo * 5. Help                          * 
echo  +++++++++++++++++++++++++++++++++++
```

##opcao
```
set /p op= Escolha uma opcao: 
echo ------------------------------
if %op% equ 1 goto op1
if %op% equ 2 goto op2
if %op% equ 3 goto op3
if %op% equ 4 goto op4
if %op% equ 5 goto op5
```

## Backup
```
:op1
cls
xcopy "C:\origem" "D:\destino" /e/h/s/y/d
echo +++++++++++++++++++++++++++++++++++
echo *      Backup concluido           *
echo +++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Scan de Disco Local
```
:op2
cls
echo +++++++++++++++++++++++++++++++++++
echo *     Scan de Disco Local		*
echo +++++++++++++++++++++++++++++++++++
chkdsk c:
pause
goto menu
```

## Sair
```
:op3
cls
exit
```

## Versão
```
:op4
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * 0.0 *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```

## Descrição (help)
```
:op5
echo +++++++++++++++++++++++++++++++++++++++++++++++
echo * Opcao 1 - Essa opcao ira realizar a limpeza da sua lixeira                  *
echo * Opcao 2 - Essa opcao ira realizar um backup na pasta deseja                 *
echo * Opcao 3 - Essa opcao ira realizar um scaneamento no seu disco rigido        *
echo * Opcao 4 - Essa opcao ira fechar o sistema                                   *
echo * Opcao 5 - Essa opcao ira mostrar a versão do sistema caso deseja saber      *
echo * Opcao 6 - Essa opcao ira abrir a lista de comandos que serão possivel fazer *
echo +++++++++++++++++++++++++++++++++++++++++++++++
pause
goto menu
```
