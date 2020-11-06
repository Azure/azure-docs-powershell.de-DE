---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/Grant-AzureRmHDInsightRdpServicesAccess.md
ms.openlocfilehash: 22d2f4617e5b8a268de8518695d5217191a211df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504986"
---
# <span data-ttu-id="3872a-101">Grant-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3872a-101">Grant-AzureRmHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="3872a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3872a-102">SYNOPSIS</span></span>
<span data-ttu-id="3872a-103">Gewährt RDP-Zugriff auf den Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3872a-103">Grants RDP access to the Windows cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3872a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3872a-104">SYNTAX</span></span>

```
Grant-AzureRmHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3872a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3872a-105">DESCRIPTION</span></span>
<span data-ttu-id="3872a-106">Das Cmdlet **Grant-AzureRmHDInsightRdpServicesAccess** ermöglicht das Remote Desktop Protokoll (RDP) für den Zugriff auf einen Windows-basierten Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3872a-106">The **Grant-AzureRmHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="3872a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3872a-107">EXAMPLES</span></span>

### <span data-ttu-id="3872a-108">Beispiel 1: Gewähren des RDP-Zugriffs auf einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="3872a-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzureRmHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="3872a-109">Dieser Befehl gewährt RDP-Zugriff auf den Cluster mit dem Namen "Your-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="3872a-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="3872a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3872a-110">PARAMETERS</span></span>

### <span data-ttu-id="3872a-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="3872a-111">-ClusterName</span></span>
<span data-ttu-id="3872a-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="3872a-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="3872a-113">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="3872a-113">-RdpAccessExpiry</span></span>
<span data-ttu-id="3872a-114">Gibt den Ablauf als **DateTime** -Objekt für den RDP-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="3872a-114">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3872a-115">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="3872a-115">-RdpCredential</span></span>
<span data-ttu-id="3872a-116">Gibt die RDP-Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="3872a-116">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="3872a-117">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="3872a-117">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="3872a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3872a-118">-ResourceGroupName</span></span>
<span data-ttu-id="3872a-119">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3872a-119">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="3872a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3872a-120">-DefaultProfile</span></span>
<span data-ttu-id="3872a-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3872a-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3872a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3872a-122">CommonParameters</span></span>
<span data-ttu-id="3872a-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3872a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3872a-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3872a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3872a-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3872a-125">INPUTS</span></span>

## <span data-ttu-id="3872a-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3872a-126">OUTPUTS</span></span>

### <span data-ttu-id="3872a-127">System. void</span><span class="sxs-lookup"><span data-stu-id="3872a-127">System.Void</span></span>

## <span data-ttu-id="3872a-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="3872a-128">NOTES</span></span>

## <span data-ttu-id="3872a-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3872a-129">RELATED LINKS</span></span>

[<span data-ttu-id="3872a-130">REVOKE-AzureRmHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="3872a-130">Revoke-AzureRmHDInsightRdpServicesAccess</span></span>](./Revoke-AzureRmHDInsightRdpServicesAccess.md)


