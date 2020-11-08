---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualhubroutetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubRouteTable.md
ms.openlocfilehash: e55cb0629bb6376253f0b8f0b636eb0b43bcb742
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009081"
---
# <span data-ttu-id="260b6-101">Remove-AzVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="260b6-101">Remove-AzVirtualHubRouteTable</span></span>

## <span data-ttu-id="260b6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="260b6-102">SYNOPSIS</span></span>
<span data-ttu-id="260b6-103">Löschen Sie eine virtuelle Hub-Routingtabellen Ressource, die einem virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="260b6-103">Delete a virtual hub route table resource associated with a virtual hub.</span></span>

## <span data-ttu-id="260b6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="260b6-104">SYNTAX</span></span>

### <span data-ttu-id="260b6-105">ByVirtualHubRouteTableName (Standard)</span><span class="sxs-lookup"><span data-stu-id="260b6-105">ByVirtualHubRouteTableName (Default)</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceGroupName <String> -HubName <String> -Name <String> [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260b6-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="260b6-106">ByVirtualHubObject</span></span>
```
Remove-AzVirtualHubRouteTable -Name <String> -VirtualHub <PSVirtualHub> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260b6-107">ByVirtualHubRouteTableObject</span><span class="sxs-lookup"><span data-stu-id="260b6-107">ByVirtualHubRouteTableObject</span></span>
```
Remove-AzVirtualHubRouteTable [-InputObject <PSVirtualHubRouteTable>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="260b6-108">ByVirtualHubRouteTableResourceId</span><span class="sxs-lookup"><span data-stu-id="260b6-108">ByVirtualHubRouteTableResourceId</span></span>
```
Remove-AzVirtualHubRouteTable -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="260b6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="260b6-109">DESCRIPTION</span></span>
<span data-ttu-id="260b6-110">Löscht die angegebene Routingtabelle, die dem angegebenen virtuellen Hub zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="260b6-110">Deletes the specified route table that is associated with the specified virtual hub.</span></span>

## <span data-ttu-id="260b6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="260b6-111">EXAMPLES</span></span>

### <span data-ttu-id="260b6-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="260b6-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzVirtualHubRouteTable�-ResourceGroupName�"testRg"�-HubName�"westushub"�-Name�"routeTable1"
```

<span data-ttu-id="260b6-113">Dieser Befehl löscht die routeTable1 des virtuellen Hub-westushub.</span><span class="sxs-lookup"><span data-stu-id="260b6-113">This command deletes the routeTable1 of the virtual hub westushub.</span></span>

## <span data-ttu-id="260b6-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="260b6-114">PARAMETERS</span></span>

### <span data-ttu-id="260b6-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="260b6-115">-AsJob</span></span>
<span data-ttu-id="260b6-116">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="260b6-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="260b6-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="260b6-117">-DefaultProfile</span></span>
<span data-ttu-id="260b6-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="260b6-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="260b6-119">-Force</span><span class="sxs-lookup"><span data-stu-id="260b6-119">-Force</span></span>
<span data-ttu-id="260b6-120">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="260b6-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="260b6-121">-HubName</span><span class="sxs-lookup"><span data-stu-id="260b6-121">-HubName</span></span>
<span data-ttu-id="260b6-122">Der Name der übergeordneten Ressource.</span><span class="sxs-lookup"><span data-stu-id="260b6-122">The parent resource name.</span></span>

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

### <span data-ttu-id="260b6-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="260b6-123">-InputObject</span></span>
<span data-ttu-id="260b6-124">Die zu entfernende virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="260b6-124">The virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="260b6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="260b6-125">-Name</span></span>
<span data-ttu-id="260b6-126">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="260b6-126">The resource name.</span></span>

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

### <span data-ttu-id="260b6-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="260b6-127">-PassThru</span></span>
<span data-ttu-id="260b6-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="260b6-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="260b6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="260b6-129">-ResourceGroupName</span></span>
<span data-ttu-id="260b6-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="260b6-130">The resource group name.</span></span>

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

### <span data-ttu-id="260b6-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="260b6-131">-ResourceId</span></span>
<span data-ttu-id="260b6-132">Die Ressourcen-ID der zu entfernenden virtualhubroutetable-Ressource.</span><span class="sxs-lookup"><span data-stu-id="260b6-132">The resource id of the virtualhubroutetable resource to remove.</span></span>

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

### <span data-ttu-id="260b6-133">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="260b6-133">-VirtualHub</span></span>
<span data-ttu-id="260b6-134">{{Fill VirtualHub Description}}</span><span class="sxs-lookup"><span data-stu-id="260b6-134">{{ Fill VirtualHub Description }}</span></span>

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

### <span data-ttu-id="260b6-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="260b6-135">-Confirm</span></span>
<span data-ttu-id="260b6-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="260b6-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="260b6-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="260b6-137">-WhatIf</span></span>
<span data-ttu-id="260b6-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="260b6-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="260b6-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="260b6-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="260b6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="260b6-140">CommonParameters</span></span>
<span data-ttu-id="260b6-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="260b6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="260b6-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="260b6-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="260b6-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="260b6-143">INPUTS</span></span>

### <span data-ttu-id="260b6-144">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="260b6-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="260b6-145">Microsoft. Azure. Commands. Network. Models. PSVirtualHubRouteTable</span><span class="sxs-lookup"><span data-stu-id="260b6-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHubRouteTable</span></span>

### <span data-ttu-id="260b6-146">System. String</span><span class="sxs-lookup"><span data-stu-id="260b6-146">System.String</span></span>

## <span data-ttu-id="260b6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="260b6-147">OUTPUTS</span></span>

### <span data-ttu-id="260b6-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="260b6-148">System.Boolean</span></span>

## <span data-ttu-id="260b6-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="260b6-149">NOTES</span></span>

## <span data-ttu-id="260b6-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="260b6-150">RELATED LINKS</span></span>
