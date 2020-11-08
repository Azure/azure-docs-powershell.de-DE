---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/remove-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Remove-AzHpcCache.md
ms.openlocfilehash: fd01dea04043d8d68009f89823fe34f3695a6d47
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178017"
---
# <span data-ttu-id="8ad4b-101">Remove-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="8ad4b-101">Remove-AzHpcCache</span></span>

## <span data-ttu-id="8ad4b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8ad4b-102">SYNOPSIS</span></span>
<span data-ttu-id="8ad4b-103">Entfernt einen HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-103">Removes a HPC Cache.</span></span>

## <span data-ttu-id="8ad4b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8ad4b-104">SYNTAX</span></span>

```
Remove-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ad4b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8ad4b-105">DESCRIPTION</span></span>
<span data-ttu-id="8ad4b-106">Mit dem Cmdlet **Remove-AzHpcCache** wird ein Azure HPC-Cache entfernt.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-106">The **Remove-AzHpcCache** cmdlet removes a Azure HPC Cache.</span></span>

## <span data-ttu-id="8ad4b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8ad4b-107">EXAMPLES</span></span>

### <span data-ttu-id="8ad4b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8ad4b-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="8ad4b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ad4b-109">PARAMETERS</span></span>

### <span data-ttu-id="8ad4b-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8ad4b-110">-AsJob</span></span>
<span data-ttu-id="8ad4b-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8ad4b-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8ad4b-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ad4b-112">-DefaultProfile</span></span>
<span data-ttu-id="8ad4b-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ad4b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="8ad4b-114">-Force</span></span>
<span data-ttu-id="8ad4b-115">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-115">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="8ad4b-116">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-116">By default, this cmdlet prompts you to confirm that you want to remove the cache.</span></span>

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

### <span data-ttu-id="8ad4b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8ad4b-117">-Name</span></span>
<span data-ttu-id="8ad4b-118">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-118">Name of cache.</span></span>

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

### <span data-ttu-id="8ad4b-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8ad4b-119">-PassThru</span></span>
<span data-ttu-id="8ad4b-120">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="8ad4b-121">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-121">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8ad4b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ad4b-122">-ResourceGroupName</span></span>
<span data-ttu-id="8ad4b-123">Name der Ressourcengruppe, unter der Sie den Cache entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-123">Name of resource group under which you want to remove cache.</span></span>

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

### <span data-ttu-id="8ad4b-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ad4b-124">-Confirm</span></span>
<span data-ttu-id="8ad4b-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ad4b-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ad4b-126">-WhatIf</span></span>
<span data-ttu-id="8ad4b-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ad4b-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ad4b-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ad4b-129">CommonParameters</span></span>
<span data-ttu-id="8ad4b-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ad4b-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ad4b-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8ad4b-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ad4b-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8ad4b-132">INPUTS</span></span>

### <span data-ttu-id="8ad4b-133">System. String</span><span class="sxs-lookup"><span data-stu-id="8ad4b-133">System.String</span></span>

## <span data-ttu-id="8ad4b-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8ad4b-134">OUTPUTS</span></span>

## <span data-ttu-id="8ad4b-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="8ad4b-135">NOTES</span></span>

## <span data-ttu-id="8ad4b-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8ad4b-136">RELATED LINKS</span></span>
