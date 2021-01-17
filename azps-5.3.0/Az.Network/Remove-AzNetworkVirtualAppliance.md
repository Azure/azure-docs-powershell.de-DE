---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: e57b68db7e2ee285ef75e0ada33a6564574bb4ed
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468860"
---
# <span data-ttu-id="1fc53-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1fc53-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1fc53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fc53-102">SYNOPSIS</span></span>
<span data-ttu-id="1fc53-103">Entfernen Sie eine Network Virtual Appliance-Ressource.</span><span class="sxs-lookup"><span data-stu-id="1fc53-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1fc53-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1fc53-104">SYNTAX</span></span>

### <span data-ttu-id="1fc53-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fc53-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc53-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fc53-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fc53-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1fc53-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fc53-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1fc53-108">DESCRIPTION</span></span>
<span data-ttu-id="1fc53-109">Mit Remove-AzNetworkVirtualAppliance Befehl "Netzwerkgerät" wird eine Network Virtual Appliance-Ressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="1fc53-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1fc53-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1fc53-110">EXAMPLES</span></span>

### <span data-ttu-id="1fc53-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fc53-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="1fc53-112">Löschen sie eine Ressource des virtuellen Geräts im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="1fc53-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="1fc53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1fc53-113">PARAMETERS</span></span>

### <span data-ttu-id="1fc53-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1fc53-114">-AsJob</span></span>
<span data-ttu-id="1fc53-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="1fc53-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1fc53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fc53-116">-DefaultProfile</span></span>
<span data-ttu-id="1fc53-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1fc53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fc53-118">-Force</span><span class="sxs-lookup"><span data-stu-id="1fc53-118">-Force</span></span>
<span data-ttu-id="1fc53-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="1fc53-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="1fc53-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1fc53-120">-Name</span></span>
<span data-ttu-id="1fc53-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="1fc53-121">The resource name.</span></span>

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

### <span data-ttu-id="1fc53-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1fc53-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="1fc53-123">Das Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="1fc53-123">The resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance
Parameter Sets: ResourceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fc53-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fc53-124">-PassThru</span></span>
<span data-ttu-id="1fc53-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1fc53-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="1fc53-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="1fc53-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="1fc53-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fc53-127">-ResourceGroupName</span></span>
<span data-ttu-id="1fc53-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fc53-128">The resource group name.</span></span>

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

### <span data-ttu-id="1fc53-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fc53-129">-ResourceId</span></span>
<span data-ttu-id="1fc53-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1fc53-130">The Resource Id.</span></span>

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

### <span data-ttu-id="1fc53-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1fc53-131">-Confirm</span></span>
<span data-ttu-id="1fc53-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fc53-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fc53-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1fc53-133">-WhatIf</span></span>
<span data-ttu-id="1fc53-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fc53-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fc53-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fc53-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fc53-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fc53-136">CommonParameters</span></span>
<span data-ttu-id="1fc53-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fc53-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fc53-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1fc53-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fc53-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1fc53-139">INPUTS</span></span>

### <span data-ttu-id="1fc53-140">System.String</span><span class="sxs-lookup"><span data-stu-id="1fc53-140">System.String</span></span>

### <span data-ttu-id="1fc53-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="1fc53-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="1fc53-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1fc53-142">OUTPUTS</span></span>

### <span data-ttu-id="1fc53-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1fc53-143">System.Boolean</span></span>

## <span data-ttu-id="1fc53-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1fc53-144">NOTES</span></span>

## <span data-ttu-id="1fc53-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1fc53-145">RELATED LINKS</span></span>
