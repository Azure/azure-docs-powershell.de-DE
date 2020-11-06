---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/revoke-azurermhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Revoke-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 32664beb1ffe7600756953294b1ec33f7d1d54ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500605"
---
# <span data-ttu-id="a32fa-101">Revoke-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a32fa-101">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="a32fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a32fa-102">SYNOPSIS</span></span>
<span data-ttu-id="a32fa-103">Deaktiviert den RDP-Zugriff auf einen Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="a32fa-103">Disables RDP access to a Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32fa-104">SYNTAX</span></span>

```
Revoke-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a32fa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a32fa-105">DESCRIPTION</span></span>
<span data-ttu-id="a32fa-106">Das **REVOKE-AzureRmHDInsightRdpServicesAccess-** Cmdlet deaktiviert den Zugriff auf einen Windows-basierten Azure HDInsight-Cluster (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="a32fa-106">The **Revoke-AzureRmHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="a32fa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a32fa-107">EXAMPLES</span></span>

### <span data-ttu-id="a32fa-108">Beispiel 1: Deaktivieren des RDP-Zugriffs auf einen angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="a32fa-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzureRmHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="a32fa-109">Mit diesem Befehl wird der RDP-Zugriff auf den Cluster "Your-Hadoop-001" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="a32fa-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="a32fa-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32fa-110">PARAMETERS</span></span>

### <span data-ttu-id="a32fa-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="a32fa-111">-ClusterName</span></span>
<span data-ttu-id="a32fa-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="a32fa-112">Specifies the name of the cluster.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32fa-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32fa-113">-DefaultProfile</span></span>
<span data-ttu-id="a32fa-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a32fa-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32fa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32fa-115">-ResourceGroupName</span></span>
<span data-ttu-id="a32fa-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a32fa-116">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a32fa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32fa-117">CommonParameters</span></span>
<span data-ttu-id="a32fa-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32fa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32fa-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32fa-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32fa-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a32fa-120">INPUTS</span></span>

### <span data-ttu-id="a32fa-121">Keine</span><span class="sxs-lookup"><span data-stu-id="a32fa-121">None</span></span>
<span data-ttu-id="a32fa-122">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a32fa-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a32fa-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a32fa-123">OUTPUTS</span></span>

### <span data-ttu-id="a32fa-124">System. void</span><span class="sxs-lookup"><span data-stu-id="a32fa-124">System.Void</span></span>

## <span data-ttu-id="a32fa-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="a32fa-125">NOTES</span></span>

## <span data-ttu-id="a32fa-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a32fa-126">RELATED LINKS</span></span>

[<span data-ttu-id="a32fa-127">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="a32fa-127">Grant-AzureRmHDInsightRdpServicesAccess</span></span>](./Grant-AzureRmHDInsightRdpServicesAccess.md)


