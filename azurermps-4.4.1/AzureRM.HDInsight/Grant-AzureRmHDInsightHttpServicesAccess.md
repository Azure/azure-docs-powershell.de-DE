---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 3F321D94-2B0B-48CA-9778-8090373F7FE0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: c447d8dbfb7ed0b1fb4cf2ac3ad4c63aa4666ad0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665053"
---
# <span data-ttu-id="aba6c-101">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aba6c-101">Grant-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="aba6c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aba6c-102">SYNOPSIS</span></span>
<span data-ttu-id="aba6c-103">Gewährt dem Cluster HTTP-Zugriff.</span><span class="sxs-lookup"><span data-stu-id="aba6c-103">Grants HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aba6c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aba6c-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-HttpCredential] <PSCredential>
 [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aba6c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aba6c-105">DESCRIPTION</span></span>
<span data-ttu-id="aba6c-106">Das Cmdlet **Grant-AzureRmHDInsightHttpServicesAccess** gewährt HTTP-Zugriff auf einen Azure HDInsight-Cluster mithilfe von ODBC, Ambari, Oozie und Webdiensten.</span><span class="sxs-lookup"><span data-stu-id="aba6c-106">The **Grant-AzureRmHDInsightHttpServicesAccess** cmdlet grants HTTP access to an Azure HDInsight cluster using ODBC, Ambari, Oozie and web services.</span></span>

## <span data-ttu-id="aba6c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aba6c-107">EXAMPLES</span></span>

### <span data-ttu-id="aba6c-108">Beispiel 1: Gewähren des HTTP-Zugriffs auf einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="aba6c-108">Example 1: Grant HTTP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightHttpServicesAccess `
            -ClusterName $clusterName `
            -HttpCredential $newClusterCreds
```

<span data-ttu-id="aba6c-109">Dieser Befehl gewährt HTTP-Zugriff auf den Cluster mit dem Namen "Your-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="aba6c-109">This command grants HTTP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="aba6c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="aba6c-110">PARAMETERS</span></span>

### <span data-ttu-id="aba6c-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="aba6c-111">-ClusterName</span></span>
<span data-ttu-id="aba6c-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="aba6c-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="aba6c-113">-HttpCredential</span><span class="sxs-lookup"><span data-stu-id="aba6c-113">-HttpCredential</span></span>
<span data-ttu-id="aba6c-114">Gibt die Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="aba6c-114">Specifies the cluster login (HTTP) credentials for the cluster.</span></span>

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

### <span data-ttu-id="aba6c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aba6c-115">-ResourceGroupName</span></span>
<span data-ttu-id="aba6c-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="aba6c-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="aba6c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aba6c-117">-DefaultProfile</span></span>
<span data-ttu-id="aba6c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aba6c-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aba6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aba6c-119">CommonParameters</span></span>
<span data-ttu-id="aba6c-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aba6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aba6c-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aba6c-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aba6c-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aba6c-122">INPUTS</span></span>

## <span data-ttu-id="aba6c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aba6c-123">OUTPUTS</span></span>

### <span data-ttu-id="aba6c-124">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="aba6c-124">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="aba6c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="aba6c-125">NOTES</span></span>

## <span data-ttu-id="aba6c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aba6c-126">RELATED LINKS</span></span>

[<span data-ttu-id="aba6c-127">REVOKE-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="aba6c-127">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>](./Revoke-AzureRmHDInsightHttpServicesAccess.md)


