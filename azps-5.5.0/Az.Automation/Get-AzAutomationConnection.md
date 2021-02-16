---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D12007E8-8693-45B9-8919-CF8A4BA63AAA
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationConnection.md
ms.openlocfilehash: 3cf369be5c7d62d9e4b85002906d55f34a47e40c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100168457"
---
# Get-AzAutomationConnection

## SYNOPSIS
Ruft eine Automatisierungsverbindung ab.

## SYNTAX

### ByAll (Standard)
```
Get-AzAutomationConnection [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionName
```
Get-AzAutomationConnection [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByConnectionTypeName
```
Get-AzAutomationConnection [-ConnectionTypeName] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzAutomationConnection"** ruft mindestens eine Azure-Automatisierungsverbindung ab.
Standardmäßig ruft dieses Cmdlet alle Verbindungen ab.
Geben Sie den Namen einer Verbindung an, um eine bestimmte Verbindung herzustellen.
Geben Sie den Namen des Verbindungstyps an, um alle Verbindungen eines bestimmten Typs zu erhalten.

## BEISPIELE

### Beispiel 1: Alle Verbindungen erhalten
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

Dieser Befehl ruft Metadaten für alle Verbindungen im Automatisierungskonto namens "Contoso17" ab.

### Beispiel 2: Alle Verbindungen eines Typs erhalten
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -ConnectionTypeName "SqlServer"
```

Dieser Befehl ruft Metadaten für Verbindungen im Automatisierungskonto namens "Contoso17" ab.
Dieser Befehl ruft Verbindungen vom Typ "SqlServer" ab.

### Beispiel 3: Herstellen einer Verbindung
```
PS C:\>Get-AzAutomationConnection -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoConnection"
```

Dieser Befehl ruft Metadaten für die Verbindung namens "ContosoConnection" ab.

## PARAMETERS

### -AutomationAccountName
Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Verbindungen erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionTypeName
Gibt den Namen eines Verbindungstyps an, für den dieses Cmdlet Verbindungen abruft.

```yaml
Type: System.String
Parameter Sets: ByConnectionTypeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Name
Gibt den Namen einer Verbindung an, die von diesem Cmdlet abgerufen wird.

```yaml
Type: System.String
Parameter Sets: ByConnectionName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Verbindungen erhält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.Connection

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzAutomationConnection](./New-AzAutomationConnection.md)

[Remove-AzAutomationConnection](./Remove-AzAutomationConnection.md)


