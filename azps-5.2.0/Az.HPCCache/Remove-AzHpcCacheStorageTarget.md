---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363066"
---
# <span data-ttu-id="0fbc0-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="0fbc0-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="0fbc0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fbc0-102">SYNOPSIS</span></span>
<span data-ttu-id="0fbc0-103">Entfernt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="0fbc0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0fbc0-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fbc0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0fbc0-105">DESCRIPTION</span></span>
<span data-ttu-id="0fbc0-106">Das **Cmdlet "Remove-AzHpcCacheStorageTarget"** entfernt ein Speicherziel aus dem Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="0fbc0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0fbc0-107">EXAMPLES</span></span>

### <span data-ttu-id="0fbc0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0fbc0-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="0fbc0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fbc0-109">PARAMETERS</span></span>

### <span data-ttu-id="0fbc0-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fbc0-110">-AsJob</span></span>
<span data-ttu-id="0fbc0-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0fbc0-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0fbc0-112">-CacheName</span><span class="sxs-lookup"><span data-stu-id="0fbc0-112">-CacheName</span></span>
<span data-ttu-id="0fbc0-113">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-113">Name of cache.</span></span>

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

### <span data-ttu-id="0fbc0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fbc0-114">-DefaultProfile</span></span>
<span data-ttu-id="0fbc0-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0fbc0-116">-Force</span><span class="sxs-lookup"><span data-stu-id="0fbc0-116">-Force</span></span>
<span data-ttu-id="0fbc0-117">Zeigt an, dass sie vom Cmdlet nicht zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0fbc0-118">Dieses Cmdlet fordert Sie standardmäßig auf zu bestätigen, dass Sie das Speicherziel entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="0fbc0-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0fbc0-119">-Name</span></span>
<span data-ttu-id="0fbc0-120">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-120">Name of storage target.</span></span>

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

### <span data-ttu-id="0fbc0-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fbc0-121">-PassThru</span></span>
<span data-ttu-id="0fbc0-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0fbc0-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0fbc0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fbc0-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fbc0-125">Name der Ressourcengruppe, unter der Sie das Speicherziel aus dem Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="0fbc0-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fbc0-126">-Confirm</span></span>
<span data-ttu-id="0fbc0-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fbc0-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0fbc0-128">-WhatIf</span></span>
<span data-ttu-id="0fbc0-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0fbc0-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fbc0-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fbc0-131">CommonParameters</span></span>
<span data-ttu-id="0fbc0-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fbc0-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fbc0-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0fbc0-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fbc0-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0fbc0-134">INPUTS</span></span>

### <span data-ttu-id="0fbc0-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0fbc0-135">System.String</span></span>

## <span data-ttu-id="0fbc0-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0fbc0-136">OUTPUTS</span></span>

## <span data-ttu-id="0fbc0-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0fbc0-137">NOTES</span></span>

## <span data-ttu-id="0fbc0-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0fbc0-138">RELATED LINKS</span></span>
