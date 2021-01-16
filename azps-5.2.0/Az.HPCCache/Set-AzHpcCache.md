---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/set-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Set-AzHpcCache.md
ms.openlocfilehash: 909f3be2e4a08ff1d1b0538b451ffa93f368d211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291952"
---
# <span data-ttu-id="48cd3-101">Set-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="48cd3-101">Set-AzHpcCache</span></span>

## <span data-ttu-id="48cd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48cd3-102">SYNOPSIS</span></span>
<span data-ttu-id="48cd3-103">Aktualisiert Tags in einem HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="48cd3-103">Updates tags on a HPC Cache.</span></span>

## <span data-ttu-id="48cd3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="48cd3-104">SYNTAX</span></span>

### <span data-ttu-id="48cd3-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="48cd3-105">ByFieldsParameterSet (Default)</span></span>
```
Set-AzHpcCache -ResourceGroupName <String> -Name <String> [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="48cd3-106">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="48cd3-106">ByObjectParameterSet</span></span>
```
Set-AzHpcCache -InputObject <PSHPCCache> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="48cd3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="48cd3-107">DESCRIPTION</span></span>
<span data-ttu-id="48cd3-108">Das **Cmdlet Set-AzHpcCache** aktualisiert Azure HPC-Cache-Tags.</span><span class="sxs-lookup"><span data-stu-id="48cd3-108">The **Set-AzHpcCache** cmdlet updates an Azure HPC Cache tags.</span></span>

## <span data-ttu-id="48cd3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="48cd3-109">EXAMPLES</span></span>

### <span data-ttu-id="48cd3-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="48cd3-110">Example 1</span></span>
```powershell
PS C:\> Set-AzHpcCache -ResourceGroupName testRG -CacheName testCache -Tag @{"tag3" = "value1"; "tag4" = "value2"}
```

## <span data-ttu-id="48cd3-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="48cd3-111">PARAMETERS</span></span>

### <span data-ttu-id="48cd3-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="48cd3-112">-AsJob</span></span>
<span data-ttu-id="48cd3-113">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="48cd3-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="48cd3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48cd3-114">-DefaultProfile</span></span>
<span data-ttu-id="48cd3-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="48cd3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="48cd3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="48cd3-116">-InputObject</span></span>
<span data-ttu-id="48cd3-117">Das zu aktualisierende Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="48cd3-117">The cache object to update.</span></span>

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

### <span data-ttu-id="48cd3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="48cd3-118">-Name</span></span>
<span data-ttu-id="48cd3-119">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="48cd3-119">Name of cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases: CacheName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48cd3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48cd3-120">-ResourceGroupName</span></span>
<span data-ttu-id="48cd3-121">Name der Ressourcengruppe, unter der Sie den Cache aktualisieren möchten.</span><span class="sxs-lookup"><span data-stu-id="48cd3-121">Name of resource group under which you want to update cache.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="48cd3-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="48cd3-122">-Tag</span></span>
<span data-ttu-id="48cd3-123">Die Tags, die mit dem HPC-Cache zu verknüpfen sind.</span><span class="sxs-lookup"><span data-stu-id="48cd3-123">The tags to associate with HPC Cache.</span></span> 

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="48cd3-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="48cd3-124">-Confirm</span></span>
<span data-ttu-id="48cd3-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="48cd3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="48cd3-126">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="48cd3-126">-WhatIf</span></span>
<span data-ttu-id="48cd3-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48cd3-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="48cd3-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="48cd3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="48cd3-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48cd3-129">CommonParameters</span></span>
<span data-ttu-id="48cd3-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48cd3-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48cd3-131">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="48cd3-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48cd3-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="48cd3-132">INPUTS</span></span>

### <span data-ttu-id="48cd3-133">System.String</span><span class="sxs-lookup"><span data-stu-id="48cd3-133">System.String</span></span>

### <span data-ttu-id="48cd3-134">System.Int32</span><span class="sxs-lookup"><span data-stu-id="48cd3-134">System.Int32</span></span>

## <span data-ttu-id="48cd3-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="48cd3-135">OUTPUTS</span></span>

### <span data-ttu-id="48cd3-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span><span class="sxs-lookup"><span data-stu-id="48cd3-136">Microsoft.Azure.PowerShell.Cmdlets.HPCCache.Models.PSHPCCache</span></span>

## <span data-ttu-id="48cd3-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="48cd3-137">NOTES</span></span>

## <span data-ttu-id="48cd3-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="48cd3-138">RELATED LINKS</span></span>
