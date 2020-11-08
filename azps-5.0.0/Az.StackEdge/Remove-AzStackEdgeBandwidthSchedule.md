---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179987"
---
# <span data-ttu-id="77a7e-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="77a7e-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="77a7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77a7e-102">SYNOPSIS</span></span>
<span data-ttu-id="77a7e-103">Entfernt einen Zeitplan für die Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="77a7e-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="77a7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="77a7e-104">SYNTAX</span></span>

### <span data-ttu-id="77a7e-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="77a7e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a7e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a7e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77a7e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77a7e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77a7e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77a7e-108">DESCRIPTION</span></span>
<span data-ttu-id="77a7e-109">Mit dem Cmdlet **Remove-AzStackEdgeBandwidthSchedule** wird der Bandbreiten Plan für ein Stack-Edge-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="77a7e-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="77a7e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77a7e-110">EXAMPLES</span></span>

### <span data-ttu-id="77a7e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77a7e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="77a7e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77a7e-112">PARAMETERS</span></span>

### <span data-ttu-id="77a7e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="77a7e-113">-AsJob</span></span>
<span data-ttu-id="77a7e-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="77a7e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77a7e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77a7e-115">-DefaultProfile</span></span>
<span data-ttu-id="77a7e-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77a7e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77a7e-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="77a7e-117">-DeviceName</span></span>
<span data-ttu-id="77a7e-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="77a7e-118">Device Name</span></span>

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

### <span data-ttu-id="77a7e-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77a7e-119">-InputObject</span></span>
<span data-ttu-id="77a7e-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="77a7e-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77a7e-121">-Name</span><span class="sxs-lookup"><span data-stu-id="77a7e-121">-Name</span></span>
<span data-ttu-id="77a7e-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="77a7e-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77a7e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77a7e-123">-PassThru</span></span>
<span data-ttu-id="77a7e-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="77a7e-124">returns true if successful</span></span>

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

### <span data-ttu-id="77a7e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77a7e-125">-ResourceGroupName</span></span>
<span data-ttu-id="77a7e-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="77a7e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="77a7e-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="77a7e-127">-ResourceId</span></span>
<span data-ttu-id="77a7e-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="77a7e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="77a7e-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77a7e-129">-Confirm</span></span>
<span data-ttu-id="77a7e-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77a7e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77a7e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77a7e-131">-WhatIf</span></span>
<span data-ttu-id="77a7e-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77a7e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77a7e-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77a7e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77a7e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77a7e-134">CommonParameters</span></span>
<span data-ttu-id="77a7e-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77a7e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77a7e-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77a7e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77a7e-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77a7e-137">INPUTS</span></span>

### <span data-ttu-id="77a7e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="77a7e-138">System.String</span></span>

### <span data-ttu-id="77a7e-139">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="77a7e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="77a7e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77a7e-140">OUTPUTS</span></span>

### <span data-ttu-id="77a7e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77a7e-141">System.Boolean</span></span>

## <span data-ttu-id="77a7e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="77a7e-142">NOTES</span></span>

## <span data-ttu-id="77a7e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77a7e-143">RELATED LINKS</span></span>
