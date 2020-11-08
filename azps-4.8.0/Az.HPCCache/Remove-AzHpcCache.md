---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166457"
---
# <span data-ttu-id="0901d-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="0901d-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="0901d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0901d-102">SYNOPSIS</span></span>
<span data-ttu-id="0901d-103">Entfernt einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="0901d-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="0901d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0901d-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0901d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0901d-105">DESCRIPTION</span></span>
<span data-ttu-id="0901d-106">Mit dem Cmdlet **Remove-AzHpcCache** wird ein Azure HPC-Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="0901d-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="0901d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0901d-107">EXAMPLES</span></span>

### <span data-ttu-id="0901d-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0901d-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="0901d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="0901d-109">PARAMETERS</span></span>

### <span data-ttu-id="0901d-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0901d-110">-AsJob</span></span>
<span data-ttu-id="0901d-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0901d-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0901d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0901d-112">-DefaultProfile</span></span>
<span data-ttu-id="0901d-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0901d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0901d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="0901d-114">-Force</span></span>
<span data-ttu-id="0901d-115">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="0901d-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="0901d-116">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0901d-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="0901d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0901d-117">-Name</span></span>
<span data-ttu-id="0901d-118">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="0901d-118">Name of cache.</span></span>

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

### <span data-ttu-id="0901d-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0901d-119">-PassThru</span></span>
<span data-ttu-id="0901d-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0901d-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0901d-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="0901d-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0901d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0901d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0901d-123">Name der Ressourcengruppe, unter der Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="0901d-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="0901d-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0901d-124">-Confirm</span></span>
<span data-ttu-id="0901d-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0901d-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0901d-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0901d-126">-WhatIf</span></span>
<span data-ttu-id="0901d-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0901d-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0901d-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0901d-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0901d-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0901d-129">CommonParameters</span></span>
<span data-ttu-id="0901d-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0901d-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0901d-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0901d-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0901d-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0901d-132">INPUTS</span></span>

### <span data-ttu-id="0901d-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0901d-133">System.String</span></span>

## <span data-ttu-id="0901d-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0901d-134">OUTPUTS</span></span>

## <span data-ttu-id="0901d-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="0901d-135">NOTES</span></span>

## <span data-ttu-id="0901d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0901d-136">RELATED LINKS</span></span>
