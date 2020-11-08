---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccachestoragetarget
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCacheStorageTarget.md
ms.openlocfilehash: a3603a1884318f567908937ab880182e0df5ee57
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178013"
---
# <span data-ttu-id="14510-101">Remove-AzHpcCacheStorageTarget</span><span class="sxs-lookup"><span data-stu-id="14510-101">Remove-AzHpcCacheStorageTarget</span></span>

## <span data-ttu-id="14510-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="14510-102">SYNOPSIS</span></span>
<span data-ttu-id="14510-103">Entfernt ein Speicherziel.</span><span class="sxs-lookup"><span data-stu-id="14510-103">Removes a Storage Target.</span></span>

## <span data-ttu-id="14510-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="14510-104">SYNTAX</span></span>

```
Remove-AzHpcCacheStorageTarget -ResourceGroupName <String> -CacheName <String> -Name <String> [-Force]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14510-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14510-105">DESCRIPTION</span></span>
<span data-ttu-id="14510-106">Das Cmdlet **Remove-AzHpcCacheStorageTarget** entfernt ein Speicherziel aus dem Azure HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="14510-106">The **Remove-AzHpcCacheStorageTarget** cmdlet removes a Storage Target from Azure HPC Cache.</span></span>

## <span data-ttu-id="14510-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="14510-107">EXAMPLES</span></span>

### <span data-ttu-id="14510-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="14510-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCacheStorageTarget -ResourceGroupName testRG -CacheName testCache -StorageTargetName testST
```

## <span data-ttu-id="14510-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="14510-109">PARAMETERS</span></span>

### <span data-ttu-id="14510-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14510-110">-AsJob</span></span>
<span data-ttu-id="14510-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="14510-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14510-112">-Cachename</span><span class="sxs-lookup"><span data-stu-id="14510-112">-CacheName</span></span>
<span data-ttu-id="14510-113">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="14510-113">Name of cache.</span></span>

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

### <span data-ttu-id="14510-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14510-114">-DefaultProfile</span></span>
<span data-ttu-id="14510-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="14510-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14510-116">-Force</span><span class="sxs-lookup"><span data-stu-id="14510-116">-Force</span></span>
<span data-ttu-id="14510-117">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="14510-117">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="14510-118">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie das Speicherziel entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="14510-118">By default, this cmdlet prompts you to confirm that you want to remove the storage target.</span></span>

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

### <span data-ttu-id="14510-119">-Name</span><span class="sxs-lookup"><span data-stu-id="14510-119">-Name</span></span>
<span data-ttu-id="14510-120">Name des Speicherziels.</span><span class="sxs-lookup"><span data-stu-id="14510-120">Name of storage target.</span></span>

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

### <span data-ttu-id="14510-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14510-121">-PassThru</span></span>
<span data-ttu-id="14510-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="14510-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14510-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="14510-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14510-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14510-124">-ResourceGroupName</span></span>
<span data-ttu-id="14510-125">Name der Ressourcengruppe, unter der Sie das Speicherziel aus dem Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="14510-125">Name of resource group under which you want to remove storage target from cache.</span></span>

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

### <span data-ttu-id="14510-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="14510-126">-Confirm</span></span>
<span data-ttu-id="14510-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14510-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14510-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14510-128">-WhatIf</span></span>
<span data-ttu-id="14510-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14510-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14510-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14510-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14510-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14510-131">CommonParameters</span></span>
<span data-ttu-id="14510-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14510-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14510-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14510-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14510-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="14510-134">INPUTS</span></span>

### <span data-ttu-id="14510-135">System. String</span><span class="sxs-lookup"><span data-stu-id="14510-135">System.String</span></span>

## <span data-ttu-id="14510-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="14510-136">OUTPUTS</span></span>

## <span data-ttu-id="14510-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="14510-137">NOTES</span></span>

## <span data-ttu-id="14510-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="14510-138">RELATED LINKS</span></span>
