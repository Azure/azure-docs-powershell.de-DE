---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: 12bf101fb404b02fc70cbec9640f5f2bd976107c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949376"
---
# <span data-ttu-id="0bfbc-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="0bfbc-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="0bfbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bfbc-102">SYNOPSIS</span></span>
<span data-ttu-id="0bfbc-103">Entfernt einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="0bfbc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0bfbc-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bfbc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0bfbc-105">DESCRIPTION</span></span>
<span data-ttu-id="0bfbc-106">Das **Cmdlet Remove-AzHpcCache** entfernt einen Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="0bfbc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0bfbc-107">EXAMPLES</span></span>

### <span data-ttu-id="0bfbc-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bfbc-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="0bfbc-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0bfbc-109">PARAMETERS</span></span>

### <span data-ttu-id="0bfbc-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0bfbc-110">-AsJob</span></span>
<span data-ttu-id="0bfbc-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0bfbc-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0bfbc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bfbc-112">-DefaultProfile</span></span>
<span data-ttu-id="0bfbc-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bfbc-114">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="0bfbc-114">-Force</span></span>
<span data-ttu-id="0bfbc-115">Gibt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0bfbc-116">Standardmäßig werden Sie in diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="0bfbc-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0bfbc-117">-Name</span></span>
<span data-ttu-id="0bfbc-118">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-118">Name of cache.</span></span>

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

### <span data-ttu-id="0bfbc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bfbc-119">-PassThru</span></span>
<span data-ttu-id="0bfbc-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0bfbc-121">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0bfbc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bfbc-122">-ResourceGroupName</span></span>
<span data-ttu-id="0bfbc-123">Name der Ressourcengruppe, unter der Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="0bfbc-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0bfbc-124">-Confirm</span></span>
<span data-ttu-id="0bfbc-125">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bfbc-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bfbc-126">-WhatIf</span></span>
<span data-ttu-id="0bfbc-127">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bfbc-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bfbc-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bfbc-129">CommonParameters</span></span>
<span data-ttu-id="0bfbc-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bfbc-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bfbc-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bfbc-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bfbc-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0bfbc-132">INPUTS</span></span>

### <span data-ttu-id="0bfbc-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0bfbc-133">System.String</span></span>

## <span data-ttu-id="0bfbc-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0bfbc-134">OUTPUTS</span></span>

## <span data-ttu-id="0bfbc-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0bfbc-135">NOTES</span></span>

## <span data-ttu-id="0bfbc-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0bfbc-136">RELATED LINKS</span></span>
