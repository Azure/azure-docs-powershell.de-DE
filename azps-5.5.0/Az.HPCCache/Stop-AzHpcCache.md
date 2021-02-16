---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170562"
---
# <span data-ttu-id="4edfc-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="4edfc-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="4edfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4edfc-102">SYNOPSIS</span></span>
<span data-ttu-id="4edfc-103">Beendet den HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="4edfc-103">Stops HPC cache.</span></span>

## <span data-ttu-id="4edfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4edfc-104">SYNTAX</span></span>

### <span data-ttu-id="4edfc-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4edfc-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4edfc-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4edfc-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4edfc-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4edfc-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4edfc-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4edfc-108">DESCRIPTION</span></span>
<span data-ttu-id="4edfc-109">Das **Cmdlet "Stop-AzHpcCache"** beendet einen Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="4edfc-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="4edfc-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4edfc-110">EXAMPLES</span></span>

### <span data-ttu-id="4edfc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4edfc-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="4edfc-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4edfc-112">PARAMETERS</span></span>

### <span data-ttu-id="4edfc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4edfc-113">-DefaultProfile</span></span>
<span data-ttu-id="4edfc-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4edfc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4edfc-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4edfc-115">-Force</span></span>
<span data-ttu-id="4edfc-116">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="4edfc-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="4edfc-117">Standardmäßig werden Sie von diesem Cmdlet aufgefordert zu bestätigen, dass Sie den Cache beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4edfc-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="4edfc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4edfc-118">-InputObject</span></span>
<span data-ttu-id="4edfc-119">Das zu beendende Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="4edfc-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="4edfc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="4edfc-120">-Name</span></span>
<span data-ttu-id="4edfc-121">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="4edfc-121">Name of cache.</span></span>

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

### <span data-ttu-id="4edfc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4edfc-122">-PassThru</span></span>
<span data-ttu-id="4edfc-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="4edfc-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="4edfc-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="4edfc-124">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4edfc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4edfc-125">-ResourceGroupName</span></span>
<span data-ttu-id="4edfc-126">Name der Ressourcengruppe, unter der Sie den Cache beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="4edfc-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="4edfc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4edfc-127">-ResourceId</span></span>
<span data-ttu-id="4edfc-128">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="4edfc-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="4edfc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4edfc-129">-Confirm</span></span>
<span data-ttu-id="4edfc-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4edfc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4edfc-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4edfc-131">-WhatIf</span></span>
<span data-ttu-id="4edfc-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4edfc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4edfc-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4edfc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4edfc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4edfc-134">CommonParameters</span></span>
<span data-ttu-id="4edfc-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4edfc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4edfc-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4edfc-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4edfc-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4edfc-137">INPUTS</span></span>

### <span data-ttu-id="4edfc-138">System.String</span><span class="sxs-lookup"><span data-stu-id="4edfc-138">System.String</span></span>

## <span data-ttu-id="4edfc-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4edfc-139">OUTPUTS</span></span>

## <span data-ttu-id="4edfc-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4edfc-140">NOTES</span></span>

## <span data-ttu-id="4edfc-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4edfc-141">RELATED LINKS</span></span>
