---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 92E876FE-AA7B-43AA-915F-D02AC5CEF0CA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Use-AzureRmHDInsightCluster.md
ms.openlocfilehash: 01f9a2a9bae03606773c146f44f7e737fb9b613f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665040"
---
# <span data-ttu-id="dbde4-101">Use-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dbde4-101">Use-AzureRmHDInsightCluster</span></span>

## <span data-ttu-id="dbde4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbde4-102">SYNOPSIS</span></span>
<span data-ttu-id="dbde4-103">Wählt einen Cluster aus, der mit dem Invoke-RmAzureHDInsightHiveJob-Cmdlet verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbde4-103">Selects a cluster to be used with the Invoke-RmAzureHDInsightHiveJob cmdlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbde4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbde4-104">SYNTAX</span></span>

```
Use-AzureRmHDInsightCluster [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbde4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbde4-105">DESCRIPTION</span></span>
<span data-ttu-id="dbde4-106">Das Cmdlet **use-AzureRmHDInsightCluster** wählt den Azure HDInsight-Cluster für das Invoke-AzureRmHDInsightHiveJob-Cmdlet aus, das zum Übermitteln von Hive-Aufträgen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dbde4-106">The **Use-AzureRmHDInsightCluster** cmdlet selects the Azure HDInsight cluster for the Invoke-AzureRmHDInsightHiveJob cmdlet to use to submit Hive jobs.</span></span>

## <span data-ttu-id="dbde4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbde4-107">EXAMPLES</span></span>

### <span data-ttu-id="dbde4-108">Beispiel 1: Auswählen eines Clusters für die Übermittlung von Hive-Abfragen</span><span class="sxs-lookup"><span data-stu-id="dbde4-108">Example 1: Select a cluster for Hive query submission</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>Use-AzureRmHDInsightCluster `
            -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="dbde4-109">Mit diesem Befehl wird ein Cluster für die Übermittlung einer Hive-Abfrage ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dbde4-109">This command selects a cluster for a Hive query submission.</span></span>

## <span data-ttu-id="dbde4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbde4-110">PARAMETERS</span></span>

### <span data-ttu-id="dbde4-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="dbde4-111">-ClusterName</span></span>
<span data-ttu-id="dbde4-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="dbde4-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="dbde4-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="dbde4-113">-HttpCredential</span></span>
<span data-ttu-id="dbde4-114">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="dbde4-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: ClusterCredential

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dbde4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbde4-115">-ResourceGroupName</span></span>
<span data-ttu-id="dbde4-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="dbde4-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="dbde4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbde4-117">-DefaultProfile</span></span>
<span data-ttu-id="dbde4-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbde4-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbde4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbde4-119">CommonParameters</span></span>
<span data-ttu-id="dbde4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbde4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbde4-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbde4-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbde4-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbde4-122">INPUTS</span></span>

## <span data-ttu-id="dbde4-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbde4-123">OUTPUTS</span></span>

### <span data-ttu-id="dbde4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="dbde4-124">System.String</span></span>

## <span data-ttu-id="dbde4-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbde4-125">NOTES</span></span>

## <span data-ttu-id="dbde4-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbde4-126">RELATED LINKS</span></span>

[<span data-ttu-id="dbde4-127">Get-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dbde4-127">Get-AzureRmHDInsightCluster</span></span>](./Get-AzureRmHDInsightCluster.md)

[<span data-ttu-id="dbde4-128">Remove-AzureRmHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="dbde4-128">Remove-AzureRmHDInsightCluster</span></span>](./Remove-AzureRmHDInsightCluster.md)


