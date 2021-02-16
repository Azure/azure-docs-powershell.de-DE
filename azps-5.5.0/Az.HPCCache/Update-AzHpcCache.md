---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170561"
---
# <span data-ttu-id="cc110-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="cc110-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="cc110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc110-102">SYNOPSIS</span></span>
<span data-ttu-id="cc110-103">Aktualisiert einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="cc110-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="cc110-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc110-104">SYNTAX</span></span>

### <span data-ttu-id="cc110-105">FlushParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc110-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc110-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc110-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc110-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc110-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc110-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc110-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc110-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc110-109">DESCRIPTION</span></span>
<span data-ttu-id="cc110-110">Das **Cmdlet "Update-AzHpcCache"** aktualisiert einen Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="cc110-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="cc110-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc110-111">EXAMPLES</span></span>

### <span data-ttu-id="cc110-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc110-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="cc110-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc110-113">PARAMETERS</span></span>

### <span data-ttu-id="cc110-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc110-114">-AsJob</span></span>
<span data-ttu-id="cc110-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc110-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc110-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc110-116">-DefaultProfile</span></span>
<span data-ttu-id="cc110-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc110-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc110-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="cc110-118">-Flush</span></span>
<span data-ttu-id="cc110-119">Leeren Sie den HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="cc110-119">Flushes HPC Cache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FlushParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc110-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cc110-120">-Force</span></span>
<span data-ttu-id="cc110-121">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="cc110-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="cc110-122">Dieses Cmdlet fordert Sie standardmäßig auf zu bestätigen, dass Sie den Cache aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cc110-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="cc110-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc110-123">-InputObject</span></span>
<span data-ttu-id="cc110-124">Das zu aktualisierende Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="cc110-124">The cache object to update.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache
Parameter Sets: ByObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc110-125">-Name</span><span class="sxs-lookup"><span data-stu-id="cc110-125">-Name</span></span>
<span data-ttu-id="cc110-126">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="cc110-126">Name of cache.</span></span>

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

### <span data-ttu-id="cc110-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc110-127">-PassThru</span></span>
<span data-ttu-id="cc110-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc110-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc110-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cc110-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc110-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc110-130">-ResourceGroupName</span></span>
<span data-ttu-id="cc110-131">Name der Ressourcengruppe, unter der Sie den Cache aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="cc110-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="cc110-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc110-132">-ResourceId</span></span>
<span data-ttu-id="cc110-133">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="cc110-133">The resource id of the Cache</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc110-134">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="cc110-134">-Upgrade</span></span>
<span data-ttu-id="cc110-135">Führen Sie ein Upgrade von HpcCache durch.</span><span class="sxs-lookup"><span data-stu-id="cc110-135">Upgrade HpcCache.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpgradeParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc110-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc110-136">-Confirm</span></span>
<span data-ttu-id="cc110-137">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc110-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc110-138">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc110-138">-WhatIf</span></span>
<span data-ttu-id="cc110-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc110-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="cc110-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc110-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc110-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc110-141">CommonParameters</span></span>
<span data-ttu-id="cc110-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc110-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc110-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc110-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc110-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc110-144">INPUTS</span></span>

### <span data-ttu-id="cc110-145">System.String</span><span class="sxs-lookup"><span data-stu-id="cc110-145">System.String</span></span>

## <span data-ttu-id="cc110-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc110-146">OUTPUTS</span></span>

## <span data-ttu-id="cc110-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc110-147">NOTES</span></span>

## <span data-ttu-id="cc110-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc110-148">RELATED LINKS</span></span>
