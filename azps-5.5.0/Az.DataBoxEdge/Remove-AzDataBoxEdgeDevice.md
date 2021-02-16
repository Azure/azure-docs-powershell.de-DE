---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgedevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeDevice.md
ms.openlocfilehash: 69a484734dfde2459cf05f6eea763a8433b15827
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100148308"
---
# <span data-ttu-id="6499a-101">Remove-AzDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6499a-101">Remove-AzDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6499a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6499a-102">SYNOPSIS</span></span>
<span data-ttu-id="6499a-103">Entfernt ein Datenfeld-Edgegerät.</span><span class="sxs-lookup"><span data-stu-id="6499a-103">Removes a Data Box Edge device.</span></span>

## <span data-ttu-id="6499a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6499a-104">SYNTAX</span></span>

### <span data-ttu-id="6499a-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6499a-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeDevice [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6499a-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6499a-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6499a-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6499a-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeDevice -InputObject <PSDataBoxEdgeDevice> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6499a-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6499a-108">DESCRIPTION</span></span>
<span data-ttu-id="6499a-109">Das **Cmdlet "Remove-AzDataBoxEdgeDevice"** entfernt die Konfiguration für ein Data Box Edge-Gerät.</span><span class="sxs-lookup"><span data-stu-id="6499a-109">The **Remove-AzDataBoxEdgeDevice** cmdlet removes the configuration for a Data Box Edge device.</span></span>
<span data-ttu-id="6499a-110">Beachten Sie, dass das Gerät erst gelöscht werden kann, nachdem Sie die Bestellung bestellt haben und bevor das Gerät von Microsoft für die Sendung vorbereitet wird.</span><span class="sxs-lookup"><span data-stu-id="6499a-110">Note that the device can only be deleted after you have placed the order and before the device is prepared by Microsoft for shipment.</span></span>

<span data-ttu-id="6499a-111">Informationen zum Löschen der Ressource vor der Verwendung dieses [Cmdlets](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource) finden Sie in der Dokumentation</span><span class="sxs-lookup"><span data-stu-id="6499a-111">Refer the documentation on Deleting the resource before using this [cmdlet](https://docs.microsoft.com/en-us/azure/databox-online/data-box-edge-return-device#delete-the-resource)</span></span>

## <span data-ttu-id="6499a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6499a-112">EXAMPLES</span></span>

### <span data-ttu-id="6499a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6499a-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeDevice ResourceGroupName resourceGroupName -Name deviceName
```

## <span data-ttu-id="6499a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6499a-114">PARAMETERS</span></span>

### <span data-ttu-id="6499a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6499a-115">-AsJob</span></span>
<span data-ttu-id="6499a-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6499a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6499a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6499a-117">-DefaultProfile</span></span>
<span data-ttu-id="6499a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6499a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6499a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6499a-119">-InputObject</span></span>
<span data-ttu-id="6499a-120">Eingabeobjekt</span><span class="sxs-lookup"><span data-stu-id="6499a-120">Input Object</span></span>

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

### <span data-ttu-id="6499a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6499a-121">-Name</span></span>
<span data-ttu-id="6499a-122">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="6499a-122">Resource Name</span></span>

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

### <span data-ttu-id="6499a-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6499a-123">-PassThru</span></span>
<span data-ttu-id="6499a-124">gibt "true" zurück, wenn dies erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="6499a-124">returns true if successful</span></span>

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

### <span data-ttu-id="6499a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6499a-125">-ResourceGroupName</span></span>
<span data-ttu-id="6499a-126">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="6499a-126">Resource Group Name</span></span>

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

### <span data-ttu-id="6499a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6499a-127">-ResourceId</span></span>
<span data-ttu-id="6499a-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="6499a-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="6499a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6499a-129">-Confirm</span></span>
<span data-ttu-id="6499a-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6499a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6499a-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="6499a-131">-WhatIf</span></span>
<span data-ttu-id="6499a-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6499a-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6499a-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6499a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6499a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6499a-134">CommonParameters</span></span>
<span data-ttu-id="6499a-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6499a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6499a-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6499a-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6499a-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6499a-137">INPUTS</span></span>

### <span data-ttu-id="6499a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6499a-138">System.String</span></span>

### <span data-ttu-id="6499a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="6499a-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="6499a-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6499a-140">OUTPUTS</span></span>

### <span data-ttu-id="6499a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6499a-141">System.Boolean</span></span>

## <span data-ttu-id="6499a-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6499a-142">NOTES</span></span>

## <span data-ttu-id="6499a-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6499a-143">RELATED LINKS</span></span>
