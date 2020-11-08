---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVHubRouteTable.md
ms.openlocfilehash: e55822ee4364022c7abca0d5daf8189dd7405067
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178308"
---
# <span data-ttu-id="01ffc-101">Remove-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01ffc-101">Remove-AzVHubRouteTable</span></span>

## <span data-ttu-id="01ffc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="01ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="01ffc-103">Löschen Sie eine Hub-Route-Tabellen Ressource, die einem VirtualHub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01ffc-103">Delete a hub route table resource associated with a VirtualHub.</span></span>

## <span data-ttu-id="01ffc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="01ffc-104">SYNTAX</span></span>

### <span data-ttu-id="01ffc-105">ByVHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01ffc-105">ByVHubRouteTableName (Default)</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceGroupName <String> -ParentResourceName <String> -Name <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ffc-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="01ffc-106">ByVirtualHubObject</span></span>
```powershell
Remove-AzVHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ffc-107">ByVHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="01ffc-107">ByVHubRouteTableObject</span></span>
```powershell
Remove-AzVHubRouteTable [-InputObject <PSVHubRouteTable>] [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01ffc-108">ByVHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="01ffc-108">ByVHubRouteTableResourceId</span></span>
```powershell
Remove-AzVHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01ffc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="01ffc-109">DESCRIPTION</span></span>
<span data-ttu-id="01ffc-110">Löscht die angegebene Hub-Route-Tabelle, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="01ffc-110">Deletes the specified hub route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="01ffc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="01ffc-111">EXAMPLES</span></span>

### <span data-ttu-id="01ffc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="01ffc-112">Example 1</span></span>
```powershell
PS C:\> $testRouteTable = Get-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
PS C:\> Remove-AzVHubRouteTable -ResourceGroupName "testRg" -VirtualHubName "testHub" -Name "testRouteTable"
```

<span data-ttu-id="01ffc-113">Mit diesem Befehl wird die Hub-Route-Tabelle des virtuellen Hubs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="01ffc-113">This command deletes the hub route table of the virtual hub.</span></span>

## <span data-ttu-id="01ffc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="01ffc-114">PARAMETERS</span></span>

### <span data-ttu-id="01ffc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01ffc-115">-AsJob</span></span>
<span data-ttu-id="01ffc-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="01ffc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="01ffc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01ffc-117">-DefaultProfile</span></span>
<span data-ttu-id="01ffc-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="01ffc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01ffc-119">-Force</span><span class="sxs-lookup"><span data-stu-id="01ffc-119">-Force</span></span>
<span data-ttu-id="01ffc-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="01ffc-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="01ffc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="01ffc-121">-InputObject</span></span>
<span data-ttu-id="01ffc-122">Die zu entfernende vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="01ffc-122">The vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="01ffc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="01ffc-123">-Name</span></span>
<span data-ttu-id="01ffc-124">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="01ffc-124">The resource name.</span></span>

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

### <span data-ttu-id="01ffc-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="01ffc-125">-ParentObject</span></span>
<span data-ttu-id="01ffc-126">Das übergeordnete virtuelle Hub-Objekt dieser Ressource.</span><span class="sxs-lookup"><span data-stu-id="01ffc-126">The parent virtual hub object of this resource.</span></span>

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

### <span data-ttu-id="01ffc-127">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="01ffc-127">-ParentResourceName</span></span>
<span data-ttu-id="01ffc-128">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="01ffc-128">The parent resource name.</span></span>

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

### <span data-ttu-id="01ffc-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01ffc-129">-PassThru</span></span>
<span data-ttu-id="01ffc-130">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01ffc-130">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="01ffc-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01ffc-131">-ResourceGroupName</span></span>
<span data-ttu-id="01ffc-132">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="01ffc-132">The resource group name.</span></span>

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

### <span data-ttu-id="01ffc-133">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="01ffc-133">-ResourceId</span></span>
<span data-ttu-id="01ffc-134">Die Ressourcen-ID der zu entfernenden vhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="01ffc-134">The resource id of the vhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="01ffc-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="01ffc-135">-Confirm</span></span>
<span data-ttu-id="01ffc-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01ffc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01ffc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01ffc-137">-WhatIf</span></span>
<span data-ttu-id="01ffc-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01ffc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01ffc-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01ffc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01ffc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01ffc-140">CommonParameters</span></span>
<span data-ttu-id="01ffc-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01ffc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01ffc-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="01ffc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01ffc-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="01ffc-143">INPUTS</span></span>

### <span data-ttu-id="01ffc-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="01ffc-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="01ffc-145">Microsoft. Azure. Commands. Network. Models. PSVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01ffc-145">Microsoft.Azure.Commands.Network.Models.PSVHubRouteTable</span></span>

### <span data-ttu-id="01ffc-146">System. String</span><span class="sxs-lookup"><span data-stu-id="01ffc-146">System.String</span></span>

## <span data-ttu-id="01ffc-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="01ffc-147">OUTPUTS</span></span>

### <span data-ttu-id="01ffc-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="01ffc-148">System.Boolean</span></span>

## <span data-ttu-id="01ffc-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="01ffc-149">NOTES</span></span>

## <span data-ttu-id="01ffc-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="01ffc-150">RELATED LINKS</span></span>

[<span data-ttu-id="01ffc-151">Get-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01ffc-151">Get-AzVHubRouteTable</span></span>](./Get-AzVHubRouteTable.md)

[<span data-ttu-id="01ffc-152">Neu – AzVHubRoute</span><span class="sxs-lookup"><span data-stu-id="01ffc-152">New-AzVHubRoute</span></span>](./New-AzVHubRoute.md)

[<span data-ttu-id="01ffc-153">Neu – AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01ffc-153">New-AzVHubRouteTable</span></span>](./New-AzVHubRouteTable.md)

[<span data-ttu-id="01ffc-154">Update-AzVHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="01ffc-154">Update-AzVHubRouteTable</span></span>](./Update-AzVHubRouteTable.md)