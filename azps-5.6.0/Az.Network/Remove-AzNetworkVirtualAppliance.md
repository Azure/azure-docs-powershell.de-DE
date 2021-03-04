---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-aznetworkvirtualappliance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzNetworkVirtualAppliance.md
ms.openlocfilehash: b75eb7e9bbac3efddc49bcccf384f288c01960a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941571"
---
# <span data-ttu-id="de233-101">Remove-AzNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="de233-101">Remove-AzNetworkVirtualAppliance</span></span>

## <span data-ttu-id="de233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de233-102">SYNOPSIS</span></span>
<span data-ttu-id="de233-103">Entfernen Sie eine Virtuelle Netzwerkgeräteressource.</span><span class="sxs-lookup"><span data-stu-id="de233-103">Remove a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="de233-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de233-104">SYNTAX</span></span>

### <span data-ttu-id="de233-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="de233-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzNetworkVirtualAppliance -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de233-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="de233-106">ResourceIdParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de233-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="de233-107">ResourceObjectParameterSet</span></span>
```
Remove-AzNetworkVirtualAppliance -NetworkVirtualAppliance <PSNetworkVirtualAppliance> [-Force] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de233-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de233-108">DESCRIPTION</span></span>
<span data-ttu-id="de233-109">Mit Remove-AzNetworkVirtualAppliance befehl wird eine Virtuelle Netzwerkgerätressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="de233-109">The Remove-AzNetworkVirtualAppliance command removes a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="de233-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de233-110">EXAMPLES</span></span>

### <span data-ttu-id="de233-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de233-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzNetworkVirtualAppliance -ResourceGroupName testrg -Name nva
```

<span data-ttu-id="de233-112">Löschen Einer virtuellen Netzwerkgerätressource.</span><span class="sxs-lookup"><span data-stu-id="de233-112">Delete a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="de233-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="de233-113">PARAMETERS</span></span>

### <span data-ttu-id="de233-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de233-114">-AsJob</span></span>
<span data-ttu-id="de233-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="de233-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de233-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de233-116">-DefaultProfile</span></span>
<span data-ttu-id="de233-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de233-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de233-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="de233-118">-Force</span></span>
<span data-ttu-id="de233-119">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="de233-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="de233-120">-Name</span><span class="sxs-lookup"><span data-stu-id="de233-120">-Name</span></span>
<span data-ttu-id="de233-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="de233-121">The resource name.</span></span>

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

### <span data-ttu-id="de233-122">-NetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="de233-122">-NetworkVirtualAppliance</span></span>
<span data-ttu-id="de233-123">Das Ressourcenobjekt.</span><span class="sxs-lookup"><span data-stu-id="de233-123">The resource object.</span></span>

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

### <span data-ttu-id="de233-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="de233-124">-PassThru</span></span>
<span data-ttu-id="de233-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="de233-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="de233-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="de233-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="de233-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de233-127">-ResourceGroupName</span></span>
<span data-ttu-id="de233-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="de233-128">The resource group name.</span></span>

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

### <span data-ttu-id="de233-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="de233-129">-ResourceId</span></span>
<span data-ttu-id="de233-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="de233-130">The Resource Id.</span></span>

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

### <span data-ttu-id="de233-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="de233-131">-Confirm</span></span>
<span data-ttu-id="de233-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de233-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de233-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="de233-133">-WhatIf</span></span>
<span data-ttu-id="de233-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de233-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de233-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de233-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de233-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de233-136">CommonParameters</span></span>
<span data-ttu-id="de233-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de233-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de233-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="de233-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de233-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de233-139">INPUTS</span></span>

### <span data-ttu-id="de233-140">System.String</span><span class="sxs-lookup"><span data-stu-id="de233-140">System.String</span></span>

### <span data-ttu-id="de233-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span><span class="sxs-lookup"><span data-stu-id="de233-141">Microsoft.Azure.Commands.Network.Models.PSNetworkVirtualAppliance</span></span>

## <span data-ttu-id="de233-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de233-142">OUTPUTS</span></span>

### <span data-ttu-id="de233-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="de233-143">System.Boolean</span></span>

## <span data-ttu-id="de233-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="de233-144">NOTES</span></span>

## <span data-ttu-id="de233-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="de233-145">RELATED LINKS</span></span>
