---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Get-AzureRmHDInsightOperationsManagementSuite.md
ms.openlocfilehash: 0f3e9e542ff1d05a9872096a784c8dabfed1910b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665056"
---
# Get-AzureRmHDInsightOperationsManagementSuite

## Synopsis
Ruft den Status der Operation Management Suite (OMS)-Installation auf dem Cluster ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmHDInsightOperationsManagementSuite [-Name] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzureRmHDInsightOperationsManagementSuite** " Ruft den Status der OMS-Installation in einem Azure HDInsight-Cluster ab. Wenn OMS aktiviert ist, gibt es auch die OMS-Arbeitsbereichs-ID zurück.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Die Operations Management Suite (OMS) ist im Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist. Die OMS-Arbeitsbereichs-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Beispiel 2
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'true', 'workspaceId':'1d364e89-bb71-4503-aa3d-a23535aea7bd'}
```

Die Operations Management Suite (OMS) ist im Cluster aktiviert, da die ClusterMonitoringEnabled-Eigenschaft true ist. Die OMS-Arbeitsbereichs-ID, in der die Protokolle fließen, ist 1d364e89-bb71-4503-aa3d-a23535aea7bd

### Beispiel 3
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

Die Operations Management Suite (OMS) ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft false ist.

### Beispiel 4
```
PS C:\> Get-AzureRmHDInsightOMS -Name testcluster -ResourceGroupName testrg

ClusterMonitoringEnabled

{'ClusterMonitoringEnabled':'false'}
```

Die Operations Management Suite (OMS) ist auf dem Cluster deaktiviert, da die ClusterMonitoringEnabled-Eigenschaft false ist.

## Parameter

### -Name
Der Name des Clusters, in dem der Status von Operations Management Suite (OMS) abgerufen werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ClusterName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ResourceGroupName
Die Ressourcengruppe des Clusters.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightOMS

## Notizen

## Verwandte Links

