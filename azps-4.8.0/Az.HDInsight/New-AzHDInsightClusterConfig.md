---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 2C06626F-E5A9-48C2-AEA2-B448AD254C2E
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightclusterconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightClusterConfig.md
ms.openlocfilehash: 66857c9d12bb23ffdccb893b8fae8bfc7c6e0f4f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009281"
---
# New-AzHDInsightClusterConfig

## Synopsis
Erstellt ein nicht persistentes Cluster Konfigurationsobjekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.

## Syntax

```
New-AzHDInsightClusterConfig [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultStorageAccountType <StorageType>] [-OozieMetastore <AzureHDInsightMetastore>]
 [-HiveMetastore <AzureHDInsightMetastore>] [-HeadNodeSize <String>] [-WorkerNodeSize <String>]
 [-EdgeNodeSize <String>] [-ZookeeperNodeSize <String>] [-ClusterType <String>] [-ClusterTier <Tier>]
 [-ObjectId <Guid>] [-ApplicationId <Guid>] [-CertificateFileContents <Byte[]>] [-CertificateFilePath <String>]
 [-CertificatePassword <String>] [-AadTenantId <Guid>] [-MinSupportedTlsVersion <String>]
 [-AssignedIdentity <String>] [-EncryptionAlgorithm <String>] [-EncryptionKeyName <String>]
 [-EncryptionKeyVersion <String>] [-EncryptionVaultUri <String>] [-PublicNetworkAccessType <String>]
 [-OutboundPublicNetworkAccessType <String>] [-EncryptionInTransit <Boolean>] [-EncryptionAtHost <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzHDInsightClusterConfig** erstellt ein nicht beibehaltenes Objekt, das eine Azure HDInsight-Cluster Konfiguration beschreibt.

## Beispiele

### Beispiel 1: Erstellen eines Cluster Konfigurationsobjekts
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container002"

# Cluster configuration info
PS C:\> $location = "East US 2"
PS C:\> $clusterResourceGroupName = "Group"
PS C:\> $clusterName = "your-hadoop-002"
PS C:\> $clusterCreds = Get-Credential

# If the cluster's resource group doesn't exist yet, run:
#   New-AzResourceGroup -Name $clusterResourceGroupName -Location $location

# Create the cluster
PS C:\> New-AzHDInsightClusterConfig `
            | Add-AzHDInsightStorage `
                -StorageAccountName "$secondStorageAccountName.blob.core.contoso.net" `
                -StorageAccountKey $key2 `
            | New-AzHDInsightCluster `
                -ClusterType Hadoop `
                -OSType Windows `
                -ClusterSizeInNodes 4 `
                -ResourceGroupName $clusterResourceGroupName `
                -ClusterName $clusterName `
                -HttpCredential $clusterCreds `
                -Location $location `
                -DefaultStorageAccountName "$storageAccountName.blob.core.contoso.net" `
                -DefaultStorageAccountKey $storageAccountKey `
                -DefaultStorageContainer $storageContainer
```

Mit diesem Befehl wird ein Cluster Konfigurationsobjekt erstellt.

## Parameter

### -AadTenantId
Gibt die Azure AD-Mandanten-ID an, die beim Zugriff auf den Azure Data Lake Store verwendet wird.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ApplicationId
Ruft die Dienstprinzipal-Anwendungs-ID für den Zugriff auf Azure Data Lake ab oder legt diese fest.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -AssignedIdentity
Ruft die zugewiesene Identität ab oder legt diese fest.

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

### -CertificateFileContents
Gibt den Dateiinhalt des Zertifikats an, das beim Zugriff auf den Azure Data Lake Store verwendet wird.

