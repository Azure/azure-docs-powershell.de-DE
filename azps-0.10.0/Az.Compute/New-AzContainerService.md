---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 522F5305-CDF6-41F2-803B-9EEA9E927668
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzContainerService.md
ms.openlocfilehash: b8f453200f2365272461373214ec92580212c4b1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844512"
---
# New-AzContainerService

## Synopsis
Erstellt einen Containerdienst.

## Syntax

```
New-AzContainerService [-ResourceGroupName] <String> [-Name] <String>
 [-ContainerService] <PSContainerService> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzContainerService** erstellt einen Containerdienst.
Geben Sie ein Containerdienst Objekt an, das Sie mithilfe des New-AzContainerServiceConfig-Cmdlets erstellen können.

## Beispiele

### Beispiel 1: Erstellen eines Container Diensts
```
PS C:\> New-AzResourceGroup -Name "ResourceGroup17" -Location "Australia Southeast" -Force
PS C:\> $Container = New-AzContainerServiceConfig -Location "Australia Southeast" -OrchestratorType "DCOS" -MasterDnsPrefix "MasterResourceGroup17" -AdminUsername "AcsLinuxAdmin" -SshPublicKey "<ssh-key>" | Add-AzContainerServiceAgentPoolProfile -Name "AgentPool01" -VmSize "Standard_A1" -DnsPrefix "APResourceGroup17"
PS C:\> New-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" -ContainerService $Container
```

Der erste Befehl erstellt eine Ressourcengruppe mit dem Namen ResourceGroup17 an der angegebenen Position.
Weitere Informationen finden Sie im New-AzResourceGroup-Cmdlet.

Der zweite Befehl erstellt einen Container und speichert ihn dann in der $Container-Variablen.
Weitere Informationen finden Sie im New-AzContainerServiceConfig-Cmdlet.

Der endgültige Befehl erstellt einen Containerdienst für den Container, der in $Container gespeichert ist.
Der Dienst hat den Namen csResourceGroup17.

## Parameter

### -AsJob
RRun-Cmdlet im Hintergrund, und geben Sie einen Auftrag zum Nachverfolgen des Fortschritts zurück.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ContainerService
Gibt ein Containerdienst Objekt an, das die Eigenschaften für den neuen Dienst enthält.
Verwenden Sie das New-AzContainerServiceConfig-Cmdlet, um ein **ContainerService** -Objekt zu erhalten.

```yaml
Type: PSContainerService
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Name
Gibt den Namen des vom Cmdlet erstellten Container Diensts an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, in der mit diesem Cmdlet der Containerdienst bereitgestellt wird.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### ContainerService
Der Parameter "ContainerService" akzeptiert den Wert vom Typ "ContainerService" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. Compute. Automation. Models. PSContainerService

## Notizen

## Verwandte Links

[Get-AzContainerService](./Get-AzContainerService.md)

[Neu – AzContainerServiceConfig](./New-AzContainerServiceConfig.md)

[Remove-AzContainerService](./Remove-AzContainerService.md)

[Update-AzContainerService](./Update-AzContainerService.md)


