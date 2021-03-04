---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: e8a9c1f65c536abb3c7b3e7aa983292ccde925a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941627"
---
# <span data-ttu-id="3f12d-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="3f12d-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="3f12d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f12d-102">SYNOPSIS</span></span>
<span data-ttu-id="3f12d-103">Löscht eine Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="3f12d-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="3f12d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f12d-104">SYNTAX</span></span>

### <span data-ttu-id="3f12d-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f12d-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f12d-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f12d-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f12d-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3f12d-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f12d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f12d-108">DESCRIPTION</span></span>
<span data-ttu-id="3f12d-109">Das **Cmdlet Remove-AzIpAllocation** löscht eine Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="3f12d-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="3f12d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f12d-110">EXAMPLES</span></span>

### <span data-ttu-id="3f12d-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3f12d-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="3f12d-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f12d-112">PARAMETERS</span></span>

### <span data-ttu-id="3f12d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f12d-113">-AsJob</span></span>
<span data-ttu-id="3f12d-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3f12d-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f12d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f12d-115">-DefaultProfile</span></span>
<span data-ttu-id="3f12d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f12d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f12d-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="3f12d-117">-Force</span></span>
<span data-ttu-id="3f12d-118">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="3f12d-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="3f12d-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3f12d-119">-InputObject</span></span>
<span data-ttu-id="3f12d-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="3f12d-120">{{ Fill InputObject Description }}</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTopLevelResource
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3f12d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3f12d-121">-Name</span></span>
<span data-ttu-id="3f12d-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="3f12d-122">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f12d-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3f12d-123">-PassThru</span></span>
<span data-ttu-id="3f12d-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3f12d-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3f12d-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3f12d-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3f12d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f12d-126">-ResourceGroupName</span></span>
<span data-ttu-id="3f12d-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3f12d-127">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3f12d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3f12d-128">-ResourceId</span></span>
<span data-ttu-id="3f12d-129">IpAllocation-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3f12d-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="3f12d-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f12d-130">-Confirm</span></span>
<span data-ttu-id="3f12d-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f12d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f12d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f12d-132">-WhatIf</span></span>
<span data-ttu-id="3f12d-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f12d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f12d-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f12d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f12d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f12d-135">CommonParameters</span></span>
<span data-ttu-id="3f12d-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f12d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f12d-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f12d-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f12d-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f12d-138">INPUTS</span></span>

### <span data-ttu-id="3f12d-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3f12d-139">System.String</span></span>

## <span data-ttu-id="3f12d-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f12d-140">OUTPUTS</span></span>

### <span data-ttu-id="3f12d-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3f12d-141">System.Boolean</span></span>

## <span data-ttu-id="3f12d-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f12d-142">NOTES</span></span>

## <span data-ttu-id="3f12d-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f12d-143">RELATED LINKS</span></span>
