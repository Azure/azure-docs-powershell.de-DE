---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 606C5453-F841-4574-95F8-5CC29A4186E1
online version: https://docs.microsoft.com/powershell/module/az.hdinsight/get-azhdinsightproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Get-AzHDInsightProperty.md
ms.openlocfilehash: 9f0ff8ea56110da2fcdc34a973fe8968aa7a701f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947160"
---
# Get-AzHDInsightProperty

## SYNOPSIS
Ruft Eigenschaften zum HDInsight-Dienst ab, z. B. verfügbare Speicherorte und Kapazität.

## SYNTAX

```
Get-AzHDInsightProperty [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Get-AzHDInsightProperty-Cmdlet** ruft spezifische Eigenschaften für Azure HDInsight ab, z. B. die Liste der verfügbaren Speicherorte, HDInsight-Clusterversionen und die verfügbare Rechenkapazität.

## BEISPIELE

### Beispiel 1: Herunterladen der Eigenschaften eines Azure HDInsight-Clusters
```
PS C:\>Get-AzHDInsightProperty -Location "East US 2"
```

Dieser Befehl ruft Eigenschaften von einem HDInsight-Dienst vom Standort Ost USA 2 ab.

## PARAMETER

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

### -Location
Gibt den Speicherort an, für den HDInsight-Eigenschaften abgerufen werden.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine
## AUSGABEN

### Microsoft.Azure.Management.HDInsight.Models.AzureHDInsightCapabilities
## NOTIZEN

## VERWANDTE LINKS
