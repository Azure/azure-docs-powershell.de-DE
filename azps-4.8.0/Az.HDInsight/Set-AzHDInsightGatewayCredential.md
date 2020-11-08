---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/set-azhdinsightgatewaycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Set-AzHDInsightGatewayCredential.md
ms.openlocfilehash: 5f5c8c193a352738f64d595188247bf0564bea43
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009825"
---
# Set-AzHDInsightGatewayCredential

## Synopsis
Legt die Gateway-http-Anmeldeinformationen eines Azure HDInsight-Clusters fest.

## Syntax

### SetByNameParameterSet (Standard)
```
Set-AzHDInsightGatewayCredential -Name <String> [-HttpCredential] <PSCredential> [-ResourceGroupName <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SetByInputObjectParameterSet
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -InputObject <AzureHDInsightCluster> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SetByResourceIdParameterSet
```
Set-AzHDInsightGatewayCredential [-HttpCredential] <PSCredential> [-ResourceGroupName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] -ResourceId <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Set-AzHDInsightGatewayCredential** " legt Gateway-Anmeldeinformationen eines Azure HDInsight-Clusters fest.

## Beispiele

### Beispiel 1
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Set-AzHDInsightGatewayCredential `
            -ClusterName $clusterName `
            -HttpCredential $clusterCreds
```

Mit diesem Befehl werden die Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" nach Name-Parametersatz festgelegt.

### Beispiel 2
```powershell
PS C:\> Set-AzHDInsightGatewayCredential `
            -ResourceId "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.HDInsight/clusters/your-hadoop-001" `
            -HttpCredential $clusterCreds
```

Mit diesem Befehl werden die Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" mithilfe des Parameters "resourcecode" festgelegt.

### Beispiel 3
```powershell
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Get-AzHDInsightCluster -ClusterName $clusterName | Set-AzHDInsightGatewayCredential `
            -HttpCredential $clusterCreds
```

Mit diesem Befehl werden Gateway-Anmeldeinformationen des Clusters "Your-Hadoop-001" nach Inputobject-Parametersatz festgelegt.

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -HttpCredential
Ruft die Anmeldung für den Benutzer des Clusters ab oder legt diese fest.

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Inputobject
Ruft das Eingabeobjekt ab oder legt dieses fest.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightCluster
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Ruft den Namen des Clusters ab oder legt ihn fest.

```yaml
Type: System.String
Parameter Sets: SetByNameParameterSet
Aliases: ClusterName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ruft den Namen der Ressourcengruppe ab oder legt ihn fest.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Ruft die Ressourcen-ID ab oder legt diese fest.

```yaml
Type: System.String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

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

### Keine

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. Management. AzureHDInsightGatewaySettings

## Notizen

## Verwandte Links
