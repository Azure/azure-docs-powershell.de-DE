---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98306920"
---
# <span data-ttu-id="4ccdf-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ccdf-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4ccdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ccdf-102">SYNOPSIS</span></span>
<span data-ttu-id="4ccdf-103">Entfernt eine Ressourcengruppenbereitstellung und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4ccdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ccdf-104">SYNTAX</span></span>

### <span data-ttu-id="4ccdf-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ccdf-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4ccdf-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ccdf-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ccdf-107">DESCRIPTION</span></span>

<span data-ttu-id="4ccdf-108">Das **Cmdlet "Remove-AzResourceGroupDeployment"** entfernt eine Bereitstellung einer Azure-Ressourcengruppe und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4ccdf-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ccdf-109">EXAMPLES</span></span>

### <span data-ttu-id="4ccdf-110">Beispiel 1: Entfernt eine Ressourcengruppenbereitstellung mit "ResourceId".</span><span class="sxs-lookup"><span data-stu-id="4ccdf-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="4ccdf-111">Mit diesem Befehl wird eine Ressourcengruppenbereitstellung mit der vollqualifizierten Ressourcen-ID der Bereitstellung entfernt.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4ccdf-112">Das erfolgreiche Entfernen gibt "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-112">Successful removal returns true.</span></span>

### <span data-ttu-id="4ccdf-113">Beispiel 2: Entfernt eine Ressourcengruppenbereitstellung mit "ResourceGroupName" und "ResourceName".</span><span class="sxs-lookup"><span data-stu-id="4ccdf-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="4ccdf-114">Mit diesem Befehl wird eine Ressourcengruppenbereitstellung mit den bereitgestellten Ressourcengruppennamen und Ressourcennamen entfernt.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="4ccdf-115">Das erfolgreiche Entfernen gibt "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-115">Successful removal returns true.</span></span>

## <span data-ttu-id="4ccdf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ccdf-116">PARAMETERS</span></span>

### <span data-ttu-id="4ccdf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ccdf-117">-DefaultProfile</span></span>
<span data-ttu-id="4ccdf-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4ccdf-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4ccdf-119">-ID</span><span class="sxs-lookup"><span data-stu-id="4ccdf-119">-Id</span></span>
<span data-ttu-id="4ccdf-120">Gibt die ID der zu entfernenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4ccdf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4ccdf-121">-Name</span></span>
<span data-ttu-id="4ccdf-122">Gibt den Namen der zu entfernenden Ressourcengruppenbereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4ccdf-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="4ccdf-123">-Pre</span></span>
<span data-ttu-id="4ccdf-124">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4ccdf-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ccdf-125">-ResourceGroupName</span></span>
<span data-ttu-id="4ccdf-126">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="4ccdf-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4ccdf-127">-Confirm</span></span>
<span data-ttu-id="4ccdf-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ccdf-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4ccdf-129">-WhatIf</span></span>
<span data-ttu-id="4ccdf-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ccdf-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ccdf-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ccdf-132">CommonParameters</span></span>
<span data-ttu-id="4ccdf-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ccdf-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ccdf-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4ccdf-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ccdf-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ccdf-135">INPUTS</span></span>

### <span data-ttu-id="4ccdf-136">System.String</span><span class="sxs-lookup"><span data-stu-id="4ccdf-136">System.String</span></span>

## <span data-ttu-id="4ccdf-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ccdf-137">OUTPUTS</span></span>

### <span data-ttu-id="4ccdf-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4ccdf-138">System.Boolean</span></span>

## <span data-ttu-id="4ccdf-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ccdf-139">NOTES</span></span>

## <span data-ttu-id="4ccdf-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ccdf-140">RELATED LINKS</span></span>

[<span data-ttu-id="4ccdf-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ccdf-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4ccdf-142">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ccdf-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4ccdf-143">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ccdf-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4ccdf-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4ccdf-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


