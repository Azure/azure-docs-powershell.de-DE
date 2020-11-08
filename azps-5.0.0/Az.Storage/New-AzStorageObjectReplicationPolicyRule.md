---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/New-azstorageobjectreplicationpolicyrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageObjectReplicationPolicyRule.md
ms.openlocfilehash: c8d41300250e41548cf949248b02c819b7da497f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177364"
---
# <span data-ttu-id="f5f97-101">New-AzStorageObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f5f97-101">New-AzStorageObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="f5f97-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f5f97-102">SYNOPSIS</span></span>
<span data-ttu-id="f5f97-103">Erstellt eine Objekt Replikationsrichtlinien Regel.</span><span class="sxs-lookup"><span data-stu-id="f5f97-103">Creates an object replication policy rule.</span></span>

## <span data-ttu-id="f5f97-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5f97-104">SYNTAX</span></span>

```
New-AzStorageObjectReplicationPolicyRule -SourceContainer <String> -DestinationContainer <String>
 [-PrefixMatch <String[]>] [-MinCreationTime <DateTime>] [-RuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5f97-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5f97-105">DESCRIPTION</span></span>
<span data-ttu-id="f5f97-106">Das Cmdlet " **Get-AzStorageObjectReplicationPolicy** " erstellt eine Objekt Replikationsrichtlinien Regel, die in Set-AzStorageObjectReplicationPolicy-Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="f5f97-106">The **Get-AzStorageObjectReplicationPolicy** cmdlet creates an object replication policy rule, which will be used in Set-AzStorageObjectReplicationPolicy cmdlet.</span></span>

## <span data-ttu-id="f5f97-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f5f97-107">EXAMPLES</span></span>

### <span data-ttu-id="f5f97-108">Beispiel 1: Erstellen einer Objekt Replikationsrichtlinien Regel mit nur Quell-und Ziel Konto und Anzeigen der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5f97-108">Example 1: Create an object replication policy rule with only source and destination account, and show its properties</span></span>
```
PS C:\> $rule1 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src1 -DestinationContainer dest1 

PS C:\> $rule1

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src1            dest1                {}
```

<span data-ttu-id="f5f97-109">Mit diesem Befehl wird eine Objekt Replikationsrichtlinien Regel mit nur Quell-und Ziel Konto erstellt, und die zugehörigen Eigenschaften werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5f97-109">This command creates an object replication policy rule with only source and destination account, and show its properties.</span></span>

### <span data-ttu-id="f5f97-110">Beispiel 2: Erstellen einer Objekt Replikationsrichtlinien Regel mit allen Eigenschaften und Anzeigen der zugehörigen Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="f5f97-110">Example 2: Create an object replication policy rule with all properties, and show its properties</span></span>
```
PS C:\> $rule2 = New-AzStorageObjectReplicationPolicyRule -SourceContainer src -DestinationContainer dest -MinCreationTime 2019-01-01T16:00:00Z -PrefixMatch a,abc,dd

PS C:\> $rule2

RuleId SourceContainer DestinationContainer Filters.PrefixMatch Filters.MinCreationTime
------ --------------- -------------------- ------------------- -----------------------
       src             dest                 {a, abc, dd}        2019-01-01T16:00:00Z
```

<span data-ttu-id="f5f97-111">Mit diesem Befehl wird eine Objekt Replikationsrichtlinien Regel mit allen Eigenschaften und deren Eigenschaften angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f5f97-111">This command an object replication policy rule with all properties, and show its properties.</span></span>

## <span data-ttu-id="f5f97-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5f97-112">PARAMETERS</span></span>

### <span data-ttu-id="f5f97-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5f97-113">-DefaultProfile</span></span>
<span data-ttu-id="f5f97-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f5f97-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5f97-115">-DestinationContainer</span><span class="sxs-lookup"><span data-stu-id="f5f97-115">-DestinationContainer</span></span>
<span data-ttu-id="f5f97-116">Der Name des Zielcontainers, in den repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5f97-116">The Destination Container name to replicate to.</span></span>

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

### <span data-ttu-id="f5f97-117">-MinCreationTime</span><span class="sxs-lookup"><span data-stu-id="f5f97-117">-MinCreationTime</span></span>
<span data-ttu-id="f5f97-118">BLOBs, die nach dem Zeitpunkt erstellt wurden, werden in das Ziel repliziert.</span><span class="sxs-lookup"><span data-stu-id="f5f97-118">Blobs created after the time will be replicated to the destination..</span></span>

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

### <span data-ttu-id="f5f97-119">-PrefixMatch</span><span class="sxs-lookup"><span data-stu-id="f5f97-119">-PrefixMatch</span></span>
<span data-ttu-id="f5f97-120">Filtert die Ergebnisse, um nur BLOBs zu replizieren, deren Namen mit dem angegebenen Präfix beginnen.</span><span class="sxs-lookup"><span data-stu-id="f5f97-120">Filters the results to replicate only blobs whose names begin with the specified prefix.</span></span>

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

### <span data-ttu-id="f5f97-121">-Lineal</span><span class="sxs-lookup"><span data-stu-id="f5f97-121">-RuleId</span></span>
<span data-ttu-id="f5f97-122">Objekt Replikationsregel-ID.</span><span class="sxs-lookup"><span data-stu-id="f5f97-122">Object Replication Rule Id.</span></span>

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

### <span data-ttu-id="f5f97-123">-SourceContainer</span><span class="sxs-lookup"><span data-stu-id="f5f97-123">-SourceContainer</span></span>
<span data-ttu-id="f5f97-124">Der Name des Quellcontainers, von dem repliziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="f5f97-124">The Source Container name to replicate from.</span></span>

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

### <span data-ttu-id="f5f97-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5f97-125">CommonParameters</span></span>
<span data-ttu-id="f5f97-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5f97-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5f97-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5f97-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5f97-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f5f97-128">INPUTS</span></span>

### <span data-ttu-id="f5f97-129">Keine</span><span class="sxs-lookup"><span data-stu-id="f5f97-129">None</span></span>

## <span data-ttu-id="f5f97-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f5f97-130">OUTPUTS</span></span>

### <span data-ttu-id="f5f97-131">Microsoft. Azure. Commands. Management. Storage. Models. PSObjectReplicationPolicyRule</span><span class="sxs-lookup"><span data-stu-id="f5f97-131">Microsoft.Azure.Commands.Management.Storage.Models.PSObjectReplicationPolicyRule</span></span>

## <span data-ttu-id="f5f97-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f5f97-132">NOTES</span></span>

## <span data-ttu-id="f5f97-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f5f97-133">RELATED LINKS</span></span>
