---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/update-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Update-AzHpcCache.md
ms.openlocfilehash: 8f84323df269d8e0fbd0f60525e54595ef89f3e8
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94175141"
---
# <span data-ttu-id="e05fc-101">Update-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="e05fc-101">Update-AzHpcCache</span></span>

## <span data-ttu-id="e05fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e05fc-102">SYNOPSIS</span></span>
<span data-ttu-id="e05fc-103">Aktualisiert einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="e05fc-103">Updates a HPC Cache.</span></span>

## <span data-ttu-id="e05fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e05fc-104">SYNTAX</span></span>

### <span data-ttu-id="e05fc-105">FlushParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="e05fc-105">FlushParameterSet (Default)</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Flush] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05fc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05fc-106">ByResourceIdParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05fc-107">UpgradeParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05fc-107">UpgradeParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> [-Upgrade] [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e05fc-108">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e05fc-108">ByObjectParameterSet</span></span>
```
Update-AzHpcCache -ResourceGroupName <String> -Name <String> -InputObject <PSHPCCache> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e05fc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e05fc-109">DESCRIPTION</span></span>
<span data-ttu-id="e05fc-110">Mit dem Cmdlet **Update-AzHpcCache** wird ein Azure HPC-Cache aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="e05fc-110">The **Update-AzHpcCache** cmdlet updates a Azure HPC Cache.</span></span>

## <span data-ttu-id="e05fc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e05fc-111">EXAMPLES</span></span>

### <span data-ttu-id="e05fc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e05fc-112">Example 1</span></span>
```powershell
PS C:\> Update-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="e05fc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="e05fc-113">PARAMETERS</span></span>

### <span data-ttu-id="e05fc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e05fc-114">-AsJob</span></span>
<span data-ttu-id="e05fc-115">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="e05fc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e05fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e05fc-116">-DefaultProfile</span></span>
<span data-ttu-id="e05fc-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e05fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e05fc-118">-Flush</span><span class="sxs-lookup"><span data-stu-id="e05fc-118">-Flush</span></span>
<span data-ttu-id="e05fc-119">Leert den HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="e05fc-119">Flushes HPC Cache.</span></span>

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

### <span data-ttu-id="e05fc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="e05fc-120">-Force</span></span>
<span data-ttu-id="e05fc-121">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="e05fc-121">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="e05fc-122">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e05fc-122">By default, this cmdlet prompts you to confirm that you want to update the cache.</span></span>

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

### <span data-ttu-id="e05fc-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e05fc-123">-InputObject</span></span>
<span data-ttu-id="e05fc-124">Das zu aktualisierbare Cache-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e05fc-124">The cache object to update.</span></span>

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

### <span data-ttu-id="e05fc-125">-Name</span><span class="sxs-lookup"><span data-stu-id="e05fc-125">-Name</span></span>
<span data-ttu-id="e05fc-126">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="e05fc-126">Name of cache.</span></span>

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

### <span data-ttu-id="e05fc-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e05fc-127">-PassThru</span></span>
<span data-ttu-id="e05fc-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e05fc-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e05fc-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="e05fc-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e05fc-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e05fc-130">-ResourceGroupName</span></span>
<span data-ttu-id="e05fc-131">Name der Ressourcengruppe, unter der Sie den Cache aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="e05fc-131">Name of resource group under which you want to update cache.</span></span>

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

### <span data-ttu-id="e05fc-132">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="e05fc-132">-ResourceId</span></span>
<span data-ttu-id="e05fc-133">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="e05fc-133">The resource id of the Cache</span></span>

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

### <span data-ttu-id="e05fc-134">-Upgrade</span><span class="sxs-lookup"><span data-stu-id="e05fc-134">-Upgrade</span></span>
<span data-ttu-id="e05fc-135">Aktualisieren Sie HpcCache.</span><span class="sxs-lookup"><span data-stu-id="e05fc-135">Upgrade HpcCache.</span></span>

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

### <span data-ttu-id="e05fc-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e05fc-136">-Confirm</span></span>
<span data-ttu-id="e05fc-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e05fc-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e05fc-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e05fc-138">-WhatIf</span></span>
<span data-ttu-id="e05fc-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e05fc-139">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e05fc-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e05fc-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e05fc-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e05fc-141">CommonParameters</span></span>
<span data-ttu-id="e05fc-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e05fc-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e05fc-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e05fc-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e05fc-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e05fc-144">INPUTS</span></span>

### <span data-ttu-id="e05fc-145">System. String</span><span class="sxs-lookup"><span data-stu-id="e05fc-145">System.String</span></span>

## <span data-ttu-id="e05fc-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e05fc-146">OUTPUTS</span></span>

## <span data-ttu-id="e05fc-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="e05fc-147">NOTES</span></span>

## <span data-ttu-id="e05fc-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e05fc-148">RELATED LINKS</span></span>
