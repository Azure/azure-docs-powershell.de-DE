---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172481"
---
# <span data-ttu-id="84604-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84604-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="84604-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84604-102">SYNOPSIS</span></span>
<span data-ttu-id="84604-103">Löschen Einer virtuellen Hub-Routentabelle-Ressource, die einem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84604-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="84604-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="84604-104">SYNTAX</span></span>

### <span data-ttu-id="84604-105">ByVirtualHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="84604-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84604-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="84604-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84604-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="84604-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="84604-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="84604-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="84604-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84604-109">DESCRIPTION</span></span>
<span data-ttu-id="84604-110">Löscht die angegebene Routentabelle, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="84604-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="84604-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="84604-111">EXAMPLES</span></span>

### <span data-ttu-id="84604-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="84604-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="84604-113">Mit diesem Befehl wird die routeTable1 des virtuellen Hubs "westushub" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="84604-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="84604-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="84604-114">PARAMETERS</span></span>

### <span data-ttu-id="84604-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="84604-115">-AsJob</span></span>
<span data-ttu-id="84604-116">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="84604-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="84604-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84604-117">-DefaultProfile</span></span>
<span data-ttu-id="84604-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="84604-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="84604-119">-Force</span><span class="sxs-lookup"><span data-stu-id="84604-119">-Force</span></span>
<span data-ttu-id="84604-120">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="84604-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="84604-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="84604-121">-HubName</span></span>
<span data-ttu-id="84604-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="84604-122">The parent resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases: VirtualHubName, ParentVirtualHubName, ParentResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84604-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="84604-123">-InputObject</span></span>
<span data-ttu-id="84604-124">Die zu entfernende Virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="84604-124">The virtualhubroutetable resource to remove.</span></span>

```yaml
Type: PSVirtualHubRouteTable
Parameter Sets: ByVirtualHubRouteTableObject
Aliases: VirtualHubRouteTable

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84604-125">-Name</span><span class="sxs-lookup"><span data-stu-id="84604-125">-Name</span></span>
<span data-ttu-id="84604-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="84604-126">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName, ByVirtualHubObject
Aliases: ResourceName, VirtualHubRouteTableName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84604-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="84604-127">-PassThru</span></span>
<span data-ttu-id="84604-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84604-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="84604-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84604-129">-ResourceGroupName</span></span>
<span data-ttu-id="84604-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="84604-130">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84604-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="84604-131">-ResourceId</span></span>
<span data-ttu-id="84604-132">Die Ressourcen-ID der zu entfernende Virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="84604-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubRouteTableResourceId
Aliases: VirtualHubRouteTableId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84604-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="84604-133">-VirtualHub</span></span>
<span data-ttu-id="84604-134">{{ Fill VirtualHub Description }}</span><span class="sxs-lookup"><span data-stu-id="84604-134">{{ Fill VirtualHub Description }}</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: ParentVirtualHub, ParentObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84604-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="84604-135">-Confirm</span></span>
<span data-ttu-id="84604-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84604-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84604-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="84604-137">-WhatIf</span></span>
<span data-ttu-id="84604-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84604-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="84604-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84604-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84604-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84604-140">CommonParameters</span></span>
<span data-ttu-id="84604-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84604-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84604-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="84604-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84604-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="84604-143">INPUTS</span></span>

### <span data-ttu-id="84604-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="84604-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="84604-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="84604-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="84604-146">System.String</span><span class="sxs-lookup"><span data-stu-id="84604-146">System.String</span></span>

## <span data-ttu-id="84604-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="84604-147">OUTPUTS</span></span>

### <span data-ttu-id="84604-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="84604-148">System.Boolean</span></span>

## <span data-ttu-id="84604-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="84604-149">NOTES</span></span>

## <span data-ttu-id="84604-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="84604-150">RELATED LINKS</span></span>
