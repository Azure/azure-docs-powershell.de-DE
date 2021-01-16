---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385285"
---
# <span data-ttu-id="a21e8-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a21e8-101">Remove-AzBastion</span></span>

## <span data-ttu-id="a21e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a21e8-102">SYNOPSIS</span></span>
<span data-ttu-id="a21e8-103">Entfernt eine Ressource aus der Quelle" aus.</span><span class="sxs-lookup"><span data-stu-id="a21e8-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="a21e8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a21e8-104">SYNTAX</span></span>

### <span data-ttu-id="a21e8-105">ByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a21e8-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a21e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a21e8-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a21e8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a21e8-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a21e8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a21e8-108">DESCRIPTION</span></span>
<span data-ttu-id="a21e8-109">Entfernt eine Ressource aus der Quelle" aus. In "Beispiel1" wird die Gruppe mit "ResourceGroupName" und "ResourceName" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a21e8-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="a21e8-110">In Beispiel2 wird die Ben mit ihrem Objekt und der Pipeline gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a21e8-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="a21e8-111">In Beispiel3 wird die Ben mit ihrem Objekt gelöscht.</span><span class="sxs-lookup"><span data-stu-id="a21e8-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="a21e8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a21e8-112">EXAMPLES</span></span>

### <span data-ttu-id="a21e8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a21e8-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="a21e8-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a21e8-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="a21e8-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a21e8-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="a21e8-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a21e8-116">PARAMETERS</span></span>

### <span data-ttu-id="a21e8-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a21e8-117">-Confirm</span></span>
<span data-ttu-id="a21e8-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a21e8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a21e8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a21e8-119">-DefaultProfile</span></span>
<span data-ttu-id="a21e8-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a21e8-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a21e8-121">-Force</span><span class="sxs-lookup"><span data-stu-id="a21e8-121">-Force</span></span>
<span data-ttu-id="a21e8-122">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="a21e8-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a21e8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a21e8-123">-InputObject</span></span>
<span data-ttu-id="a21e8-124">Das zu löschende Objekt "Weiter".</span><span class="sxs-lookup"><span data-stu-id="a21e8-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a21e8-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a21e8-125">-Name</span></span>
<span data-ttu-id="a21e8-126">Der zu löschende Ressourcenname der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a21e8-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21e8-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a21e8-127">-PassThru</span></span>
<span data-ttu-id="a21e8-128">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a21e8-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="a21e8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a21e8-129">-ResourceGroupName</span></span>
<span data-ttu-id="a21e8-130">Der Ressourcengruppenname, in dem "ort" vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a21e8-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a21e8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a21e8-131">-ResourceId</span></span>
<span data-ttu-id="a21e8-132">Die Azure-Ressourcen-ID für das zu löschende Hotel.</span><span class="sxs-lookup"><span data-stu-id="a21e8-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a21e8-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="a21e8-133">-WhatIf</span></span>
<span data-ttu-id="a21e8-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a21e8-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a21e8-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a21e8-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a21e8-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a21e8-136">CommonParameters</span></span>
<span data-ttu-id="a21e8-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a21e8-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a21e8-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a21e8-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a21e8-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a21e8-139">INPUTS</span></span>

### <span data-ttu-id="a21e8-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="a21e8-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="a21e8-141">System.String</span><span class="sxs-lookup"><span data-stu-id="a21e8-141">System.String</span></span>

## <span data-ttu-id="a21e8-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a21e8-142">OUTPUTS</span></span>

### <span data-ttu-id="a21e8-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a21e8-143">System.Boolean</span></span>

## <span data-ttu-id="a21e8-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a21e8-144">NOTES</span></span>

## <span data-ttu-id="a21e8-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a21e8-145">RELATED LINKS</span></span>
[<span data-ttu-id="a21e8-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a21e8-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="a21e8-147">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="a21e8-147">New-AzBastion</span></span>](./New-AzBastion.md)