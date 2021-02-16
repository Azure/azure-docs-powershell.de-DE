---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160689"
---
# <span data-ttu-id="601d4-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="601d4-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="601d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="601d4-102">SYNOPSIS</span></span>
<span data-ttu-id="601d4-103">Löschen Sie eine Hubroutentabelle, die einem VirtualHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="601d4-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="601d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="601d4-104">SYNTAX</span></span>

### <span data-ttu-id="601d4-105">ByVHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="601d4-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601d4-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="601d4-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601d4-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="601d4-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="601d4-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="601d4-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="601d4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="601d4-109">DESCRIPTION</span></span>
<span data-ttu-id="601d4-110">Löscht die angegebene Hubroutentabelle, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="601d4-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="601d4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="601d4-111">EXAMPLES</span></span>

### <span data-ttu-id="601d4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="601d4-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="601d4-113">Mit diesem Befehl wird die Hubroutentabelle des virtuellen Hubs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="601d4-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="601d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="601d4-114">PARAMETERS</span></span>

### <span data-ttu-id="601d4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="601d4-115">-AsJob</span></span>
<span data-ttu-id="601d4-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="601d4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="601d4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601d4-117">-DefaultProfile</span></span>
<span data-ttu-id="601d4-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="601d4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601d4-119">-Force</span><span class="sxs-lookup"><span data-stu-id="601d4-119">-Force</span></span>
<span data-ttu-id="601d4-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="601d4-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="601d4-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="601d4-121">-InputObject</span></span>
<span data-ttu-id="601d4-122">Die zu entfernende vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="601d4-122">The vhubroutetable resource to remove.</span></span>

```yaml
Type: PSVHubRouteTable
Parameter Sets: ByVHubRouteTableObject
Aliases: VHubRouteTable, RouteTable

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-123">-Name</span><span class="sxs-lookup"><span data-stu-id="601d4-123">-Name</span></span>
<span data-ttu-id="601d4-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="601d4-124">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="601d4-125">-ParentObject</span></span>
<span data-ttu-id="601d4-126">Das übergeordnete virtuelle Hubobjekt dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="601d4-126">The parent virtual hub object of this resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, VirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="601d4-127">-ParentResourceName</span></span>
<span data-ttu-id="601d4-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="601d4-128">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="601d4-129">-PassThru</span></span>
<span data-ttu-id="601d4-130">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="601d4-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="601d4-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="601d4-131">-ResourceGroupName</span></span>
<span data-ttu-id="601d4-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="601d4-132">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="601d4-133">-ResourceId</span></span>
<span data-ttu-id="601d4-134">Die Ressourcen-ID der zu entfernende vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="601d4-134">The resource id of the vhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVHubRouteTableResourceId
Aliases: VHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="601d4-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="601d4-135">-Confirm</span></span>
<span data-ttu-id="601d4-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="601d4-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="601d4-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="601d4-137">-WhatIf</span></span>
<span data-ttu-id="601d4-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="601d4-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="601d4-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="601d4-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="601d4-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601d4-140">CommonParameters</span></span>
<span data-ttu-id="601d4-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601d4-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601d4-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="601d4-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601d4-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="601d4-143">INPUTS</span></span>

### <span data-ttu-id="601d4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="601d4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="601d4-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="601d4-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="601d4-146">System.String</span><span class="sxs-lookup"><span data-stu-id="601d4-146">System.String</span></span>

## <span data-ttu-id="601d4-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="601d4-147">OUTPUTS</span></span>

### <span data-ttu-id="601d4-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="601d4-148">System.Boolean</span></span>

## <span data-ttu-id="601d4-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="601d4-149">NOTES</span></span>

## <span data-ttu-id="601d4-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="601d4-150">RELATED LINKS</span></span>

[<span data-ttu-id="601d4-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="601d4-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="601d4-152">New-AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="601d4-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="601d4-153">New-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="601d4-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="601d4-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="601d4-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)