---
external help file: Az.StackHCI-help.xml
Module Name: Az.StackHCI
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackhci/test-azstackhciconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackHCI/help/Test-AzStackHCIConnection.md
ms.openlocfilehash: 34831104bc1b27aa115d56545c784e0fea856ba4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145497"
---
# Test-AzStackHCIConnection

## SYNOPSIS
Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.

## SYNTAX

```
Test-AzStackHCIConnection [[-EnvironmentName] <String>] [[-Region] <String>] [[-ComputerName] <String>]
 [[-Credential] <PSCredential>] [<CommonParameters>]
```

## BESCHREIBUNG
Test-AzStackHCIConnection überprüft die Konnektivität von lokalen gruppierten Knoten zu den Azure-Diensten, die für Azure Stack HCI erforderlich sind.

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
Aufrufen eines Clusterknotens Fehler im Fall eines Fehlers.

## PARAMETERS

### -ComputerName
Gibt einen der Clusterknoten in einem lokalen Cluster an, der für Azure registriert wird.

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

### -Credential
Gibt die Anmeldeinformationen für den Computernamen an.
Standard ist der aktuelle Benutzer, der das Cmdlet ausgeführt.

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
Der Standardwert ist AzureCloud.
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
Wird nur verwendet, wenn es sich um eine Canary-Region handelt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

## AUSGABEN

### PSCustomObject. Gibt die folgenden Eigenschaften in PSCustomObject zurück.
### Test: Name des ausgeführten Tests.
### EndpointTested: Im Test verwendeter Endpunkt.
### IsRequired: True or False
### Ergebnis: Erfolgreich oder fehlgeschlagen
### FailedNodes: Liste der Knoten, bei denen der Test fehlgeschlagen ist.
## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
