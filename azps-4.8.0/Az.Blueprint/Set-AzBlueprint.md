---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165316"
---
# Set-AzBlueprint

## Synopsis
Aktualisieren einer Blueprint-Definition

## Syntax

### UpdateBlueprintBySubscription (Standard)
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### UpdateBlueprintByManagementGroup
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Aktualisieren Sie eine Blueprint-Definition, und speichern Sie Sie in der angegebenen Abonnement-oder Verwaltungsgruppe.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

Aktualisieren einer Blueprint-Definition mit neuen Parametern

## Parameter

### -Blueprintdatei
Pfad zu einer Blueprint-JSON-Datei auf dem Datenträger.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -ManagementGroupId
Verwaltungsgruppen-ID, in der die Blueprint-Definition steht oder gespeichert werden soll.

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Blueprint-Definitionsname

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Abonnement-Nr
Die Abonnement-ID, in der die Blueprint-Definition fest steht oder gespeichert werden soll.

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Blueprint. Models. PSBlueprint

## Notizen

## Verwandte Links
