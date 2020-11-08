---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disconnect-azaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disconnect-AzAccount.md
ms.openlocfilehash: 23689d4e84228d4eaeaae82e2efe53b6450d44f9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166629"
---
# Disconnect-AzAccount

## Synopsis
Trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte, die diesem Konto zugeordnet sind.

## Syntax

### Contextname (Standard)
```
Disconnect-AzAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserID
```
Disconnect-AzAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipal
```
Disconnect-AzAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kontoobject
```
Disconnect-AzAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Contextobject
```
Disconnect-AzAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Disconnect-AzAccount-Cmdlet trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte (Abonnement-und Mandanteninformationen), die diesem Konto zugeordnet sind.
Nachdem Sie dieses Cmdlet ausgeführt haben, müssen Sie sich mit Connect-AzAccount erneut anmelden.

## Beispiele

### Beispiel 1: Abmelden des aktuellen Kontos
```powershell
PS C:\> Disconnect-AzAccount
```

Loggt sich vom Azure-Konto ab, das dem aktuellen Kontext zugeordnet ist.

### Beispiel 2: Abmelden des Kontos, das einem bestimmten Kontext zugeordnet ist
```powershell
PS C:\> Get-AzContext "Work" | Disconnect-AzAccount -Scope CurrentUser
```

Loggt das Konto ab, das dem angegebenen Kontext zugeordnet ist ("Arbeit" genannt). Da dadurch der Bereich "CurrentUser" verwendet wird, werden alle Anmeldeinformationen und Kontexte endgültig gelöscht.

### Beispiel 3: Abmelden eines bestimmten Benutzers
```powershell
PS C:\> Disconnect-AzAccount -Username 'user1@contoso.org'
```

Sie user1@contoso.org können die Anmeldeinformationen für "Benutzer" und alle diesem Benutzer zugeordneten Kontexte entfernen.

## Parameter

### -ApplicationId
ServicePrincipal-ID (Globally Unique ID)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases: SPN, ServicePrincipal

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Azurecontext
Kontext

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.Core.PSAzureContext
Parameter Sets: ContextObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Contextname
Name des Kontexts, von dem abgemeldet werden soll

```yaml
Type: System.String
Parameter Sets: ContextName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### -Inputobject
Das zu entfernende Kontoobjekt

```yaml
Type: Microsoft.Azure.Commands.Profile.Models.PSAzureRmAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Scope
Bestimmt den Bereich von Kontextänderungen, beispielsweise, ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Mandanten-Nr
Mandanten-ID (Globally Unique ID)

```yaml
Type: System.String
Parameter Sets: ServicePrincipal
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Username
Benutzername des Formulars ' user@contoso.org '

```yaml
Type: System.String
Parameter Sets: UserId
Aliases: Id, UserId

Required: True
Position: 0
Default value: None
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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount

### Microsoft. Azure. Commands. profile. Models. Core. PSAzureContext

## Ausgaben

### Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount

## Notizen

## Verwandte Links
