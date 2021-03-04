---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 8bca1314433f8fcbcc0c9f395783bbb3d9835ffb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943192"
---
# Enable-AzContextAutosave

## SYNOPSIS
Azure-Kontexte sind PowerShell-Objekte, die Ihr aktives Abonnement zum Ausführen von Befehlen darstellen, und die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind. Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal erneut authentifizieren, wenn Sie abonnements wechseln. Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekte](https://docs.microsoft.com/powershell/azure/context-persistence).

Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und automatisch geladen werden, wenn Sie einen PowerShell-Prozess starten. Beispielsweise beim Öffnen eines neuen Fensters.

## SYNTAX

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Ermöglicht das Speichern und automatische Laden der Azure-Kontextinformationen, wenn ein PowerShell-Prozess gestartet wird. Der Kontext wird am Ende der Ausführung eines cmdlets gespeichert, das sich auf den Kontext auswirkt. Beispiel: ein beliebiges Profil-Cmdlet. Wenn Sie die Benutzerauthentifizierung verwenden, können Token während der Ausführung eines cmdlets aktualisiert werden.

## BEISPIELE

### Beispiel 1: Aktivieren der automatischen Speicherung von Anmeldeinformationen für den aktuellen Benutzer

Aktivieren Sie die automatische Speicherung von Anmeldeinformationen für den aktuellen Benutzer. Wenn ein PowerShell-Fenster geöffnet wird, wird Ihr aktueller Kontext ohne Anmeldung gespeichert.

```powershell
Enable-AzContextAutosave
```

### Beispiel 2

Zulassen, dass die Azure-Anmeldeinformationen, konto- und Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster in dieser PowerShell-Sitzung öffnen. (automatisch generiert)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETER

### -DefaultProfile

Die Anmeldeinformationen, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Scope

Bestimmt den Umfang von Kontextänderungen. Beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle sitzungen gelten, die von diesem Benutzer gestartet wurden. Änderungen, die mit dem Bereich vorgenommen werden, wirken sich auf alle vom Benutzer `CurrentUser` gestarteten PowerShell-Sitzungen aus. Wenn eine bestimmte Sitzung unterschiedliche Einstellungen haben muss, verwenden Sie den Bereich `Process` .

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: CurrentUser
Accept pipeline input: False
Accept wildcard characters: False
```

### -Bestätigen

Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf

Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## NOTIZEN

## VERWANDTE LINKS
