---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 5effec8ed39f9219bcecba23f6ca3cabaae5cec9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176719"
---
# <span data-ttu-id="15b76-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="15b76-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="15b76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="15b76-102">SYNOPSIS</span></span>
<span data-ttu-id="15b76-103">Entfernt die Reihenfolge für ein Gerät.</span><span class="sxs-lookup"><span data-stu-id="15b76-103">Removes the order for a device.</span></span>

## <span data-ttu-id="15b76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="15b76-104">SYNTAX</span></span>

### <span data-ttu-id="15b76-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="15b76-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15b76-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="15b76-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="15b76-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="15b76-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15b76-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15b76-108">DESCRIPTION</span></span>
<span data-ttu-id="15b76-109">Das Cmdlet **Remove-AzStackEdgeOrder** löscht eine vorhandene Reihenfolge für ein Stack-Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="15b76-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="15b76-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="15b76-110">EXAMPLES</span></span>

### <span data-ttu-id="15b76-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="15b76-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="15b76-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="15b76-112">PARAMETERS</span></span>

### <span data-ttu-id="15b76-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="15b76-113">-AsJob</span></span>
<span data-ttu-id="15b76-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="15b76-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="15b76-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15b76-115">-DefaultProfile</span></span>
<span data-ttu-id="15b76-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="15b76-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15b76-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="15b76-117">-DeviceName</span></span>
<span data-ttu-id="15b76-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="15b76-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b76-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="15b76-119">-InputObject</span></span>
<span data-ttu-id="15b76-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="15b76-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="15b76-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="15b76-121">-PassThru</span></span>
<span data-ttu-id="15b76-122">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="15b76-122">returns true if successful</span></span>

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

### <span data-ttu-id="15b76-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15b76-123">-ResourceGroupName</span></span>
<span data-ttu-id="15b76-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="15b76-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b76-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="15b76-125">-ResourceId</span></span>
<span data-ttu-id="15b76-126">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="15b76-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15b76-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="15b76-127">-Confirm</span></span>
<span data-ttu-id="15b76-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="15b76-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="15b76-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15b76-129">-WhatIf</span></span>
<span data-ttu-id="15b76-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="15b76-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="15b76-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="15b76-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="15b76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15b76-132">CommonParameters</span></span>
<span data-ttu-id="15b76-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15b76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15b76-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="15b76-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15b76-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="15b76-135">INPUTS</span></span>

### <span data-ttu-id="15b76-136">System. String</span><span class="sxs-lookup"><span data-stu-id="15b76-136">System.String</span></span>

### <span data-ttu-id="15b76-137">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="15b76-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="15b76-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="15b76-138">OUTPUTS</span></span>

### <span data-ttu-id="15b76-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="15b76-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="15b76-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="15b76-140">NOTES</span></span>

## <span data-ttu-id="15b76-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="15b76-141">RELATED LINKS</span></span>
