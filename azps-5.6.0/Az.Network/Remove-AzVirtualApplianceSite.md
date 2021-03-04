---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualappliancesite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualApplianceSite.md
ms.openlocfilehash: 1456acb101302297e807d6d46bf83183e8a6e523
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945881"
---
# <span data-ttu-id="d9cfb-101">Remove-AzVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d9cfb-101">Remove-AzVirtualApplianceSite</span></span>

## <span data-ttu-id="d9cfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9cfb-102">SYNOPSIS</span></span>
<span data-ttu-id="d9cfb-103">Entfernen Einer virtuellen Gerätewebsite aus einer Virtuellen Netzwerkgerätressource.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-103">Remove a virtual appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d9cfb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d9cfb-104">SYNTAX</span></span>

### <span data-ttu-id="d9cfb-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9cfb-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzVirtualApplianceSite -Name <String> -NetworkVirtualApplianceId <String> -ResourceGroupName <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9cfb-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cfb-106">ResourceIdParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9cfb-107">ResourceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d9cfb-107">ResourceObjectParameterSet</span></span>
```
Remove-AzVirtualApplianceSite -VirtualApplianceSite <PSVirtualApplianceSite> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9cfb-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d9cfb-108">DESCRIPTION</span></span>
<span data-ttu-id="d9cfb-109">Mit Remove-AzVirtualApplianceSite befehl wird eine Virtual Appliance-Website aus einer Virtuellen Netzwerkgerätressource entfernt.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-109">The Remove-AzVirtualApplianceSite command removes a Virtual Appliance site from a Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="d9cfb-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d9cfb-110">EXAMPLES</span></span>

### <span data-ttu-id="d9cfb-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d9cfb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualApplianceSite -Name testsite -ResourceGroupName testrg -NetworkVirtualApplianceId $nva.Id
```

<span data-ttu-id="d9cfb-112">Löschen Sie eine Websiteressource für virtuelle Geräte.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-112">Delete a Virtual Appliance site resource.</span></span> 

## <span data-ttu-id="d9cfb-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d9cfb-113">PARAMETERS</span></span>

### <span data-ttu-id="d9cfb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9cfb-114">-AsJob</span></span>
<span data-ttu-id="d9cfb-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9cfb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9cfb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9cfb-116">-DefaultProfile</span></span>
<span data-ttu-id="d9cfb-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9cfb-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d9cfb-118">-Force</span></span>
<span data-ttu-id="d9cfb-119">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d9cfb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d9cfb-120">-Name</span></span>
<span data-ttu-id="d9cfb-121">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-121">The resource name.</span></span>

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

### <span data-ttu-id="d9cfb-122">-NetworkVirtualApplianceId</span><span class="sxs-lookup"><span data-stu-id="d9cfb-122">-NetworkVirtualApplianceId</span></span>
<span data-ttu-id="d9cfb-123">Die Ressourcen-ID der virtuellen Netzwerkgeräte, die dieser Website zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-123">The resource ID of the Network Virtual Appliance associated with this site.</span></span>

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

### <span data-ttu-id="d9cfb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9cfb-124">-PassThru</span></span>
<span data-ttu-id="d9cfb-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-125">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="d9cfb-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="d9cfb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9cfb-127">-ResourceGroupName</span></span>
<span data-ttu-id="d9cfb-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-128">The resource group name.</span></span>

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

### <span data-ttu-id="d9cfb-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9cfb-129">-ResourceId</span></span>
<span data-ttu-id="d9cfb-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-130">The resource id.</span></span>

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

### <span data-ttu-id="d9cfb-131">-VirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d9cfb-131">-VirtualApplianceSite</span></span>
<span data-ttu-id="d9cfb-132">Das Websiteobjekt der virtuellen Einheit.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-132">The virtual appliance site object.</span></span>

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

### <span data-ttu-id="d9cfb-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9cfb-133">-Confirm</span></span>
<span data-ttu-id="d9cfb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9cfb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9cfb-135">-WhatIf</span></span>
<span data-ttu-id="d9cfb-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9cfb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9cfb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9cfb-138">CommonParameters</span></span>
<span data-ttu-id="d9cfb-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9cfb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9cfb-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9cfb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9cfb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d9cfb-141">INPUTS</span></span>

### <span data-ttu-id="d9cfb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d9cfb-142">System.String</span></span>

### <span data-ttu-id="d9cfb-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span><span class="sxs-lookup"><span data-stu-id="d9cfb-143">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSite</span></span>

## <span data-ttu-id="d9cfb-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d9cfb-144">OUTPUTS</span></span>

### <span data-ttu-id="d9cfb-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d9cfb-145">System.Boolean</span></span>

## <span data-ttu-id="d9cfb-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d9cfb-146">NOTES</span></span>

## <span data-ttu-id="d9cfb-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d9cfb-147">RELATED LINKS</span></span>
