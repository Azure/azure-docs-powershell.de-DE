---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 1246C3AC-A123-4EA1-B99E-458A85789109
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodereport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeReport.md
ms.openlocfilehash: cc7beb921e09a2cdf1568e9cb693dd01f059e562
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171737"
---
# Get-AzAutomationDscNodeReport

## SYNOPSIS
Ruft Berichte ab, die von einem DSC-Knoten an die Automatisierung gesendet werden.

## SYNTAX

### ByAll (Standard)
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-StartTime <DateTimeOffset>] [-EndTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ByLatest
```
Get-AzAutomationDscNodeReport -NodeId <Guid> [-Latest] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ById
```
Get-AzAutomationDscNodeReport -NodeId <Guid> -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzAutomationDscNodeReport"** ruft Berichte ab, die von einem Knoten der APS Desired State Configuration (DSC) an die Azure Automation gesendet werden.

## BEISPIELE

### Beispiel 1: Alle Berichte für einen DSC-Knoten erhalten
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id
```

Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.
Der Befehl speichert dieses Objekt in der $Node Variable.
Der zweite Befehl ruft Metadaten für alle Berichte ab, die vom DSC-Knoten "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet werden.
Der Befehl gibt den Knoten mithilfe der **Id-Eigenschaft** des $Node an.

### Beispiel 2: Erhalten eines Berichts für einen DSC-Knoten nach Berichts-ID
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Id c0a1718e-d8be-4fa3-91b6-82e1d3a36298
```

Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.
Der Befehl speichert dieses Objekt in der $Node Variable.
Der zweite Befehl ruft Metadaten für den Bericht ab, der durch die angegebene ID identifiziert wird, die vom Knoten "DSC" namens "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet wird.

### Beispiel 3: Erhalten des neuesten Berichts für einen DSC-Knoten
```
PS C:\>$Node = Get-AzAutomationDscNode -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -Name "Computer14"
PS C:\> Get-AzAutomationDscNodeReport -ResourceGroupName "ResourceGroup03" -AutomationAccountName "Contoso17" -NodeId $Node.Id -Latest
```

Der erste Befehl ruft den DSC-Knoten für den Computer namens "Computer14" im Automatisierungskonto namens "Contoso17" ab.
Der Befehl speichert dieses Objekt in der $Node Variable.
Der zweite Befehl ruft Metadaten für den neuesten Bericht ab, der vom Knoten "DSC" namens "Computer14" an das Automatisierungskonto namens "Contoso17" gesendet wurde.

## PARAMETERS

### -AutomationAccountName
Gibt den Namen eines Automatisierungskontos an.
Dieses Cmdlet exportiert Berichte für einen DSC-Knoten, der zu dem Konto gehört, das dieser Parameter angibt.

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

### -EndTime
Gibt eine Endzeit an.
Dieses Cmdlet ruft Berichte ab, die die Automatisierung vor diesem Zeitpunkt erhalten hat.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ID
Gibt die eindeutige ID des DSC-Knotenberichts an, den dieses Cmdlet erhalten soll.

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases: ReportId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Latest
Gibt an, dass dieses Cmdlet nur den neuesten DSC-Bericht für den angegebenen Knoten erhält.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByLatest
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NodeId
Gibt die eindeutige ID des DSC-Knotens an, für den dieses Cmdlet Berichte erhält.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Ressourcengruppe an, die den DSC-Knoten enthält, für den dieses Cmdlet Berichte erhält.

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

### -StartTime
Gibt eine Startzeit an.
Dieses Cmdlet ruft Berichte ab, die Automatisierung nach diesem Zeitpunkt erhalten hat.

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.Guid

### System.Nullable'1[[System.DateTimeOffset, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Automation.Model.DscNode

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Export-AzAutomationDscNodeReportContent](./Export-AzAutomationDscNodeReportContent.md)


