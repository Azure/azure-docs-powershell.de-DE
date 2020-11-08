---
external help file: Microsoft.WindowsAzure.Commands.HDInsight.dll-Help.xml
ms.assetid: EE2ADA86-B2A3-4F6F-96EF-BB61D6DC550F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 338bef67e771bf211c063bf054e13e3844497850
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005970"
---
# Stop-AzureHDInsightJob

## Synopsis
Beendet einen HDInsight-Auftrag.

## Syntax

### Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (Standard)
```
Stop-AzureHDInsightJob -Cluster <String> [-Credential <PSCredential>] -JobId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### Starten von Tabelle Jobdetails auf einem HDInsight-Cluster (mit bestimmten Anmeldeinformationen für Abonnements)
```
Stop-AzureHDInsightJob [-Certificate <X509Certificate2>] [-HostedService <String>] -Cluster <String>
 [-Endpoint <Uri>] [-IgnoreSslErrors <Boolean>] -JobId <String> [-Subscription <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Diese Version von Azure PowerShell-HDInsight ist veraltet.
Diese Cmdlets werden vom 1. Januar 2017 entfernt.
Verwenden Sie bitte die neuere Version von Azure PowerShell-HDInsight.

Informationen zum Verwenden des neuen HDInsight zum Erstellen eines Clusters finden Sie unter [Erstellen von Linux-basierten Clustern in HDInsight mithilfe von Azure PowerShell](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-hadoop-create-linux-clusters-azure-powershell/) .
Informationen zum Übermitteln von Aufträgen mithilfe von Azure PowerShell und anderen Ansätzen finden Sie unter über [Mitteln von Hadoop-Aufträgen in HDInsight](https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) ( https://azure.microsoft.com/en-us/documentation/articles/hdinsight-submit-hadoop-jobs-programmatically/) .
Referenzinformationen zu Azure PowerShell-HDInsight finden Sie unter [Azure HDInsight-Cmdlets](https://msdn.microsoft.com/en-us/library/mt438705.aspx) ( https://msdn.microsoft.com/en-us/library/mt438705.aspx) .

Das Cmdlet **Stop-AzureHDInsightJob** beendet einen Azure HDInsight-Auftrag auf dem angegebenen Cluster.

## Beispiele

## Parameter

### -Zertifikat
Gibt das Verwaltungszertifikat für ein Azure-Abonnement an.

```yaml
Type: X509Certificate2
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Cert

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Cluster
Gibt einen Cluster an.
Dieses Cmdlet beendet einen Auftrag, der auf dem Cluster ausgeführt wird, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### – Anmeldeinformationen
Gibt die für den direkten HTTP-Zugriff auf einen Cluster zu verwendenden Anmeldeinformationen an.
Sie können diesen Parameter anstelle des *Subscription* -Parameters angeben, um den Zugriff auf einen Cluster zu authentifizieren.

```yaml
Type: PSCredential
Parameter Sets: Start jobDetails on an HDInsight Cluster
Aliases: Cred

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpunkt
Gibt den Endpunkt an, mit dem eine Verbindung mit Azure hergestellt werden soll.
Wenn Sie diesen Parameter nicht angeben, verwendet dieses Cmdlet den Standardendpunkt.

```yaml
Type: Uri
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -HostedService
Gibt den Namespace eines HDInsight-Diensts an, wenn Sie den Standardnamespace nicht verwenden möchten.

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: CloudServiceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -IgnoreSslErrors
Gibt an, ob SSL-Fehler (Secure Sockets Layer) ignoriert werden.

```yaml
Type: Boolean
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Gibt die ID des HDInsight-Auftrags an, der beendet werden soll.

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Abonnement
Gibt ein Abonnement an.
Dieses Cmdlet beendet einen Auftrag für das Abonnement, den dieser Parameter angibt.

```yaml
Type: String
Parameter Sets: Start jobDetails on an HDInsight Cluster (with Specific Subscription Credential)
Aliases: Sub

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureHDInsightJob](./Get-AzureHDInsightJob.md)

[Anfang-AzureHDInsightJob](./Start-AzureHDInsightJob.md)

[Wait-AzureHDInsightJob](./Wait-AzureHDInsightJob.md)


