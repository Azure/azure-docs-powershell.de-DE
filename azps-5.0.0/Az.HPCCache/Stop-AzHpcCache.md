---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HPCCache.dll-Help.xml
Module Name: Az.HPCCache
online version: https://docs.microsoft.com/en-us/powershell/module/az.hpccache/stop-azhpccache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HPCCache/HPCCache/help/Stop-AzHpcCache.md
ms.openlocfilehash: 22813d762fe575f7f34b6c8eb81f1b5c1c167047
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175555"
---
# <span data-ttu-id="fcb09-101">Stop-AzHpcCache</span><span class="sxs-lookup"><span data-stu-id="fcb09-101">Stop-AzHpcCache</span></span>

## <span data-ttu-id="fcb09-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fcb09-102">SYNOPSIS</span></span>
<span data-ttu-id="fcb09-103">Beendet den HPC-Cache.</span><span class="sxs-lookup"><span data-stu-id="fcb09-103">Stops HPC cache.</span></span>

## <span data-ttu-id="fcb09-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fcb09-104">SYNTAX</span></span>

### <span data-ttu-id="fcb09-105">ByFieldsParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="fcb09-105">ByFieldsParameterSet (Default)</span></span>
```
Stop-AzHpcCache -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb09-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcb09-106">ByResourceIdParameterSet</span></span>
```
Stop-AzHpcCache -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcb09-107">ByObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fcb09-107">ByObjectParameterSet</span></span>
```
Stop-AzHpcCache -InputObject <PSHPCCache> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcb09-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fcb09-108">DESCRIPTION</span></span>
<span data-ttu-id="fcb09-109">Mit dem Cmdlet " **Stop-AzHpcCache** " wird ein Azure HPC-Cache beendet.</span><span class="sxs-lookup"><span data-stu-id="fcb09-109">The **Stop-AzHpcCache** cmdlet stops a Azure HPC Cache.</span></span>

## <span data-ttu-id="fcb09-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fcb09-110">EXAMPLES</span></span>

### <span data-ttu-id="fcb09-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fcb09-111">Example 1</span></span>
```powershell
PS C:\> Stop-AzHpcCache -ResourceGroupName testRG -CacheName testCache
```

## <span data-ttu-id="fcb09-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="fcb09-112">PARAMETERS</span></span>

### <span data-ttu-id="fcb09-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcb09-113">-DefaultProfile</span></span>
<span data-ttu-id="fcb09-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fcb09-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fcb09-115">-Force</span><span class="sxs-lookup"><span data-stu-id="fcb09-115">-Force</span></span>
<span data-ttu-id="fcb09-116">Gibt an, dass das Cmdlet Sie nicht zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="fcb09-116">Indicates that the cmdlet does not prompt you for confirmation.</span></span> <span data-ttu-id="fcb09-117">Standardmäßig werden Sie von diesem Cmdlet aufgefordert, zu bestätigen, dass Sie den Cache beenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fcb09-117">By default, this cmdlet prompts you to confirm that you want to stop the cache.</span></span>

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

### <span data-ttu-id="fcb09-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fcb09-118">-InputObject</span></span>
<span data-ttu-id="fcb09-119">Das zu beendende Cache-Objekt.</span><span class="sxs-lookup"><span data-stu-id="fcb09-119">The cache object to stop.</span></span>

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

### <span data-ttu-id="fcb09-120">-Name</span><span class="sxs-lookup"><span data-stu-id="fcb09-120">-Name</span></span>
<span data-ttu-id="fcb09-121">Name des Caches.</span><span class="sxs-lookup"><span data-stu-id="fcb09-121">Name of cache.</span></span>

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

### <span data-ttu-id="fcb09-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fcb09-122">-PassThru</span></span>
<span data-ttu-id="fcb09-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="fcb09-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fcb09-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="fcb09-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fcb09-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcb09-125">-ResourceGroupName</span></span>
<span data-ttu-id="fcb09-126">Name der Ressourcengruppe, unter der der Cache beendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fcb09-126">Name of resource group under which you want to stop cache.</span></span>

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

### <span data-ttu-id="fcb09-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="fcb09-127">-ResourceId</span></span>
<span data-ttu-id="fcb09-128">Die Ressourcen-ID des Caches</span><span class="sxs-lookup"><span data-stu-id="fcb09-128">The resource id of the Cache</span></span>

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

### <span data-ttu-id="fcb09-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fcb09-129">-Confirm</span></span>
<span data-ttu-id="fcb09-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fcb09-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcb09-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcb09-131">-WhatIf</span></span>
<span data-ttu-id="fcb09-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fcb09-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcb09-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fcb09-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcb09-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcb09-134">CommonParameters</span></span>
<span data-ttu-id="fcb09-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fcb09-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcb09-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fcb09-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcb09-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fcb09-137">INPUTS</span></span>

### <span data-ttu-id="fcb09-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fcb09-138">System.String</span></span>

## <span data-ttu-id="fcb09-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fcb09-139">OUTPUTS</span></span>

## <span data-ttu-id="fcb09-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="fcb09-140">NOTES</span></span>

## <span data-ttu-id="fcb09-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fcb09-141">RELATED LINKS</span></span>
