Jako administrátor bych primárně upravil zdrojový kód utility syscheck, aby volala systémové příkazy výhradně pomocí absolutních cest (např. /usr/bin/date), čímž se zamezí Path Injection. 
Dále je nezbytné provést audit SUID souborů a odstranit tento příznak u aplikací, které jej k funkci nepotřebují (např. nano).
Pro zvýšení bezpečnosti by bylo vhodné nahradit SUID mechanismus pomocí Linux Capabilities, které umožňují přidělit procesu jen specifické oprávnění místo plného přístupu pod uživatelem root.
