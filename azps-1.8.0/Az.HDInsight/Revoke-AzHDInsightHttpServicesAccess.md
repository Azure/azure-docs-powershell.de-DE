---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsighthttpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightHttpServicesAccess.md
ms.openlocfilehash: ddc269d342a6119187ec578e236a30c928d9ea3f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93819864"
---
# <span data-ttu-id="68513-101">Revoke-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="68513-101">Revoke-AzHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="68513-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68513-102">SYNOPSIS</span></span>
<span data-ttu-id="68513-103">Deaktiviert den HTTP-Zugriff auf den Cluster.</span><span class="sxs-lookup"><span data-stu-id="68513-103">Disables HTTP access to the cluster.</span></span>

## <span data-ttu-id="68513-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68513-104">SYNTAX</span></span>

```
Revoke-AzHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="68513-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68513-105">DESCRIPTION</span></span>
<span data-ttu-id="68513-106">Das **REVOKE-AzHDInsightHttpServicesAccess-** Cmdlet deaktiviert den HTTP-Zugriff auf einen Azure HDInsight-Cluster für ODBC-, Ambari-, Oozie-und webHCatalog-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="68513-106">The **Revoke-AzHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="68513-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68513-107">EXAMPLES</span></span>

### <span data-ttu-id="68513-108">Beispiel 1: Deaktivieren des HTTP-Zugriffs auf einen Cluster</span><span class="sxs-lookup"><span data-stu-id="68513-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="68513-109">Mit diesem Befehl wird der HTTP-Zugriff auf den Cluster mit dem Namen your-hadoop_001 aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="68513-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="68513-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="68513-110">PARAMETERS</span></span>

### <span data-ttu-id="68513-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="68513-111">-ClusterName</span></span>
<span data-ttu-id="68513-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="68513-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="68513-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68513-113">-DefaultProfile</span></span>
<span data-ttu-id="68513-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68513-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68513-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68513-115">-ResourceGroupName</span></span>
<span data-ttu-id="68513-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="68513-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="68513-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68513-117">CommonParameters</span></span>
<span data-ttu-id="68513-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68513-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68513-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68513-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68513-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68513-120">INPUTS</span></span>

### <span data-ttu-id="68513-121">Keine</span><span class="sxs-lookup"><span data-stu-id="68513-121">None</span></span>

## <span data-ttu-id="68513-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68513-122">OUTPUTS</span></span>

### <span data-ttu-id="68513-123">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="68513-123">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="68513-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="68513-124">NOTES</span></span>

## <span data-ttu-id="68513-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68513-125">RELATED LINKS</span></span>

[<span data-ttu-id="68513-126">Grant-AzHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="68513-126">Grant-AzHDInsightHttpServicesAccess</span></span>](./Grant-AzHDInsightHttpServicesAccess.md)


