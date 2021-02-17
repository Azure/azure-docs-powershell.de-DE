---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 0b29719dee8a1e69d27dd36cee2888df4575eefc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169662"
---
# <span data-ttu-id="85dc7-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="85dc7-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="85dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="85dc7-103">Entfernen sie eine Website für virtuelle Geräte aus einer Network Virtual Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="85dc7-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="85dc7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85dc7-104">SYNTAX</span></span>

### <span data-ttu-id="85dc7-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="85dc7-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="85dc7-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="85dc7-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85dc7-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="85dc7-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85dc7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85dc7-108">DESCRIPTION</span></span>
<span data-ttu-id="85dc7-109">Mit Remove-AzVirtualApplianceSite Befehl wird eine Virtual Appliance-Website von einer Network Virtual Appliance-Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="85dc7-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="85dc7-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85dc7-110">EXAMPLES</span></span>

### <span data-ttu-id="85dc7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85dc7-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="85dc7-112">Löschen sie eine Websiteressource für virtuelle Geräte.</span><span class="sxs-lookup"><span data-stu-id="85dc7-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="85dc7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85dc7-113">PARAMETERS</span></span>

### <span data-ttu-id="85dc7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85dc7-114">-AsJob</span></span>
<span data-ttu-id="85dc7-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="85dc7-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="85dc7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85dc7-116">-DefaultProfile</span></span>
<span data-ttu-id="85dc7-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85dc7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85dc7-118">-Force</span><span class="sxs-lookup"><span data-stu-id="85dc7-118">-Force</span></span>
<span data-ttu-id="85dc7-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="85dc7-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="85dc7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="85dc7-120">-Name</span></span>
<span data-ttu-id="85dc7-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="85dc7-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dc7-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="85dc7-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="85dc7-123">Die Ressourcen-ID der virtuellen Network Appliance, die dieser Website zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="85dc7-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dc7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85dc7-124">-PassThru</span></span>
<span data-ttu-id="85dc7-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="85dc7-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="85dc7-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="85dc7-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="85dc7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85dc7-127">-ResourceGroupName</span></span>
<span data-ttu-id="85dc7-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85dc7-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dc7-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85dc7-129">-ResourceId</span></span>
<span data-ttu-id="85dc7-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="85dc7-130">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dc7-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="85dc7-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="85dc7-132">Das Websiteobjekt der virtuellen Einheit.</span><span class="sxs-lookup"><span data-stu-id="85dc7-132">The virtual appliance site object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85dc7-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85dc7-133">-Confirm</span></span>
<span data-ttu-id="85dc7-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85dc7-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85dc7-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85dc7-135">-WhatIf</span></span>
<span data-ttu-id="85dc7-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85dc7-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85dc7-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85dc7-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85dc7-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85dc7-138">CommonParameters</span></span>
<span data-ttu-id="85dc7-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85dc7-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85dc7-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85dc7-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85dc7-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85dc7-141">INPUTS</span></span>

### <span data-ttu-id="85dc7-142">System.String</span><span class="sxs-lookup"><span data-stu-id="85dc7-142">System.String</span></span>

### <span data-ttu-id="85dc7-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="85dc7-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="85dc7-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85dc7-144">OUTPUTS</span></span>

### <span data-ttu-id="85dc7-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85dc7-145">System.Boolean</span></span>

## <span data-ttu-id="85dc7-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85dc7-146">NOTES</span></span>

## <span data-ttu-id="85dc7-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85dc7-147">RELATED LINKS</span></span>
