---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: f1bb3530c31305e5f70c80d7b520286da9878480
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180035"
---
# <span data-ttu-id="6f6d8-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f6d8-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6f6d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f6d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6f6d8-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="6f6d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f6d8-104">SYNTAX</span></span>

### <span data-ttu-id="6f6d8-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="6f6d8-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6f6d8-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6f6d8-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f6d8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f6d8-107">DESCRIPTION</span></span>

<span data-ttu-id="6f6d8-108">Das Cmdlet **Remove-AzResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="6f6d8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f6d8-109">EXAMPLES</span></span>

### <span data-ttu-id="6f6d8-110">Beispiel 1: Entfernen einer Ressourcengruppen Bereitstellung mit der Ressourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6f6d8-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="6f6d8-111">Dieser Befehl entfernt eine Ressourcengruppen Bereitstellung mit der vollqualifizierten Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="6f6d8-112">Erfolgreiche Entfernung gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-112">Successful removal returns true.</span></span>

### <span data-ttu-id="6f6d8-113">Beispiel 2: entfernt eine Ressourcengruppen Bereitstellung mit ResourceGroupName und resourceName</span><span class="sxs-lookup"><span data-stu-id="6f6d8-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="6f6d8-114">Mit diesem Befehl wird eine Ressourcengruppen Bereitstellung mit dem bereitgestellten ResourceGroupName und resourceName entfernt.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="6f6d8-115">Erfolgreiche Entfernung gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-115">Successful removal returns true.</span></span>

## <span data-ttu-id="6f6d8-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f6d8-116">PARAMETERS</span></span>

### <span data-ttu-id="6f6d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f6d8-117">-DefaultProfile</span></span>
<span data-ttu-id="6f6d8-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6f6d8-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6f6d8-119">-ID</span><span class="sxs-lookup"><span data-stu-id="6f6d8-119">-Id</span></span>
<span data-ttu-id="6f6d8-120">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-120">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="6f6d8-121">-Name</span><span class="sxs-lookup"><span data-stu-id="6f6d8-121">-Name</span></span>
<span data-ttu-id="6f6d8-122">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-122">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="6f6d8-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="6f6d8-123">-Pre</span></span>
<span data-ttu-id="6f6d8-124">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-124">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6f6d8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6f6d8-125">-ResourceGroupName</span></span>
<span data-ttu-id="6f6d8-126">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-126">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="6f6d8-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f6d8-127">-Confirm</span></span>
<span data-ttu-id="6f6d8-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f6d8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f6d8-129">-WhatIf</span></span>
<span data-ttu-id="6f6d8-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6f6d8-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f6d8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f6d8-132">CommonParameters</span></span>
<span data-ttu-id="6f6d8-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f6d8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f6d8-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6f6d8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f6d8-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f6d8-135">INPUTS</span></span>

### <span data-ttu-id="6f6d8-136">System. String</span><span class="sxs-lookup"><span data-stu-id="6f6d8-136">System.String</span></span>

## <span data-ttu-id="6f6d8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f6d8-137">OUTPUTS</span></span>

### <span data-ttu-id="6f6d8-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6f6d8-138">System.Boolean</span></span>

## <span data-ttu-id="6f6d8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f6d8-139">NOTES</span></span>

## <span data-ttu-id="6f6d8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f6d8-140">RELATED LINKS</span></span>

[<span data-ttu-id="6f6d8-141">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f6d8-141">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f6d8-142">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f6d8-142">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f6d8-143">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f6d8-143">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="6f6d8-144">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6f6d8-144">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


