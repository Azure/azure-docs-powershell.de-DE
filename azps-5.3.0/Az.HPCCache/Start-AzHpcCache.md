---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/start-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Start-AzHpcCache.md
ms.openlocfilehash: 7465a74db4da777d60e097fe959ef69bed11918c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458475"
---
# <span data-ttu-id="fa029-101">Start-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fa029-101">Start-AzHpcCache</span></span>

## <span data-ttu-id="fa029-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa029-102">SYNOPSIS</span></span>
<span data-ttu-id="fa029-103">Startet den HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="fa029-103">Starts HPC cache.</span></span>

## <span data-ttu-id="fa029-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa029-104">SYNTAX</span></span>

### <span data-ttu-id="fa029-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fa029-105">ByFieldsParameterSet (Default)</span></span>
```
Start-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa029-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa029-106">ByResourceIdParameterSet</span></span>
```
Start-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa029-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa029-107">ByObjectParameterSet</span></span>
```
Start-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa029-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa029-108">DESCRIPTION</span></span>
<span data-ttu-id="fa029-109">Das **Cmdlet "Start-AzHpcCache"** startet einen Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="fa029-109">The **Start-AzHpcCache** cmdlet starts a Azure HPC Cache.</span></span>

## <span data-ttu-id="fa029-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa029-110">EXAMPLES</span></span>

### <span data-ttu-id="fa029-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa029-111">Example 1</span></span>
```powershell
PS C:\> Start-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="fa029-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa029-112">PARAMETERS</span></span>

### <span data-ttu-id="fa029-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa029-113">-AsJob</span></span>
<span data-ttu-id="fa029-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fa029-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fa029-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa029-115">-DefaultProfile</span></span>
<span data-ttu-id="fa029-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fa029-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa029-117">-Force</span><span class="sxs-lookup"><span data-stu-id="fa029-117">-Force</span></span>
<span data-ttu-id="fa029-118">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="fa029-118">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fa029-119">Standardmäßig werden Sie von diesem Cmdlet aufgefordert zu bestätigen, dass Sie den Cache starten möchten.</span><span class="sxs-lookup"><span data-stu-id="fa029-119">By default, this cmdlet prompts you to confirm that you want to start the cache.</span></span>

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

### <span data-ttu-id="fa029-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fa029-120">-InputObject</span></span>
<span data-ttu-id="fa029-121">Das zu startde Cacheobjekt.</span><span class="sxs-lookup"><span data-stu-id="fa029-121">The cache object to start.</span></span>

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

### <span data-ttu-id="fa029-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fa029-122">-Name</span></span>
<span data-ttu-id="fa029-123">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="fa029-123">Name of cache.</span></span>

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

### <span data-ttu-id="fa029-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa029-124">-PassThru</span></span>
<span data-ttu-id="fa029-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fa029-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fa029-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="fa029-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fa029-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa029-127">-ResourceGroupName</span></span>
<span data-ttu-id="fa029-128">Name der Ressourcengruppe, unter der Sie den Cache starten möchten.</span><span class="sxs-lookup"><span data-stu-id="fa029-128">Name of resource group under which you want to start cache.</span></span>

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

### <span data-ttu-id="fa029-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fa029-129">-ResourceId</span></span>
<span data-ttu-id="fa029-130">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="fa029-130">The resource id of the Cache</span></span>

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

### <span data-ttu-id="fa029-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa029-131">-Confirm</span></span>
<span data-ttu-id="fa029-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fa029-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa029-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fa029-133">-WhatIf</span></span>
<span data-ttu-id="fa029-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fa029-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fa029-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fa029-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa029-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa029-136">CommonParameters</span></span>
<span data-ttu-id="fa029-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa029-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa029-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa029-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa029-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa029-139">INPUTS</span></span>

### <span data-ttu-id="fa029-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fa029-140">System.String</span></span>

## <span data-ttu-id="fa029-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa029-141">OUTPUTS</span></span>

## <span data-ttu-id="fa029-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa029-142">NOTES</span></span>

## <span data-ttu-id="fa029-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa029-143">RELATED LINKS</span></span>
