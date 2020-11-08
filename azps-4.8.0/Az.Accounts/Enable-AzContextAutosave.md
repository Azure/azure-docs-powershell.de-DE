---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azcontextautosave
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzContextAutosave.md
ms.openlocfilehash: 6d80ee2ee2072bd31e96f4daa5706cba5f1c8dab
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166628"
---
# Enable-AzContextAutosave

## Synopsis
Azure-Kontexte sind PowerShell-Objekte, die das aktive Abonnement für die Ausführung von Befehlen darstellen, und die Authentifizierungsinformationen, die zum Herstellen einer Verbindung mit einer Azure-Cloud erforderlich sind. Bei Azure-Kontexten muss Azure PowerShell Ihr Konto nicht jedes Mal erneut authentifizieren, wenn Sie Abonnements wechseln. Weitere Informationen finden Sie unter [Azure PowerShell-Kontextobjekte](https://docs.microsoft.com/powershell/azure/context-persistence).

Mit diesem Cmdlet können die Azure-Kontextinformationen gespeichert und beim Starten eines PowerShell-Prozesses automatisch geladen werden. Beispielsweise beim Öffnen eines neuen Fensters.

## Syntax

```
Enable-AzContextAutosave [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung

Ermöglicht das Speichern und Automatisches Laden der Azure-Kontextinformationen, wenn ein PowerShell-Prozess gestartet wird. Der Kontext wird am Ende der Ausführung eines beliebigen Cmdlets gespeichert, das sich auf den Kontext auswirkt. Beispiel: jedes Profil-Cmdlet. Wenn Sie die Benutzerauthentifizierung verwenden, können Token im Verlauf der Ausführung eines beliebigen Cmdlets aktualisiert werden.

## Beispiele

### Beispiel 1: Aktivieren der AutoSpeichern-Anmeldeinformationen für den aktuellen Benutzer

Aktivieren Sie das automatische Speichern von Anmeldeinformationen für den aktuellen Benutzer. Wenn ein PowerShell-Fenster geöffnet wird, wird der aktuelle Kontext ohne Anmeldung gespeichert.

```powershell
Enable-AzContextAutosave
```

### Beispiel 2

Zulassen, dass die Azure-Anmeldeinformationen, das Konto und die Abonnementinformationen gespeichert und automatisch geladen werden, wenn Sie ein PowerShell-Fenster in dieser PowerShell-Sitzung öffnen. automatisch

```powershell <!-- Aladdin Generated Example -->
Enable-AzContextAutosave -Scope Process
```

## Parameter

### -DefaultProfile

Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, Mandanten und Abonnements

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

Bestimmt den Bereich von Kontextänderungen. So können Sie beispielsweise festlegen, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten. Mit dem Bereich vorgenommene Änderungen `CurrentUser` wirken sich auf alle PowerShell-Sitzungen aus, die vom Benutzer gestartet wurden. Wenn eine bestimmte Sitzung unterschiedliche Einstellungen aufweisen muss, verwenden Sie den Bereich `Process` .

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

Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

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

Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Common. Authentication. ContextAutosaveSettings

## Notizen

## Verwandte Links
