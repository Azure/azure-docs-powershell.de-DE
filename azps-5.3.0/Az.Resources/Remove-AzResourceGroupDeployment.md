---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98468548"
---
# <span data-ttu-id="3e6f3-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3e6f3-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="3e6f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3e6f3-102">SYNOPSIS</span></span>
<span data-ttu-id="3e6f3-103">Entfernt eine Ressourcengruppenbereitstellung und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="3e6f3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3e6f3-104">SYNTAX</span></span>

### <span data-ttu-id="3e6f3-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e6f3-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3e6f3-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3e6f3-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e6f3-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3e6f3-107">DESCRIPTION</span></span>

<span data-ttu-id="3e6f3-108">Das **Cmdlet "Remove-AzResourceGroupDeployment"** entfernt eine Bereitstellung einer Azure-Ressourcengruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="3e6f3-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3e6f3-109">EXAMPLES</span></span>

### <span data-ttu-id="3e6f3-110">Beispiel 1: Entfernt eine Ressourcengruppenbereitstellung mit "ResourceId".</span><span class="sxs-lookup"><span data-stu-id="3e6f3-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="3e6f3-111">Mit diesem Befehl wird eine Ressourcengruppenbereitstellung mit der vollqualifizierten Ressourcen-ID der Bereitstellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3e6f3-112">Beim erfolgreichen Entfernen wird "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-112">Successful removal returns true.</span></span>

### <span data-ttu-id="3e6f3-113">Beispiel 2: Entfernt eine Ressourcengruppenbereitstellung mit "ResourceGroupName" und "ResourceName".</span><span class="sxs-lookup"><span data-stu-id="3e6f3-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="3e6f3-114">Mit diesem Befehl wird eine Ressourcengruppenbereitstellung mit den bereitgestellten Ressourcengruppennamen und Ressourcennamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="3e6f3-115">Beim erfolgreichen Entfernen wird "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-115">Successful removal returns true.</span></span>

## <span data-ttu-id="3e6f3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3e6f3-116">PARAMETERS</span></span>

### <span data-ttu-id="3e6f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e6f3-117">-DefaultProfile</span></span>
<span data-ttu-id="3e6f3-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3e6f3-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3e6f3-119">-ID</span><span class="sxs-lookup"><span data-stu-id="3e6f3-119">-Id</span></span>
<span data-ttu-id="3e6f3-120">Gibt die ID der zu entfernenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-120">Specifies the ID of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3e6f3-121">-Name</span></span>
<span data-ttu-id="3e6f3-122">Gibt den Namen der zu entfernenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-122">Specifies the name of the resource group deployment to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f3-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="3e6f3-123">-Pre</span></span>
<span data-ttu-id="3e6f3-124">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3e6f3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e6f3-125">-ResourceGroupName</span></span>
<span data-ttu-id="3e6f3-126">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-126">Specifies the name of the resource group to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceGroupName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f3-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3e6f3-127">-Confirm</span></span>
<span data-ttu-id="3e6f3-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f3-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3e6f3-129">-WhatIf</span></span>
<span data-ttu-id="3e6f3-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e6f3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-131">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e6f3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e6f3-132">CommonParameters</span></span>
<span data-ttu-id="3e6f3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e6f3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e6f3-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3e6f3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e6f3-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3e6f3-135">INPUTS</span></span>

### <span data-ttu-id="3e6f3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3e6f3-136">System.String</span></span>

## <span data-ttu-id="3e6f3-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3e6f3-137">OUTPUTS</span></span>

### <span data-ttu-id="3e6f3-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="3e6f3-138">System.Boolean</span></span>

## <span data-ttu-id="3e6f3-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3e6f3-139">NOTES</span></span>

## <span data-ttu-id="3e6f3-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3e6f3-140">RELATED LINKS</span></span>

[<span data-ttu-id="3e6f3-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3e6f3-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="3e6f3-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3e6f3-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="3e6f3-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3e6f3-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="3e6f3-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="3e6f3-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


