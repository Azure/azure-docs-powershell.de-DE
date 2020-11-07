---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 6288DD8A-FF23-4B12-A065-856DBAE200E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/grant-azhdinsightrdpservicesaccess
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Grant-AzHDInsightRdpServicesAccess.md
ms.openlocfilehash: 6cbe18311f4a14b31bc50f7c0b95266bf99d4a40
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651063"
---
# <span data-ttu-id="6b33f-101">Grant-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6b33f-101">Grant-AzHDInsightRdpServicesAccess</span></span>

## <span data-ttu-id="6b33f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b33f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b33f-103">Gewährt RDP-Zugriff auf den Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6b33f-103">Grants RDP access to the Windows cluster.</span></span>

## <span data-ttu-id="6b33f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b33f-104">SYNTAX</span></span>

```
Grant-AzHDInsightRdpServicesAccess [-ClusterName] <String> [-RdpCredential] <PSCredential>
 [-RdpAccessExpiry] <DateTime> [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b33f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b33f-105">DESCRIPTION</span></span>
<span data-ttu-id="6b33f-106">Das Cmdlet **Grant-AzHDInsightRdpServicesAccess** ermöglicht das Remote Desktop Protokoll (RDP) für den Zugriff auf einen Windows-basierten Azure HDInsight-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6b33f-106">The **Grant-AzHDInsightRdpServicesAccess** cmdlet enables Remote Desktop Protocol (RDP) to access to a Windows-based Azure HDInsight cluster.</span></span>

## <span data-ttu-id="6b33f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b33f-107">EXAMPLES</span></span>

### <span data-ttu-id="6b33f-108">Beispiel 1: Gewähren des RDP-Zugriffs auf einen Azure HDInsight-Cluster</span><span class="sxs-lookup"><span data-stu-id="6b33f-108">Example 1: Grant RDP access to an Azure HDInsight cluster</span></span>
```
PS C:\># Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

PS C:\> Grant-AzHDInsightRdpServicesAccess `
            -ClusterName $clusterName `
            -RdpCredential $newRdpCreds `
            -RdpAccessExpiry $newRdpExpiry
```

<span data-ttu-id="6b33f-109">Dieser Befehl gewährt RDP-Zugriff auf den Cluster mit dem Namen "Your-Hadoop-001".</span><span class="sxs-lookup"><span data-stu-id="6b33f-109">This command grants RDP access to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="6b33f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b33f-110">PARAMETERS</span></span>

### <span data-ttu-id="6b33f-111">-Clustername</span><span class="sxs-lookup"><span data-stu-id="6b33f-111">-ClusterName</span></span>
<span data-ttu-id="6b33f-112">Gibt den Namen des Clusters an.</span><span class="sxs-lookup"><span data-stu-id="6b33f-112">Specifies the name of the cluster.</span></span>

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

### <span data-ttu-id="6b33f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b33f-113">-DefaultProfile</span></span>
<span data-ttu-id="6b33f-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6b33f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b33f-115">-RdpAccessExpiry</span><span class="sxs-lookup"><span data-stu-id="6b33f-115">-RdpAccessExpiry</span></span>
<span data-ttu-id="6b33f-116">Gibt den Ablauf als **DateTime** -Objekt für den RDP-Zugriff auf einen Cluster an.</span><span class="sxs-lookup"><span data-stu-id="6b33f-116">Specifies the expiration, as a **DateTime** object, for RDP access to a cluster.</span></span>

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

### <span data-ttu-id="6b33f-117">-RdpCredential</span><span class="sxs-lookup"><span data-stu-id="6b33f-117">-RdpCredential</span></span>
<span data-ttu-id="6b33f-118">Gibt die RDP-Anmeldeinformationen für den Cluster an.</span><span class="sxs-lookup"><span data-stu-id="6b33f-118">Specifies the RDP credentials for the cluster.</span></span>
<span data-ttu-id="6b33f-119">Dies gilt nur für Windows-Cluster.</span><span class="sxs-lookup"><span data-stu-id="6b33f-119">This is only for Windows clusters.</span></span>

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

### <span data-ttu-id="6b33f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b33f-120">-ResourceGroupName</span></span>
<span data-ttu-id="6b33f-121">Gibt den Namen der Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6b33f-121">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6b33f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b33f-122">CommonParameters</span></span>
<span data-ttu-id="6b33f-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b33f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b33f-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b33f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b33f-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b33f-125">INPUTS</span></span>

### <span data-ttu-id="6b33f-126">Keine</span><span class="sxs-lookup"><span data-stu-id="6b33f-126">None</span></span>

## <span data-ttu-id="6b33f-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b33f-127">OUTPUTS</span></span>

### <span data-ttu-id="6b33f-128">System. void</span><span class="sxs-lookup"><span data-stu-id="6b33f-128">System.Void</span></span>

## <span data-ttu-id="6b33f-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b33f-129">NOTES</span></span>

## <span data-ttu-id="6b33f-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b33f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6b33f-131">REVOKE-AzHDInsightRdpServicesAccess</span><span class="sxs-lookup"><span data-stu-id="6b33f-131">Revoke-AzHDInsightRdpServicesAccess</span></span>](./Revoke-AzHDInsightRdpServicesAccess.md)


