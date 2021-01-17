---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471597"
---
# Enable-AzContextAutosave

## SYNOPSIS
Bei den Azure-Kontexten handelt es sich um PowerShell-Objekte, die Ihr aktives Abonnement zum Ausführen von Befehlen darstellen, sowie die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure Cloud erforderlich sind. Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal neu authentifizieren, wenn Sie zwischen Abonnements wechseln. Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekten.](https://docs.microsoft.com/powershell/azure/context-persistence)

Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und automatisch geladen werden, wenn Sie einen PowerShell-Prozess starten. Beispielsweise beim Öffnen eines neuen Fensters.

## SYNTAX

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG

Ermöglicht das Speichern und automatische Laden der Azure-Kontextinformationen, wenn ein PowerShell-Prozess gestartet wird. Der Kontext wird am Ende der Ausführung eines Cmdlets gespeichert, das sich auf den Kontext auswirkt. Beispiel: ein beliebiges Profil-Cmdlet. Wenn Sie die Benutzerauthentifizierung verwenden, können die Token während der Ausführung eines beliebigen Cmdlets aktualisiert werden.

## BEISPIELE

### Beispiel 1: Aktivieren der automatischen Speicherung von Anmeldeinformationen für den aktuellen Benutzer

Aktivieren Sie die automatische Speicherung der Anmeldeinformationen für den aktuellen Benutzer. Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.

```powershell
Enable-AzContextAutosave
```

### Beispiel 2

Lassen Sie zu, dass die Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster in dieser PowerShell-Sitzung öffnen. (automatisch generiert)

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## PARAMETERS

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

Bestimmt den Umfang der Kontextänderungen. Beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten. Änderungen, die mit dem Bereich vorgenommen werden, wirken sich auf alle vom Benutzer `CurrentUser` gestarteten PowerShell-Sitzungen aus. Wenn eine bestimmte Sitzung unterschiedliche Einstellungen haben muss, verwenden Sie den `Process` Bereich.

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

### -Confirm

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

### -Waswenn

Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
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

### Allgemeine Parameter

Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
