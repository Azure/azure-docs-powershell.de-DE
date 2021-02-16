---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualnetworktap
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualNetworkTap.md
ms.openlocfilehash: bfe1c586d85a44460b1adbb84942be9b556973dd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146684"
---
# <span data-ttu-id="f7577-101">Remove-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7577-101">Remove-AzVirtualNetworkTap</span></span>

## <span data-ttu-id="f7577-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7577-102">SYNOPSIS</span></span>
<span data-ttu-id="f7577-103">Entfernt das Anzapfen eines virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f7577-103">Removes a virtual network tap.</span></span>

## <span data-ttu-id="f7577-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7577-104">SYNTAX</span></span>

### <span data-ttu-id="f7577-105">RemoveByNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7577-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzVirtualNetworkTap -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7577-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7577-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7577-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7577-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzVirtualNetworkTap -InputObject <PSVirtualNetworkTap> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7577-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7577-108">DESCRIPTION</span></span>
<span data-ttu-id="f7577-109">Das **Cmdlet "Remove-AzVirtualNetworkTap"** entfernt das Anzapfen eines virtuellen Azure-Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f7577-109">The **Remove-AzVirtualNetworkTap** cmdlet removes an Azure virtual network tap.</span></span>

## <span data-ttu-id="f7577-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7577-110">EXAMPLES</span></span>

### <span data-ttu-id="f7577-111">Beispiel 1: Entfernen der Anzapfung eines virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="f7577-111">Example 1: Remove a virtual network tap</span></span>
```
PS C:\>Remove-AzNetworkInterface -Name "VirtualNetworkTap1" -ResourceGroup "ResourceGroup1"
```

<span data-ttu-id="f7577-112">Mit diesem Befehl wird VirtualNetworkTap1 in der Ressourcengruppe "ResourceGroup1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="f7577-112">This command removes the VirtualNetworkTap1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="f7577-113">Da der *Parameter "Force"* nicht verwendet wird, wird der Benutzer aufgefordert, diese Aktion zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="f7577-113">Because the *Force* parameter is not used, the user will be prompted to confirm this action.</span></span>

## <span data-ttu-id="f7577-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7577-114">PARAMETERS</span></span>

### <span data-ttu-id="f7577-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7577-115">-AsJob</span></span>
<span data-ttu-id="f7577-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f7577-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7577-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7577-117">-DefaultProfile</span></span>
<span data-ttu-id="f7577-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7577-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7577-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f7577-119">-Force</span></span>
<span data-ttu-id="f7577-120">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="f7577-120">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="f7577-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7577-121">-InputObject</span></span>
<span data-ttu-id="f7577-122">Verweis auf die Ressource "VirtualNetworkTap"</span><span class="sxs-lookup"><span data-stu-id="f7577-122">Reference to VirtualNetworkTap resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7577-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f7577-123">-Name</span></span>
<span data-ttu-id="f7577-124">Der Name des Tippens.</span><span class="sxs-lookup"><span data-stu-id="f7577-124">The name of the tap.</span></span>

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

### <span data-ttu-id="f7577-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7577-125">-PassThru</span></span>
<span data-ttu-id="f7577-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="f7577-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f7577-127">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="f7577-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f7577-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7577-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7577-129">Der Ressourcengruppenname des Anzapfens des virtuellen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f7577-129">The resource group name of the virtual network tap.</span></span>

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

### <span data-ttu-id="f7577-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7577-130">-ResourceId</span></span>
<span data-ttu-id="f7577-131">VirtualNetworkTap resourceId</span><span class="sxs-lookup"><span data-stu-id="f7577-131">VirtualNetworkTap resourceId</span></span>

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

### <span data-ttu-id="f7577-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7577-132">-Confirm</span></span>
<span data-ttu-id="f7577-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7577-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7577-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7577-134">-WhatIf</span></span>
<span data-ttu-id="f7577-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7577-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7577-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7577-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7577-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7577-137">CommonParameters</span></span>
<span data-ttu-id="f7577-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7577-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7577-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7577-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7577-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7577-140">INPUTS</span></span>

### <span data-ttu-id="f7577-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f7577-141">System.String</span></span>

### <span data-ttu-id="f7577-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7577-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkTap</span></span>

## <span data-ttu-id="f7577-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7577-143">OUTPUTS</span></span>

### <span data-ttu-id="f7577-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7577-144">System.Boolean</span></span>

## <span data-ttu-id="f7577-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7577-145">NOTES</span></span>

## <span data-ttu-id="f7577-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7577-146">RELATED LINKS</span></span>

[<span data-ttu-id="f7577-147">Get-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7577-147">Get-AzVirtualNetworkTap</span></span>](./Get-AzVirtualNetworkTap.md)

[<span data-ttu-id="f7577-148">New-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7577-148">New-AzVirtualNetworkTap</span></span>](./New-AzVirtualNetworkTap.md)

[<span data-ttu-id="f7577-149">Set-AzVirtualNetworkTap</span><span class="sxs-lookup"><span data-stu-id="f7577-149">Set-AzVirtualNetworkTap</span></span>](./Set-AzVirtualNetworkTap.md)