```yaml
Type: System.Byte[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -CertificateFilePath
Gibt den Dateipfad zu dem Zertifikat an, das zur Authentifizierung als Dienstprinzipal verwendet wird.
Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.

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

### -CertificatePassword
Gibt das Kennwort für das Zertifikat an, das für die Authentifizierung als Dienstprinzipal verwendet wird.
Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.

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

### -ClusterTier
Gibt die HDInsight-Clusterebene an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Standard
- Premium der Standardwert ist Standard.
Die Premium-Stufe kann nur mit Linux-Clustern verwendet werden und ermöglicht die Verwendung einiger neuer Funktionen.

```yaml
Type: Microsoft.Azure.Management.HDInsight.Models.Tier
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Clustertyp
Gibt den Typ des zu erstellende Clusters an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:
- Hadoop
- HBase
- Sturm
- Funken
- INTERACTIVEHIVE
- Kafka
- RServer

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -DefaultStorageAccountKey
Gibt den Kontoschlüssel für das standardmäßige Azure Storage-Konto an, das vom HDInsight-Cluster verwendet wird.

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

### -DefaultStorageAccountName
Gibt den Namen des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird.

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

### -DefaultStorageAccountType
Gibt den Typ des Standardspeicher Kontos an, das vom HDInsight-Cluster verwendet wird. Mögliche Werte sind AzureStorage und AzureDataLakeStore.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.Management.StorageType
Parameter Sets: (All)
Aliases:
Accepted values: AzureStorage, AzureDataLakeStore

Required: False
Position: Named
Default value: AzureStorage
Accept pipeline input: False
Accept wildcard characters: False
```

### -EdgeNodeSize
Gibt die Größe des virtuellen Computers für den Edge-Knoten an. Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an. Dieser Parameter ist nur für RServer-Cluster gültig.

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

### -EncryptionAlgorithm
Ruft den Verschlüsselungsalgorithmus ab oder legt ihn fest.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: RSA-OAEP, RSA-OAEP-256, RSA1_5

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionAtHost
Ruft das Flag ab, das angibt, ob die Verschlüsselung beim Host aktiviert werden soll, oder legt dieses fest.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionInTransit
Ruft das Flag ab, das angibt, ob die Verschlüsselung bei der Übertragung aktiviert werden soll, oder legt dieses fest.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -EncryptionKeyName
Ruft den Namen des Verschlüsselungsschlüssels ab oder legt ihn fest.

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

### -EncryptionKeyVersion
Ruft die Version des Verschlüsselungsschlüssels ab oder legt diese fest.

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

### -EncryptionVaultUri
Ruft den Verschlüsselungs Tresor-URI ab oder legt ihn fest.

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

### -HeadNodeSize
Gibt die Größe des virtuellen Computers für den Head-Knoten an.
Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.

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

### -HiveMetastore
Gibt den metastore an, in dem die Struktur Metadaten gespeichert werden.
Sie können das Add-AzHDInsightMetastore-Cmdlet auch verwenden.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MinSupportedTlsVersion
Ruft die minimal unterstützte TLS-Version ab oder legt diese fest.

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

### -ObjectID
Gibt die Azure AD-Objekt-ID (eine GUID) des Azure AD-Dienst Prinzipals an, der den Cluster darstellt.
Der Cluster verwendet diesen beim Zugriff auf den Azure Data Lake Store.

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OozieMetastore
Gibt den metastore an, in dem Oozie-Metadaten gespeichert werden.
Alternativ können Sie das Cmdlet **Add-AzHDInsightMetastore** verwenden.

```yaml
Type: Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightMetastore
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutboundPublicNetworkAccessType
Ruft den ausgehenden Zugriffstyp für das öffentliche Netzwerk ab oder legt diesen fest.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: PublicLoadBalancer, UDR

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PublicNetworkAccessType
Ruft den Zugriffstyp für öffentliche Netzwerke ab oder legt diesen fest.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: InboundAndOutbound, OutboundOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WorkerNodeSize
Gibt die Größe des virtuellen Computers für den Worker-Knoten an.
Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.

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

### -ZookeeperNodeSize
Gibt die Größe des virtuellen Computers für den zoowärter-Knoten an.
Verwenden Sie Get-AzVMSize für akzeptable VM-Größen, und schauen Sie sich die HDInsight-Preisseite an.
Dieser Parameter ist nur für HBAs oder Storm-Cluster gültig.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightConfig

## Notizen

## Verwandte Links

[Add-AzHDInsightStorage](./Add-AzHDInsightStorage.md)


