# Changelog #

- Extended vimTodo
  - *line:31*
- vimBuiltin, vimBuiltinAmp
  - *line:37*
- vimScriptID 
  - *line:40*
- vimVarNamespace
  - *line:215*
- vimCVar
  - *line:217*
- Extended `vimOper` to include '?' & ':'
  - *line:261*
- vimNamespace
  - *line:247*
- Snuck in vimBrackets for inclusion in funcs/userFuncs
  - *line:459*
- Removed `<sid>` & `<plug>` from vimNotation. They belong to `mapMod`
  - *line:582*

```viml
" vimScopeResolutionOper
syn match vimScriptID contained "#"	containedin=vimAugroup,vimFunc,vimFunction,vimFuncBody,vimFuncName,vimUserCmd,vimUserCommand,vimUserFunc,vimVar,vimFBVar,vimCVar,vimVarNamespace

" Added `vimVarNamespace`
syn match vimVarNamespace contained	"g:\S*#\ze\%(\h*\)"	containedin=vimAugroup,vimFunc,vimFunction,vimFuncBody,vimFuncName,vimUserCmd,vimUserCommand,vimUserFunc,vimVar,vimFBVar,vimCVar,vimVarNamespace

" Added `vimCVar`
syn match vimCVar       contained   "\(b\|w\|l\|s\|t\|a\|v\)\:"

" Added `vimNamespace
syn match         vimNamespace	"\%(\s\)\@<=\(\w\+\)\%(#\)\@="
syn match         vimNamespace	contained	"\v%(\s)\zs(\S*#)\ze%(\S+\(.+\))"	containedin=vimAugroup,vimCommand,vimIsCommand,vimFunc,vimFunction,vimFuncBody,vimFuncBodyList,vimFuncName,vimUserCmd,vimUserCommand,vimUserFunc,vimVar,vimFBVar,vimCVar,vimVarNamespace

```
