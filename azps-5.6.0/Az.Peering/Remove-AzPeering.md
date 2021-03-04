---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/powershell/module/az.peering/remove-azpeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Remove-AzPeering.md
ms.openlocfilehash: ba6817928751c67e87f6641a6362a1fbf84eece8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937627"
---
# <span data-ttu-id="6c2d0-101">Remove-AzPeering</span><span class="sxs-lookup"><span data-stu-id="6c2d0-101">Remove-AzPeering</span></span>

## <span data-ttu-id="6c2d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c2d0-102">SYNOPSIS</span></span>
<span data-ttu-id="6c2d0-103">Löschen oder Entfernen eines Peerings</span><span class="sxs-lookup"><span data-stu-id="6c2d0-103">Delete or remove a peering.</span></span> <span data-ttu-id="6c2d0-104">Dadurch werden alle untergeordneten Ressourcen oder Benachrichtigungen für die Ressource gelöscht.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-104">This will delete all child resources or alerting on the resource.</span></span>

## <span data-ttu-id="6c2d0-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6c2d0-105">SYNTAX</span></span>

### <span data-ttu-id="6c2d0-106">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6c2d0-106">ByName (Default)</span></span>
```
Remove-AzPeering [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c2d0-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="6c2d0-107">InputObject</span></span>
```
Remove-AzPeering [-InputObject] <PSPeering> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6c2d0-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2d0-108">ByResourceId</span></span>
```
Remove-AzPeering -ResourceId <String> [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6c2d0-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c2d0-109">DESCRIPTION</span></span>
<span data-ttu-id="6c2d0-110">Löschen Sie eine Peeringressource.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-110">Perminently delete a peering resource.</span></span>

## <span data-ttu-id="6c2d0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6c2d0-111">EXAMPLES</span></span>

### <span data-ttu-id="6c2d0-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c2d0-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzPeering -ResourceId $resourceId
```

<span data-ttu-id="6c2d0-113">Entfernen Sie ein Peering nach Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-113">Remove a peering by resource id.</span></span>

## <span data-ttu-id="6c2d0-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6c2d0-114">PARAMETERS</span></span>

### <span data-ttu-id="6c2d0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6c2d0-115">-AsJob</span></span>
<span data-ttu-id="6c2d0-116">Führen Sie im Hintergrund aus.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-116">Run in the background.</span></span>

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

### <span data-ttu-id="6c2d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c2d0-117">-DefaultProfile</span></span>
<span data-ttu-id="6c2d0-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c2d0-119">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="6c2d0-119">-Force</span></span>
<span data-ttu-id="6c2d0-120">Erzwingen des Vorgangs</span><span class="sxs-lookup"><span data-stu-id="6c2d0-120">Force the operation to complete</span></span>

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

### <span data-ttu-id="6c2d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6c2d0-121">-InputObject</span></span>
<span data-ttu-id="6c2d0-122">Verwenden Get-AzPeering, um dieses Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-122">Use Get-AzPeering to retrieve this object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2d0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6c2d0-123">-Name</span></span>
<span data-ttu-id="6c2d0-124">Der eindeutige Name des PSPeerings.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-124">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2d0-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6c2d0-125">-PassThru</span></span>
<span data-ttu-id="6c2d0-126">"True" zurückgeben, wenn dies abgeschlossen ist</span><span class="sxs-lookup"><span data-stu-id="6c2d0-126">Return true if complete</span></span>

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

### <span data-ttu-id="6c2d0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c2d0-127">-ResourceGroupName</span></span>
<span data-ttu-id="6c2d0-128">Erstellen oder Verwenden eines vorhandenen Ressourcengruppennamens.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-128">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c2d0-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6c2d0-129">-ResourceId</span></span>
<span data-ttu-id="6c2d0-130">Der Zeichenfolgenname der Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-130">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c2d0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6c2d0-131">-Confirm</span></span>
<span data-ttu-id="6c2d0-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6c2d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6c2d0-133">-WhatIf</span></span>
<span data-ttu-id="6c2d0-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6c2d0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6c2d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c2d0-136">CommonParameters</span></span>
<span data-ttu-id="6c2d0-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c2d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c2d0-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6c2d0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c2d0-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6c2d0-139">INPUTS</span></span>

### <span data-ttu-id="6c2d0-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span><span class="sxs-lookup"><span data-stu-id="6c2d0-140">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeering</span></span>

### <span data-ttu-id="6c2d0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="6c2d0-141">System.String</span></span>

## <span data-ttu-id="6c2d0-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6c2d0-142">OUTPUTS</span></span>

### <span data-ttu-id="6c2d0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6c2d0-143">System.Boolean</span></span>

## <span data-ttu-id="6c2d0-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6c2d0-144">NOTES</span></span>

## <span data-ttu-id="6c2d0-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6c2d0-145">RELATED LINKS</span></span>
