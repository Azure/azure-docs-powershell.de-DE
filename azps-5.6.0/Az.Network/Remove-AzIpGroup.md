---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azipgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpGroup.md
ms.openlocfilehash: f1c8589663008b0ebc640a052199a11c82d3b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941619"
---
# <span data-ttu-id="7510b-101">Remove-AzIpGroup</span><span class="sxs-lookup"><span data-stu-id="7510b-101">Remove-AzIpGroup</span></span>

## <span data-ttu-id="7510b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7510b-102">SYNOPSIS</span></span>
<span data-ttu-id="7510b-103">Löscht eine Azure IpGroup.</span><span class="sxs-lookup"><span data-stu-id="7510b-103">Deletes an Azure IpGroup.</span></span>

## <span data-ttu-id="7510b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7510b-104">SYNTAX</span></span>

### <span data-ttu-id="7510b-105">IpGroupNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7510b-105">IpGroupNameParameterSet</span></span>
```
Remove-AzIpGroup -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7510b-106">IpGroupInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7510b-106">IpGroupInputObjectParameterSet</span></span>
```
Remove-AzIpGroup -IpGroup <PSIpGroup> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7510b-107">IpGroupResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7510b-107">IpGroupResourceIdParameterSet</span></span>
```
Remove-AzIpGroup -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7510b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7510b-108">DESCRIPTION</span></span>
<span data-ttu-id="7510b-109">Das **Cmdlet Remove-AzIpGroup** löscht eine Azure IpGroup</span><span class="sxs-lookup"><span data-stu-id="7510b-109">The **Remove-AzIpGroup** cmdlet deletes an Azure IpGroup</span></span>

## <span data-ttu-id="7510b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7510b-110">EXAMPLES</span></span>

### <span data-ttu-id="7510b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7510b-111">Example 1</span></span>
```powershell
Remove-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
```

### <span data-ttu-id="7510b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7510b-112">Example 2</span></span>
```powershell
$ipGroupId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/ipGroupRG/providers/Microsoft.Network/ipGroups/ipGroup'
Remove-AzIpGroup -ResourceId $ipGroupId
```

### <span data-ttu-id="7510b-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7510b-113">Example 3</span></span>
```powershell
$ipGroup = Get-AzIpGroup -ResourceGroupName ipGroupRG -Name ipGroup
Remove-AzIpGroup -IpGroup $ipGroup
```

## <span data-ttu-id="7510b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7510b-114">PARAMETERS</span></span>

### <span data-ttu-id="7510b-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7510b-115">-AsJob</span></span>
<span data-ttu-id="7510b-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7510b-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7510b-117">-DefaultProfile</span></span>
<span data-ttu-id="7510b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7510b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="7510b-119">-Force</span></span>
<span data-ttu-id="7510b-120">Bitten Sie nicht um Bestätigung, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="7510b-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-121">-IpGroup</span><span class="sxs-lookup"><span data-stu-id="7510b-121">-IpGroup</span></span>
<span data-ttu-id="7510b-122">Das ipGroup-Eingabeobjekt.</span><span class="sxs-lookup"><span data-stu-id="7510b-122">The ipGroup input object.</span></span>

```yaml
Type: PSIpGroup
Parameter Sets: IpGroupInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7510b-123">-Name</span></span>
<span data-ttu-id="7510b-124">Der Name der ipgroup.</span><span class="sxs-lookup"><span data-stu-id="7510b-124">The name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7510b-125">-PassThru</span></span>
<span data-ttu-id="7510b-126">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7510b-126">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7510b-127">-ResourceGroupName</span></span>
<span data-ttu-id="7510b-128">Der Ressourcengruppenname der IP-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7510b-128">The resource group name of the ipgroup.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7510b-129">-ResourceId</span></span>
<span data-ttu-id="7510b-130">Die ipgroup-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="7510b-130">The ipgroup resource Id.</span></span>

```yaml
Type: String
Parameter Sets: IpGroupResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7510b-131">-Confirm</span></span>
<span data-ttu-id="7510b-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7510b-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7510b-133">-WhatIf</span></span>
<span data-ttu-id="7510b-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7510b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7510b-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7510b-135">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7510b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7510b-136">CommonParameters</span></span>
<span data-ttu-id="7510b-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7510b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7510b-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7510b-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7510b-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7510b-139">INPUTS</span></span>

### <span data-ttu-id="7510b-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7510b-140">System.String</span></span>

### <span data-ttu-id="7510b-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span><span class="sxs-lookup"><span data-stu-id="7510b-141">Microsoft.Azure.Commands.Network.Models.PSIpGroup</span></span>

## <span data-ttu-id="7510b-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7510b-142">OUTPUTS</span></span>

### <span data-ttu-id="7510b-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7510b-143">System.Boolean</span></span>

## <span data-ttu-id="7510b-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="7510b-144">NOTES</span></span>

## <span data-ttu-id="7510b-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="7510b-145">RELATED LINKS</span></span>
