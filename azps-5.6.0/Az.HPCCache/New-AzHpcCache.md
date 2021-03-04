---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: e0df378cb50d7d308d5d6a9f0acf8a15466b8a11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949384"
---
# <span data-ttu-id="9aa39-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="9aa39-101">New-AzHpcCache</span></span>

## <span data-ttu-id="9aa39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aa39-102">SYNOPSIS</span></span>
<span data-ttu-id="9aa39-103">Erstellt einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="9aa39-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="9aa39-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9aa39-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9aa39-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9aa39-105">DESCRIPTION</span></span>
<span data-ttu-id="9aa39-106">Das **Cmdlet New-AzHpcCache** erstellt einen Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="9aa39-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="9aa39-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9aa39-107">EXAMPLES</span></span>

### <span data-ttu-id="9aa39-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9aa39-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="9aa39-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9aa39-109">PARAMETERS</span></span>

### <span data-ttu-id="9aa39-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9aa39-110">-AsJob</span></span>
<span data-ttu-id="9aa39-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9aa39-111">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="9aa39-112">-CacheSize</span></span>
<span data-ttu-id="9aa39-113">CacheGröße.</span><span class="sxs-lookup"><span data-stu-id="9aa39-113">CacheSize.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aa39-114">-DefaultProfile</span></span>
<span data-ttu-id="9aa39-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9aa39-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9aa39-116">-Location</span><span class="sxs-lookup"><span data-stu-id="9aa39-116">-Location</span></span>
<span data-ttu-id="9aa39-117">Ort.</span><span class="sxs-lookup"><span data-stu-id="9aa39-117">Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9aa39-118">-Name</span></span>
<span data-ttu-id="9aa39-119">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="9aa39-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aa39-120">-ResourceGroupName</span></span>
<span data-ttu-id="9aa39-121">Name der Ressourcengruppe, unter der Sie den Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9aa39-121">Name of resource group under which you want to create cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-122">-Sku</span><span class="sxs-lookup"><span data-stu-id="9aa39-122">-Sku</span></span>
<span data-ttu-id="9aa39-123">Sku.</span><span class="sxs-lookup"><span data-stu-id="9aa39-123">Sku.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="9aa39-124">-SubnetUri</span></span>
<span data-ttu-id="9aa39-125">SubnetzURI.</span><span class="sxs-lookup"><span data-stu-id="9aa39-125">SubnetURI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="9aa39-126">-Tag</span></span>
<span data-ttu-id="9aa39-127">Die Tags, die dem HPC-Cache zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="9aa39-127">The tags to associate with HPC Cache.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9aa39-128">-Confirm</span></span>
<span data-ttu-id="9aa39-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9aa39-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aa39-130">-WhatIf</span></span>
<span data-ttu-id="9aa39-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9aa39-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aa39-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9aa39-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9aa39-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aa39-133">CommonParameters</span></span>
<span data-ttu-id="9aa39-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9aa39-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aa39-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9aa39-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aa39-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9aa39-136">INPUTS</span></span>

### <span data-ttu-id="9aa39-137">System.String</span><span class="sxs-lookup"><span data-stu-id="9aa39-137">System.String</span></span>

### <span data-ttu-id="9aa39-138">System.Int32</span><span class="sxs-lookup"><span data-stu-id="9aa39-138">System.Int32</span></span>

## <span data-ttu-id="9aa39-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9aa39-139">OUTPUTS</span></span>

### <span data-ttu-id="9aa39-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="9aa39-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="9aa39-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9aa39-141">NOTES</span></span>

## <span data-ttu-id="9aa39-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9aa39-142">RELATED LINKS</span></span>
