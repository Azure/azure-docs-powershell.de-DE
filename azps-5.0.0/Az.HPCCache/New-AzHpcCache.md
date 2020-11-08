---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/new-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/New-AzHpcCache.md
ms.openlocfilehash: faadb14259dd397f713480c771d2d450260d99cc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178020"
---
# <span data-ttu-id="7337f-101">New-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="7337f-101">New-AzHpcCache</span></span>

## <span data-ttu-id="7337f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7337f-102">SYNOPSIS</span></span>
<span data-ttu-id="7337f-103">Erstellt einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="7337f-103">Creates a HPC Cache.</span></span>

## <span data-ttu-id="7337f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7337f-104">SYNTAX</span></span>

```
New-AzHpcCache -ResourceGroupName <String> -Name <String> -Sku <String> -SubnetUri <String> -CacheSize <Int32>
 -Location <String> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7337f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7337f-105">DESCRIPTION</span></span>
<span data-ttu-id="7337f-106">Mit dem Cmdlet **New-AzHpcCache** wird ein Azure HPC-Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="7337f-106">The **New-AzHpcCache** cmdlet creates a Azure HPC Cache.</span></span>

## <span data-ttu-id="7337f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7337f-107">EXAMPLES</span></span>

### <span data-ttu-id="7337f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7337f-108">Example 1</span></span>
```powershell
PS C:\> New-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Sku Standard_2G -SubnetUri /subscriptions/<subid>/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/testvnet/subnets/defauly-tip1-test2 -cacheSize 3072 -Location eastus -Tag @{"tag1" = "value1"; "tag2" = "value2"}
```

## <span data-ttu-id="7337f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7337f-109">PARAMETERS</span></span>

### <span data-ttu-id="7337f-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7337f-110">-AsJob</span></span>
<span data-ttu-id="7337f-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7337f-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7337f-112">-CacheSize</span><span class="sxs-lookup"><span data-stu-id="7337f-112">-CacheSize</span></span>
<span data-ttu-id="7337f-113">CacheSize.</span><span class="sxs-lookup"><span data-stu-id="7337f-113">CacheSize.</span></span>

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

### <span data-ttu-id="7337f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7337f-114">-DefaultProfile</span></span>
<span data-ttu-id="7337f-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7337f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7337f-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="7337f-116">-Location</span></span>
<span data-ttu-id="7337f-117">Lage.</span><span class="sxs-lookup"><span data-stu-id="7337f-117">Location.</span></span>

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

### <span data-ttu-id="7337f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="7337f-118">-Name</span></span>
<span data-ttu-id="7337f-119">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="7337f-119">Name of cache.</span></span>

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

### <span data-ttu-id="7337f-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7337f-120">-ResourceGroupName</span></span>
<span data-ttu-id="7337f-121">Name der Ressourcengruppe, unter der Sie den Cache erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7337f-121">Name of resource group under which you want to create cache.</span></span>

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

### <span data-ttu-id="7337f-122">-SKU</span><span class="sxs-lookup"><span data-stu-id="7337f-122">-Sku</span></span>
<span data-ttu-id="7337f-123">SKU.</span><span class="sxs-lookup"><span data-stu-id="7337f-123">Sku.</span></span>

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

### <span data-ttu-id="7337f-124">-SubnetUri</span><span class="sxs-lookup"><span data-stu-id="7337f-124">-SubnetUri</span></span>
<span data-ttu-id="7337f-125">SubnetURI.</span><span class="sxs-lookup"><span data-stu-id="7337f-125">SubnetURI.</span></span>

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

### <span data-ttu-id="7337f-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="7337f-126">-Tag</span></span>
<span data-ttu-id="7337f-127">Die Tags, die dem HPC-Cache zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7337f-127">The tags to associate with HPC Cache.</span></span>

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

### <span data-ttu-id="7337f-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7337f-128">-Confirm</span></span>
<span data-ttu-id="7337f-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7337f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7337f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7337f-130">-WhatIf</span></span>
<span data-ttu-id="7337f-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7337f-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7337f-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7337f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7337f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7337f-133">CommonParameters</span></span>
<span data-ttu-id="7337f-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7337f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7337f-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7337f-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7337f-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7337f-136">INPUTS</span></span>

### <span data-ttu-id="7337f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7337f-137">System.String</span></span>

### <span data-ttu-id="7337f-138">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7337f-138">System.Int32</span></span>

## <span data-ttu-id="7337f-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7337f-139">OUTPUTS</span></span>

### <span data-ttu-id="7337f-140">Microsoft. Azure. PowerShell. Cmdlets. HPCCache. Models. PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="7337f-140">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="7337f-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7337f-141">NOTES</span></span>

## <span data-ttu-id="7337f-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7337f-142">RELATED LINKS</span></span>
