---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/remove-azurermaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disconnect-AzureRmAccount.md
ms.openlocfilehash: e72e326fd3251a9b3150b9def06e2fb60afb7d82
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664224"
---
# Disconnect-AzureRmAccount

## Synopsis
Trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte, die diesem Konto zugeordnet sind.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### Contextname (Standard)
```
Disconnect-AzureRmAccount [-ContextName <String>] [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UserID
```
Disconnect-AzureRmAccount [-Username] <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### ServicePrincipal
```
Disconnect-AzureRmAccount -ApplicationId <String> -TenantId <String> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kontoobject
```
Disconnect-AzureRmAccount [-InputObject] <PSAzureRmAccount> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Contextobject
```
Disconnect-AzureRmAccount [-AzureContext] <PSAzureContext> [-Scope <ContextModificationScope>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Disconnect-AzureRmAccount-Cmdlet trennt ein verbundenes Azure-Konto und entfernt alle Anmeldeinformationen und Kontexte (Abonnement-und Mandanteninformationen), die diesem Konto zugeordnet sind.

Nachdem Sie dieses Cmdlet ausgeführt haben, müssen Sie sich mit Connect-AzureRmAccount erneut anmelden.

## Beispiele

### Abmelden des aktuellen Kontos
```
PS C:\> Disconnect-AzureRmAccount
```

Loggt sich vom Azure-Konto ab, das dem aktuellen Kontext zugeordnet ist.

### Abmelden des Kontos, das einem bestimmten Kontext zugeordnet ist
```
PS C:\> Get-AzureRmContext "Work" | Disconnect-AzureRmAccount -Scope CurrentUser
```

Loggt das Konto ab, das dem angegebenen Kontext zugeordnet ist ("Arbeit" genannt). Da dadurch der Bereich "CurrentUser" verwendet wird, werden alle Anmeldeinformationen und Kontexte endgültig gelöscht.

### Abmelden eines bestimmten Benutzers
```
PS C:\> Disconnect-AzureRmAccount -Username 'user1@contoso.org'
```

Sie user1@contoso.org können die Anmeldeinformationen für "Benutzer" und alle diesem Benutzer zugeordneten Kontexte entfernen.

## Parameter

### -ApplicationId
ServicePrincipal-ID (Globally Unique ID)

```yaml
Type: String
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
Type: PSAzureContext
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
Type: String
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
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Das zu entfernende Kontoobjekt

```yaml
Type: PSAzureRmAccount
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
Type: ContextModificationScope
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
Type: String
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
Type: String
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
Type: SwitchParameter
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount

### Microsoft. Azure. Commands. profile. Models. PSAzureContext

## Ausgaben

### Microsoft. Azure. Commands. profile. Models. PSAzureRmAccount

## Notizen

## Verwandte Links
