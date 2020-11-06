---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 670EAFC0-3F8D-4F3D-8B62-448F04378F8B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightHttpServicesAccess.md
ms.openlocfilehash: 795882aa421037252ca920093f1df39b4e242fce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479222"
---
# <span data-ttu-id="1f983-101">Revoke-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1f983-101">Revoke-AzureRmHDInsightHttpServicesAccess</span></span>

## <span data-ttu-id="1f983-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1f983-102">SYNOPSIS</span></span>
<span data-ttu-id="1f983-103">Deaktiviert den HTTP-Zugriff auf den Cluster.</span><span class="sxs-lookup"><span data-stu-id="1f983-103">Disables HTTP access to the cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f983-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1f983-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightHttpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1f983-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1f983-105">DESCRIPTION</span></span>
<span data-ttu-id="1f983-106">Das **REVOKE-AzureRmHDInsightHttpServicesAccess-** Cmdlet deaktiviert den HTTP-Zugriff auf einen Azure HDInsight-Cluster für ODBC-, Ambari-, Oozie-und webHCatalog-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="1f983-106">The **Revoke-AzureRmHDInsightHttpServicesAccess** cmdlet disables HTTP access to an Azure HDInsight cluster for ODBC, Ambari, Oozie and webHCatalog web services.</span></span>

## <span data-ttu-id="1f983-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1f983-107">EXAMPLES</span></span>

### <span data-ttu-id="1f983-108">Beispiel 1: Deaktivieren des HTTP-Zugriffs auf einen Cluster</span><span class="sxs-lookup"><span data-stu-id="1f983-108">Example 1: Disable HTTP access to a cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightHttpServicesAccess `
       -ClusterName "your-hadoop_001"
```

<span data-ttu-id="1f983-109">Mit diesem Befehl wird der HTTP-Zugriff auf den Cluster mit dem Namen your-hadoop_001 aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1f983-109">This command revokes HTTP access to the cluster named your-hadoop_001.</span></span>

## <span data-ttu-id="1f983-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f983-110">PARAMETERS</span></span>

### <span data-ttu-id="1f983-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1f983-111">-ClusterName</span></span>
<span data-ttu-id="1f983-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="1f983-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1f983-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f983-113">-ResourceGroupName</span></span>
<span data-ttu-id="1f983-114">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1f983-114">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1f983-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f983-115">-DefaultProfile</span></span>
<span data-ttu-id="1f983-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1f983-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f983-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f983-117">CommonParameters</span></span>
<span data-ttu-id="1f983-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f983-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f983-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f983-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f983-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1f983-120">INPUTS</span></span>

## <span data-ttu-id="1f983-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1f983-121">OUTPUTS</span></span>

### <span data-ttu-id="1f983-122">Microsoft. Azure. Management. HDInsight. Models. HttpConnectivitySettings</span><span class="sxs-lookup"><span data-stu-id="1f983-122">Microsoft.Azure.Management.HDInsight.Models.HttpConnectivitySettings</span></span>

## <span data-ttu-id="1f983-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="1f983-123">NOTES</span></span>

## <span data-ttu-id="1f983-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1f983-124">RELATED LINKS</span></span>

[<span data-ttu-id="1f983-125">Grant-AzureRmHDInsightHttpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1f983-125">Grant-AzureRmHDInsightHttpServicesAccess</span></span>](./Grant-AzureRmHDInsightHttpServicesAccess.md)


