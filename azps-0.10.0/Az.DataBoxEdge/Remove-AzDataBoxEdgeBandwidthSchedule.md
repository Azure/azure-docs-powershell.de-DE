---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 91be880f5e667287c1a9e62e2a003eb306ae1f5c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844051"
---
# <span data-ttu-id="27667-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="27667-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="27667-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="27667-102">SYNOPSIS</span></span>
<span data-ttu-id="27667-103">Entfernt einen Zeitplan für die Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="27667-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="27667-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="27667-104">SYNTAX</span></span>

### <span data-ttu-id="27667-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="27667-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27667-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27667-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27667-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27667-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27667-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="27667-108">DESCRIPTION</span></span>
<span data-ttu-id="27667-109">Mit dem Cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** wird der Bandbreiten Plan für ein Daten Feld-Edge-Gerät entfernt.</span><span class="sxs-lookup"><span data-stu-id="27667-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="27667-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="27667-110">EXAMPLES</span></span>

### <span data-ttu-id="27667-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="27667-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="27667-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="27667-112">PARAMETERS</span></span>

### <span data-ttu-id="27667-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27667-113">-AsJob</span></span>
<span data-ttu-id="27667-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="27667-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27667-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27667-115">-DefaultProfile</span></span>
<span data-ttu-id="27667-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="27667-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27667-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="27667-117">-DeviceName</span></span>
<span data-ttu-id="27667-118">Geräte Name</span><span class="sxs-lookup"><span data-stu-id="27667-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27667-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="27667-119">-InputObject</span></span>
<span data-ttu-id="27667-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="27667-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27667-121">-Name</span><span class="sxs-lookup"><span data-stu-id="27667-121">-Name</span></span>
<span data-ttu-id="27667-122">Ressourcen Name</span><span class="sxs-lookup"><span data-stu-id="27667-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27667-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="27667-123">-PassThru</span></span>
<span data-ttu-id="27667-124">gibt "true" zurück, wenn erfolgreich</span><span class="sxs-lookup"><span data-stu-id="27667-124">returns true if successful</span></span>

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

### <span data-ttu-id="27667-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27667-125">-ResourceGroupName</span></span>
<span data-ttu-id="27667-126">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="27667-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27667-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="27667-127">-ResourceId</span></span>
<span data-ttu-id="27667-128">Azure-Hilfsquelle</span><span class="sxs-lookup"><span data-stu-id="27667-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="27667-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="27667-129">-Confirm</span></span>
<span data-ttu-id="27667-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="27667-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27667-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27667-131">-WhatIf</span></span>
<span data-ttu-id="27667-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="27667-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27667-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="27667-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27667-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27667-134">CommonParameters</span></span>
<span data-ttu-id="27667-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27667-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27667-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="27667-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27667-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="27667-137">INPUTS</span></span>

### <span data-ttu-id="27667-138">System. String</span><span class="sxs-lookup"><span data-stu-id="27667-138">System.String</span></span>

### <span data-ttu-id="27667-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="27667-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="27667-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="27667-140">OUTPUTS</span></span>

### <span data-ttu-id="27667-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="27667-141">System.Boolean</span></span>

## <span data-ttu-id="27667-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="27667-142">NOTES</span></span>

## <span data-ttu-id="27667-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="27667-143">RELATED LINKS</span></span>
