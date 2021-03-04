---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 1f2c2e2bf02718053d3656b084f845f40215aceb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937048"
---
# <span data-ttu-id="1a34c-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1a34c-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1a34c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a34c-102">SYNOPSIS</span></span>
<span data-ttu-id="1a34c-103">Entfernt ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1a34c-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="1a34c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a34c-104">SYNTAX</span></span>

### <span data-ttu-id="1a34c-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1a34c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a34c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a34c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a34c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1a34c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a34c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a34c-108">DESCRIPTION</span></span>
<span data-ttu-id="1a34c-109">Das **Cmdlet Remove-AzDataBoxEdgeDevice** entfernt die Konfiguration für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="1a34c-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="1a34c-110">Beachten Sie, dass das Gerät erst gelöscht werden kann, nachdem Sie die Bestellung bestellt haben und bevor das Gerät von Microsoft für den Versand vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="1a34c-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="1a34c-111">Lesen Sie die Dokumentation zum Löschen der Ressource, bevor Sie dieses [Cmdlet verwenden.](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span><span class="sxs-lookup"><span data-stu-id="1a34c-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="1a34c-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a34c-112">EXAMPLES</span></span>

### <span data-ttu-id="1a34c-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a34c-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="1a34c-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1a34c-114">PARAMETERS</span></span>

### <span data-ttu-id="1a34c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1a34c-115">-AsJob</span></span>
<span data-ttu-id="1a34c-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1a34c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1a34c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a34c-117">-DefaultProfile</span></span>
<span data-ttu-id="1a34c-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a34c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a34c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a34c-119">-InputObject</span></span>
<span data-ttu-id="1a34c-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="1a34c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a34c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1a34c-121">-Name</span></span>
<span data-ttu-id="1a34c-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="1a34c-122">Resource Name</span></span>

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

### <span data-ttu-id="1a34c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1a34c-123">-PassThru</span></span>
<span data-ttu-id="1a34c-124">gibt "true" zurück, wenn dies erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="1a34c-124">returns true if successful</span></span>

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

### <span data-ttu-id="1a34c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a34c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1a34c-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="1a34c-126">Resource Group Name</span></span>

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

### <span data-ttu-id="1a34c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a34c-127">-ResourceId</span></span>
<span data-ttu-id="1a34c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1a34c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1a34c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a34c-129">-Confirm</span></span>
<span data-ttu-id="1a34c-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a34c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a34c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a34c-131">-WhatIf</span></span>
<span data-ttu-id="1a34c-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a34c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a34c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a34c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a34c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a34c-134">CommonParameters</span></span>
<span data-ttu-id="1a34c-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a34c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a34c-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a34c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a34c-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a34c-137">INPUTS</span></span>

### <span data-ttu-id="1a34c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1a34c-138">System.String</span></span>

### <span data-ttu-id="1a34c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="1a34c-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="1a34c-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a34c-140">OUTPUTS</span></span>

### <span data-ttu-id="1a34c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1a34c-141">System.Boolean</span></span>

## <span data-ttu-id="1a34c-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1a34c-142">NOTES</span></span>

## <span data-ttu-id="1a34c-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1a34c-143">RELATED LINKS</span></span>
