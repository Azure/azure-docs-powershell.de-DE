---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146724"
---
# <span data-ttu-id="cc77f-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="cc77f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc77f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc77f-103">Entfernt ein CustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="cc77f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc77f-104">SYNTAX</span></span>

### <span data-ttu-id="cc77f-105">DeleteByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc77f-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc77f-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc77f-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc77f-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cc77f-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc77f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc77f-108">DESCRIPTION</span></span>
<span data-ttu-id="cc77f-109">Das **Cmdlet "Remove-AzCustomIpPrefix"** entfernt ein CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="cc77f-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="cc77f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc77f-110">EXAMPLES</span></span>

### <span data-ttu-id="cc77f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cc77f-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="cc77f-112">Entfernt das CustomIpPrefix mit name $prefixName aus der Ressourcengruppe $rgName</span><span class="sxs-lookup"><span data-stu-id="cc77f-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="cc77f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc77f-113">PARAMETERS</span></span>

### <span data-ttu-id="cc77f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cc77f-114">-AsJob</span></span>
<span data-ttu-id="cc77f-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="cc77f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cc77f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc77f-116">-DefaultProfile</span></span>
<span data-ttu-id="cc77f-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc77f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc77f-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cc77f-118">-Force</span></span>
<span data-ttu-id="cc77f-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="cc77f-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cc77f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc77f-120">-InputObject</span></span>
<span data-ttu-id="cc77f-121">Ein customIpPrefix-Objekt.</span><span class="sxs-lookup"><span data-stu-id="cc77f-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc77f-122">-Name</span><span class="sxs-lookup"><span data-stu-id="cc77f-122">-Name</span></span>
<span data-ttu-id="cc77f-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="cc77f-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc77f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc77f-124">-PassThru</span></span>
<span data-ttu-id="cc77f-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc77f-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc77f-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cc77f-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc77f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc77f-127">-ResourceGroupName</span></span>
<span data-ttu-id="cc77f-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc77f-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc77f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cc77f-129">-ResourceId</span></span>
<span data-ttu-id="cc77f-130">Die Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="cc77f-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cc77f-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc77f-131">-Confirm</span></span>
<span data-ttu-id="cc77f-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc77f-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc77f-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc77f-133">-WhatIf</span></span>
<span data-ttu-id="cc77f-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc77f-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc77f-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc77f-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc77f-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc77f-136">CommonParameters</span></span>
<span data-ttu-id="cc77f-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc77f-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc77f-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc77f-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc77f-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc77f-139">INPUTS</span></span>

### <span data-ttu-id="cc77f-140">System.String</span><span class="sxs-lookup"><span data-stu-id="cc77f-140">System.String</span></span>

### <span data-ttu-id="cc77f-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="cc77f-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc77f-142">OUTPUTS</span></span>

### <span data-ttu-id="cc77f-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cc77f-143">System.Boolean</span></span>

## <span data-ttu-id="cc77f-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc77f-144">NOTES</span></span>

## <span data-ttu-id="cc77f-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc77f-145">RELATED LINKS</span></span>

[<span data-ttu-id="cc77f-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="cc77f-147">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="cc77f-148">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="cc77f-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)