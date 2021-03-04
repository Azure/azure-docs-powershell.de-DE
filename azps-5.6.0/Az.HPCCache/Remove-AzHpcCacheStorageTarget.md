---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: 2de3856a51ce8b55d6db7a82f6e50027b60d9d87
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949371"
---
# <span data-ttu-id="7c6e0-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="7c6e0-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="7c6e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c6e0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6e0-103">Entfernt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="7c6e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c6e0-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c6e0-105">DESCRIPTION</span></span>
<span data-ttu-id="7c6e0-106">Das **Cmdlet Remove-AzHpcCacheStorageTarget** entfernt ein Speicherziel aus dem Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="7c6e0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c6e0-107">EXAMPLES</span></span>

### <span data-ttu-id="7c6e0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c6e0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="7c6e0-109">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7c6e0-109">PARAMETERS</span></span>

### <span data-ttu-id="7c6e0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c6e0-110">-AsJob</span></span>
<span data-ttu-id="7c6e0-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7c6e0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c6e0-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="7c6e0-112">-CacheName</span></span>
<span data-ttu-id="7c6e0-113">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-113">Name of cache.</span></span>

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

### <span data-ttu-id="7c6e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6e0-114">-DefaultProfile</span></span>
<span data-ttu-id="7c6e0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c6e0-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7c6e0-116">-Force</span></span>
<span data-ttu-id="7c6e0-117">Gibt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="7c6e0-118">Standardmäßig werden Sie in diesem Cmdlet aufgefordert, zu bestätigen, dass Sie das Speicherziel entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="7c6e0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c6e0-119">-Name</span></span>
<span data-ttu-id="7c6e0-120">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-120">Name of storage target.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageTargetName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6e0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c6e0-121">-PassThru</span></span>
<span data-ttu-id="7c6e0-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c6e0-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c6e0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6e0-124">-ResourceGroupName</span></span>
<span data-ttu-id="7c6e0-125">Name der Ressourcengruppe, unter der Sie das Speicherziel aus dem Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="7c6e0-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c6e0-126">-Confirm</span></span>
<span data-ttu-id="7c6e0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6e0-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6e0-128">-WhatIf</span></span>
<span data-ttu-id="7c6e0-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7c6e0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6e0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6e0-131">CommonParameters</span></span>
<span data-ttu-id="7c6e0-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6e0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6e0-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7c6e0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6e0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c6e0-134">INPUTS</span></span>

### <span data-ttu-id="7c6e0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="7c6e0-135">System.String</span></span>

## <span data-ttu-id="7c6e0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c6e0-136">OUTPUTS</span></span>

## <span data-ttu-id="7c6e0-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7c6e0-137">NOTES</span></span>

## <span data-ttu-id="7c6e0-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7c6e0-138">RELATED LINKS</span></span>
