---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: 8338f13829ebc3feff4c5a81fdfb3bd13934d90d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101944501"
---
# <span data-ttu-id="1cad9-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1cad9-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="1cad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cad9-102">SYNOPSIS</span></span>
<span data-ttu-id="1cad9-103">Erstellt eine Objektreplikationsrichtlinienregel.</span><span class="sxs-lookup"><span data-stu-id="1cad9-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="1cad9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1cad9-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1cad9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1cad9-105">DESCRIPTION</span></span>
<span data-ttu-id="1cad9-106">Das **Get-AzStorageObjectReplicationPolicy-Cmdlet** erstellt eine Objektreplikationsrichtlinienregel, die in Set-AzStorageObjectReplicationPolicy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1cad9-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="1cad9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1cad9-107">EXAMPLES</span></span>

### <span data-ttu-id="1cad9-108">Beispiel 1: Erstellen einer Objektreplikationsrichtlinienregel mit nur Quell- und Zielkonto und Anzeigen der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cad9-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="1cad9-109">Mit diesem Befehl wird eine Objektreplikationsrichtlinienregel mit nur quell- und zielkonto erstellt und die Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cad9-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="1cad9-110">Beispiel 2: Erstellen einer Objektreplikationsrichtlinienregel mit allen Eigenschaften und Anzeigen der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="1cad9-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="1cad9-111">Mit diesem Befehl wird eine Objektreplikationsrichtlinienregel mit allen Eigenschaften und deren Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1cad9-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="1cad9-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1cad9-112">PARAMETERS</span></span>

### <span data-ttu-id="1cad9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cad9-113">-DefaultProfile</span></span>
<span data-ttu-id="1cad9-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1cad9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cad9-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="1cad9-115">-DestinationContainer</span></span>
<span data-ttu-id="1cad9-116">Der Name des Zielcontainers, in den repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cad9-116">The Destination Container name to replicate to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cad9-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="1cad9-117">-MinCreationTime</span></span>
<span data-ttu-id="1cad9-118">Blobs, die nach der Uhrzeit erstellt wurden, werden an das Ziel repliziert.</span><span class="sxs-lookup"><span data-stu-id="1cad9-118">Blobs created after the time will be replicated to the destination..</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cad9-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="1cad9-119">-PrefixMatch</span></span>
<span data-ttu-id="1cad9-120">Filtert die Ergebnisse, um nur Blobs zu replizieren, deren Namen mit dem angegebenen Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="1cad9-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cad9-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="1cad9-121">-RuleId</span></span>
<span data-ttu-id="1cad9-122">Objektreplikationsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="1cad9-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="1cad9-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="1cad9-123">-SourceContainer</span></span>
<span data-ttu-id="1cad9-124">Der Name des Quellcontainers, aus dem repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1cad9-124">The Source Container name to replicate from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1cad9-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cad9-125">CommonParameters</span></span>
<span data-ttu-id="1cad9-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cad9-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cad9-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cad9-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cad9-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1cad9-128">INPUTS</span></span>

### <span data-ttu-id="1cad9-129">Keine</span><span class="sxs-lookup"><span data-stu-id="1cad9-129">None</span></span>

## <span data-ttu-id="1cad9-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1cad9-130">OUTPUTS</span></span>

### <span data-ttu-id="1cad9-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="1cad9-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="1cad9-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1cad9-132">NOTES</span></span>

## <span data-ttu-id="1cad9-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1cad9-133">RELATED LINKS</span></span>
