---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azpublicipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPublicIpPrefix.md
ms.openlocfilehash: d0ed76dfc656e52ec7f83344346957334627e086
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473446"
---
# <span data-ttu-id="0f171-101">Remove-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f171-101">Remove-AzPublicIpPrefix</span></span>

## <span data-ttu-id="0f171-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f171-102">SYNOPSIS</span></span>
<span data-ttu-id="0f171-103">Entfernt ein öffentliches IP-Präfix.</span><span class="sxs-lookup"><span data-stu-id="0f171-103">Removes a public IP prefix</span></span>

## <span data-ttu-id="0f171-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0f171-104">SYNTAX</span></span>

### <span data-ttu-id="0f171-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0f171-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzPublicIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f171-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f171-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzPublicIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f171-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f171-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzPublicIpPrefix -InputObject <PSPublicIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f171-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0f171-108">DESCRIPTION</span></span>
<span data-ttu-id="0f171-109">Das **Cmdlet "Remove-AzPublicIpPrefix"** entfernt ein öffentliches Azure-IP-Präfix, solange keine öffentlichen IP-Adressen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="0f171-109">The **Remove-AzPublicIpPrefix** cmdlet removes an Azure public IP prefix as long as there are no public IP addresses allocated from it.</span></span>

## <span data-ttu-id="0f171-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0f171-110">EXAMPLES</span></span>

### <span data-ttu-id="0f171-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0f171-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzPublicIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="0f171-112">Entfernt das öffentliche IP-Präfix mit name $prefixName aus der Ressourcengruppe $rgName</span><span class="sxs-lookup"><span data-stu-id="0f171-112">Removes the public IP prefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="0f171-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f171-113">PARAMETERS</span></span>

### <span data-ttu-id="0f171-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f171-114">-AsJob</span></span>
<span data-ttu-id="0f171-115">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0f171-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f171-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f171-116">-DefaultProfile</span></span>
<span data-ttu-id="0f171-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0f171-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f171-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0f171-118">-Force</span></span>
<span data-ttu-id="0f171-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="0f171-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0f171-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0f171-120">-InputObject</span></span>
<span data-ttu-id="0f171-121">Ein PublicIpPrefix-Objekt</span><span class="sxs-lookup"><span data-stu-id="0f171-121">A PublicIpPrefix object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f171-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0f171-122">-Name</span></span>
<span data-ttu-id="0f171-123">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="0f171-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f171-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0f171-124">-PassThru</span></span>
<span data-ttu-id="0f171-125">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0f171-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0f171-126">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0f171-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0f171-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f171-127">-ResourceGroupName</span></span>
<span data-ttu-id="0f171-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0f171-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f171-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f171-129">-ResourceId</span></span>
<span data-ttu-id="0f171-130">Die resourceId für die zu entfernende Ressource</span><span class="sxs-lookup"><span data-stu-id="0f171-130">The resourceId for the resource to remove</span></span>

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

### <span data-ttu-id="0f171-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f171-131">-Confirm</span></span>
<span data-ttu-id="0f171-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0f171-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f171-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0f171-133">-WhatIf</span></span>
<span data-ttu-id="0f171-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0f171-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f171-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0f171-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f171-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f171-136">CommonParameters</span></span>
<span data-ttu-id="0f171-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f171-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f171-138">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f171-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f171-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0f171-139">INPUTS</span></span>

### <span data-ttu-id="0f171-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0f171-140">System.String</span></span>

### <span data-ttu-id="0f171-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f171-141">Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix</span></span>

## <span data-ttu-id="0f171-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0f171-142">OUTPUTS</span></span>

### <span data-ttu-id="0f171-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0f171-143">System.Boolean</span></span>

## <span data-ttu-id="0f171-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0f171-144">NOTES</span></span>

## <span data-ttu-id="0f171-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0f171-145">RELATED LINKS</span></span>

[<span data-ttu-id="0f171-146">Get-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f171-146">Get-AzPublicIpPrefix</span></span>](./Get-AzPublicIpPrefix.md)

[<span data-ttu-id="0f171-147">New-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f171-147">New-AzPublicIpPrefix</span></span>](./New-AzPublicIpPrefix.md)

[<span data-ttu-id="0f171-148">Set-AzPublicIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0f171-148">Set-AzPublicIpPrefix</span></span>](./Set-AzPublicIpPrefix.md)
