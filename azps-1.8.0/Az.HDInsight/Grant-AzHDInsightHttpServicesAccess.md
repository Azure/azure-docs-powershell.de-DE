---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: c531135af3d118a9987a3c328eb4c06847e75fe6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819911"
---
# <span data-ttu-id="723cf-101">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="723cf-101">Grant-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="723cf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="723cf-102">SYNOPSIS</span></span>
<span data-ttu-id="723cf-103">Gewährt dem Cluster HTTP-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="723cf-103">Grants HTTP access to the cluster.</span></span>

## <span data-ttu-id="723cf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="723cf-104">SYNTAX</span></span>

```
Grant-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="723cf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="723cf-105">DESCRIPTION</span></span>
<span data-ttu-id="723cf-106">Das Cmdlet **Grant-AzHDInsightHttpServicesAccess** gewährt HTTP-Zugriff auf einen Azure HDInsight-Cluster mithilfe von ODBC, Ambari, Oozie und Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="723cf-106">The **Grant-AzHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="723cf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="723cf-107">EXAMPLES</span></span>

### <span data-ttu-id="723cf-108">Beispiel 1: Gewähren des HTTP-Zugriffs auf einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="723cf-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="723cf-109">Dieser Befehl gewährt HTTP-Zugriff auf den Cluster mit dem Namen "Your-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="723cf-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="723cf-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="723cf-110">PARAMETERS</span></span>

### <span data-ttu-id="723cf-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="723cf-111">-ClusterName</span></span>
<span data-ttu-id="723cf-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="723cf-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="723cf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="723cf-113">-DefaultProfile</span></span>
<span data-ttu-id="723cf-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="723cf-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="723cf-115">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="723cf-115">-HttpCredential</span></span>
<span data-ttu-id="723cf-116">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="723cf-116">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="723cf-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="723cf-117">-ResourceGroupName</span></span>
<span data-ttu-id="723cf-118">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="723cf-118">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="723cf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="723cf-119">CommonParameters</span></span>
<span data-ttu-id="723cf-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="723cf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="723cf-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="723cf-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="723cf-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="723cf-122">INPUTS</span></span>

### <span data-ttu-id="723cf-123">Keine</span><span class="sxs-lookup"><span data-stu-id="723cf-123">None</span></span>

## <span data-ttu-id="723cf-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="723cf-124">OUTPUTS</span></span>

### <span data-ttu-id="723cf-125">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="723cf-125">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="723cf-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="723cf-126">NOTES</span></span>

## <span data-ttu-id="723cf-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="723cf-127">RELATED LINKS</span></span>

[<span data-ttu-id="723cf-128">REVOKE-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="723cf-128">Revoke-AzHDInsightHttpServicesAccess</span></span>](./Revoke-AzHDInsightHttpServicesAccess.md)


