---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azipallocation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzIpAllocation.md
ms.openlocfilehash: 7a81ce555ed99de1504dc0625c0c83cdab6ab881
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363472"
---
# <span data-ttu-id="82b05-101">Remove-AzIpAllocation</span><span class="sxs-lookup"><span data-stu-id="82b05-101">Remove-AzIpAllocation</span></span>

## <span data-ttu-id="82b05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82b05-102">SYNOPSIS</span></span>
<span data-ttu-id="82b05-103">Löscht eine Azure IpAllocation.</span><span class="sxs-lookup"><span data-stu-id="82b05-103">Deletes an Azure IpAllocation.</span></span>

## <span data-ttu-id="82b05-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="82b05-104">SYNTAX</span></span>

### <span data-ttu-id="82b05-105">DeleteByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b05-105">DeleteByNameParameterSet</span></span>
```
Remove-AzIpAllocation [-Name] <String> [-ResourceGroupName] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82b05-106">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b05-106">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzIpAllocation [-InputObject] <PSTopLevelResource> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82b05-107">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82b05-107">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzIpAllocation [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82b05-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="82b05-108">DESCRIPTION</span></span>
<span data-ttu-id="82b05-109">Das **Cmdlet "Remove-AzIpAllocation"** löscht eine Azure IpAllocation</span><span class="sxs-lookup"><span data-stu-id="82b05-109">The **Remove-AzIpAllocation** cmdlet deletes an Azure IpAllocation</span></span>

## <span data-ttu-id="82b05-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="82b05-110">EXAMPLES</span></span>

### <span data-ttu-id="82b05-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82b05-111">Example 1</span></span>
```powershell
Remove-AzIpAllocation -ResourceGroupName 'TestResourceGroup' -Name 'TestIpAllocation'
```

## <span data-ttu-id="82b05-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="82b05-112">PARAMETERS</span></span>

### <span data-ttu-id="82b05-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="82b05-113">-AsJob</span></span>
<span data-ttu-id="82b05-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="82b05-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="82b05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82b05-115">-DefaultProfile</span></span>
<span data-ttu-id="82b05-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="82b05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82b05-117">-Force</span><span class="sxs-lookup"><span data-stu-id="82b05-117">-Force</span></span>
<span data-ttu-id="82b05-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="82b05-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="82b05-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="82b05-119">-InputObject</span></span>
<span data-ttu-id="82b05-120">{{ Fill InputObject Description }}</span><span class="sxs-lookup"><span data-stu-id="82b05-120">{{ Fill InputObject Description }}</span></span>

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

### <span data-ttu-id="82b05-121">-Name</span><span class="sxs-lookup"><span data-stu-id="82b05-121">-Name</span></span>
<span data-ttu-id="82b05-122">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="82b05-122">The resource name.</span></span>

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

### <span data-ttu-id="82b05-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82b05-123">-PassThru</span></span>
<span data-ttu-id="82b05-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="82b05-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="82b05-125">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="82b05-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="82b05-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82b05-126">-ResourceGroupName</span></span>
<span data-ttu-id="82b05-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="82b05-127">The resource group name.</span></span>

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

### <span data-ttu-id="82b05-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82b05-128">-ResourceId</span></span>
<span data-ttu-id="82b05-129">IpAllocation-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="82b05-129">IpAllocation resource id.</span></span>

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

### <span data-ttu-id="82b05-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="82b05-130">-Confirm</span></span>
<span data-ttu-id="82b05-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82b05-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82b05-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="82b05-132">-WhatIf</span></span>
<span data-ttu-id="82b05-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82b05-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82b05-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82b05-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82b05-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82b05-135">CommonParameters</span></span>
<span data-ttu-id="82b05-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82b05-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82b05-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="82b05-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82b05-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="82b05-138">INPUTS</span></span>

### <span data-ttu-id="82b05-139">System.String</span><span class="sxs-lookup"><span data-stu-id="82b05-139">System.String</span></span>

## <span data-ttu-id="82b05-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="82b05-140">OUTPUTS</span></span>

### <span data-ttu-id="82b05-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="82b05-141">System.Boolean</span></span>

## <span data-ttu-id="82b05-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="82b05-142">NOTES</span></span>

## <span data-ttu-id="82b05-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="82b05-143">RELATED LINKS</span></span>
