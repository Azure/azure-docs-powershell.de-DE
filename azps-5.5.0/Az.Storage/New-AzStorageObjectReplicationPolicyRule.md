---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158073"
---
# <span data-ttu-id="26b3a-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="26b3a-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="26b3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26b3a-102">SYNOPSIS</span></span>
<span data-ttu-id="26b3a-103">Erstellt eine Regel für die Objektreplikationsrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="26b3a-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="26b3a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="26b3a-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26b3a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="26b3a-105">DESCRIPTION</span></span>
<span data-ttu-id="26b3a-106">Das **Cmdlet "Get-AzStorageObjectReplicationPolicy"** erstellt eine Richtlinie für die Objektreplikation, die im Set-AzStorageObjectReplicationPolicy verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="26b3a-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="26b3a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="26b3a-107">EXAMPLES</span></span>

### <span data-ttu-id="26b3a-108">Beispiel 1: Erstellen einer Regel für die Objektreplikationsrichtlinie, die nur ein Quell- und Zielkonto enthält, und Anzeigen der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26b3a-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="26b3a-109">Mit diesem Befehl wird eine Regel für die Objektreplikationrichtlinie erstellt, die nur das Quell- und Zielkonto enthält, und die Eigenschaften werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26b3a-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="26b3a-110">Beispiel 2: Erstellen einer Richtlinie für die Objektreplikation mit allen Eigenschaften und Anzeigen der Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="26b3a-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="26b3a-111">Mit diesem Befehl wird eine Richtlinie für die Objektreplikation mit allen Eigenschaften befehlen und deren Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="26b3a-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="26b3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26b3a-112">PARAMETERS</span></span>

### <span data-ttu-id="26b3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26b3a-113">-DefaultProfile</span></span>
<span data-ttu-id="26b3a-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="26b3a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26b3a-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="26b3a-115">-DestinationContainer</span></span>
<span data-ttu-id="26b3a-116">Der Name des Zielcontainers, in den repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26b3a-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="26b3a-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="26b3a-117">-MinCreationTime</span></span>
<span data-ttu-id="26b3a-118">Blobs, die nach dieser Zeit erstellt wurden, werden an das Ziel repliziert.</span><span class="sxs-lookup"><span data-stu-id="26b3a-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="26b3a-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="26b3a-119">-PrefixMatch</span></span>
<span data-ttu-id="26b3a-120">Filtert die Ergebnisse, um nur BLOBs zu replizieren, deren Namen mit dem angegebenen Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="26b3a-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="26b3a-121">-RuleId</span><span class="sxs-lookup"><span data-stu-id="26b3a-121">-RuleId</span></span>
<span data-ttu-id="26b3a-122">Objektreplikationsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="26b3a-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="26b3a-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="26b3a-123">-SourceContainer</span></span>
<span data-ttu-id="26b3a-124">Der Name des Quellcontainers, aus dem repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="26b3a-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="26b3a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26b3a-125">CommonParameters</span></span>
<span data-ttu-id="26b3a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26b3a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26b3a-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26b3a-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26b3a-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="26b3a-128">INPUTS</span></span>

### <span data-ttu-id="26b3a-129">Keine</span><span class="sxs-lookup"><span data-stu-id="26b3a-129">None</span></span>

## <span data-ttu-id="26b3a-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="26b3a-130">OUTPUTS</span></span>

### <span data-ttu-id="26b3a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="26b3a-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="26b3a-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="26b3a-132">NOTES</span></span>

## <span data-ttu-id="26b3a-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="26b3a-133">RELATED LINKS</span></span>
