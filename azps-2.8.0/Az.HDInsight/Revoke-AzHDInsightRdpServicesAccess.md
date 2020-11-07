---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 8C6D9533-68FD-4AFF-91FB-8307A8C8EAEB
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/revoke-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Revoke-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 7f5fcb8dcfbb325b8bc0381b3c943e550fe27e62
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651034"
---
# <span data-ttu-id="1219d-101">Revoke-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1219d-101">Revoke-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="1219d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1219d-102">SYNOPSIS</span></span>
<span data-ttu-id="1219d-103">Deaktiviert den RDP-Zugriff auf einen Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="1219d-103">Disables RDP access to a Windows cluster.</span></span>

## <span data-ttu-id="1219d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1219d-104">SYNTAX</span></span>

```
Revoke-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1219d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1219d-105">DESCRIPTION</span></span>
<span data-ttu-id="1219d-106">Das **REVOKE-AzHDInsightRdpServicesAccess-** Cmdlet deaktiviert den Zugriff auf einen Windows-basierten Azure HDInsight-Cluster (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="1219d-106">The **Revoke-AzHDInsightRdpServicesAccess** cmdlet disables Remote Desktop Protocol (RDP) access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="1219d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1219d-107">EXAMPLES</span></span>

### <span data-ttu-id="1219d-108">Beispiel 1: Deaktivieren des RDP-Zugriffs auf einen angegebenen Cluster</span><span class="sxs-lookup"><span data-stu-id="1219d-108">Example 1: Disable RDP access to a specified cluster</span></span>
```
PS C:\>Revoke-AzHDInsightRdpServicesAccess -ClusterName "your-hadoop-001"
```

<span data-ttu-id="1219d-109">Mit diesem Befehl wird der RDP-Zugriff auf den Cluster "Your-Hadoop-001" aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="1219d-109">This command revokes RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="1219d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1219d-110">PARAMETERS</span></span>

### <span data-ttu-id="1219d-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="1219d-111">-ClusterName</span></span>
<span data-ttu-id="1219d-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="1219d-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="1219d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1219d-113">-DefaultProfile</span></span>
<span data-ttu-id="1219d-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1219d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1219d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1219d-115">-ResourceGroupName</span></span>
<span data-ttu-id="1219d-116">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="1219d-116">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="1219d-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1219d-117">CommonParameters</span></span>
<span data-ttu-id="1219d-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1219d-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1219d-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1219d-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1219d-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1219d-120">INPUTS</span></span>

### <span data-ttu-id="1219d-121">Keine</span><span class="sxs-lookup"><span data-stu-id="1219d-121">None</span></span>

## <span data-ttu-id="1219d-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1219d-122">OUTPUTS</span></span>

### <span data-ttu-id="1219d-123">System. void</span><span class="sxs-lookup"><span data-stu-id="1219d-123">System.Void</span></span>

## <span data-ttu-id="1219d-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="1219d-124">NOTES</span></span>

## <span data-ttu-id="1219d-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1219d-125">RELATED LINKS</span></span>

[<span data-ttu-id="1219d-126">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="1219d-126">Grant-AzHDInsightRdpServicesAccess</span></span>](./Grant-AzHDInsightRdpServicesAccess.md)


