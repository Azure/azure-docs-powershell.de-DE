---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 4de1e1467e1bc422666b7144f5d5fcd6c30c0c63
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930720"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten mit den Azure-Diensten, die von Azure Stack HCI erforderlich sind.

## SYNTAX

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## BESCHREIBUNG
Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten mit den Azure-Diensten, die von Azure Stack HCI erforderlich sind.

## BEISPIELE

### BEISPIEL 1
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Succeeded
```
Aufrufen eines Clusterknotens Erfolgsfall.

### BEISPIEL 2
```powershell
C:\PS\>Test-AzStackHCIConnection
Test: Connect to Azure Stack HCI Service
EndpointTested: https://azurestackhci-df.azurefd.net/health
IsRequired: True
Result: Failed
FailedNodes: Node1inClus2, Node2inClus3
```
Aufrufen eines Clusterknotens Fehlgeschlagener Fall.

## PARAMETER

### -ComputerName
Gibt einen der Clusterknoten im lokalen Cluster an, der bei Azure registriert wird.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Anmeldeinformationen
Gibt die Anmeldeinformationen für den Computernamen an.
Standardmäßig wird das Cmdlet vom aktuellen Benutzer ausgeführt.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EnvironmentName
Gibt die Azure-Umgebung an.
Standardmäßig ist AzureCloud.
Gültige Werte sind AzureCloud, AzureChinaCloud, AzureUSGovernment, AzureGermanCloud, AzurePPE

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: $AzureCloud
Accept pipeline input: False
Accept wildcard characters: False
```

### -Region
Gibt die Region an, mit der eine Verbindung hergestellt werden soll.
Wird nur verwendet, wenn es sich um eine Kanarenregion handelt.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

## AUSGABEN

### PSCustomObject. Gibt folgende Eigenschaften in PSCustomObject zurück.
### Test: Name des durchgeführten Tests.
### EndpunktTested: Endpunkt, der im Test verwendet wird.
### IsRequired: True or False
### Ergebnis: Erfolgreich oder fehlgeschlagen
### FailedNodes: Liste der Knoten, bei denen der Test fehlgeschlagen ist.
## NOTIZEN

## VERWANDTE LINKS
