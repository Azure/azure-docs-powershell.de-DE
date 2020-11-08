---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3DD193E-B8FE-468D-BEE7-00C3D99B469E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzResourceGroupDeployment.md
ms.openlocfilehash: c504a839b47fc36863e207f74d9b309309a31fbb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165646"
---
# <span data-ttu-id="4d75e-101">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d75e-101">Remove-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4d75e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d75e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d75e-103">Entfernt eine Ressourcengruppen Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4d75e-103">Removes a resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4d75e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d75e-104">SYNTAX</span></span>

### <span data-ttu-id="4d75e-105">RemoveByResourceGroupName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d75e-105">RemoveByResourceGroupName (Default)</span></span>
```
Remove-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d75e-106">RemoveByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4d75e-106">RemoveByResourceGroupDeploymentId</span></span>
```
Remove-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d75e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d75e-107">DESCRIPTION</span></span>

<span data-ttu-id="4d75e-108">Das Cmdlet **Remove-AzResourceGroupDeployment** entfernt eine Azure Resource Group-Bereitstellung und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="4d75e-108">The **Remove-AzResourceGroupDeployment** cmdlet removes an Azure resource group deployment and any associated operations.</span></span>

## <span data-ttu-id="4d75e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d75e-109">EXAMPLES</span></span>

### <span data-ttu-id="4d75e-110">Beispiel 1: Entfernen einer Ressourcengruppen Bereitstellung mit der Ressourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4d75e-110">Example 1: Removes a resource group deployment with ResourceId</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceId /subscriptions/{subId}/resourceGroups/testGroup/providers/Microsoft.Resources/deployments/testDeployment1

True
```

<span data-ttu-id="4d75e-111">Dieser Befehl entfernt eine Ressourcengruppen Bereitstellung mit der vollqualifizierten Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="4d75e-111">This command removes a resource group deployment with the fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="4d75e-112">Erfolgreiche Entfernung gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="4d75e-112">Successful removal returns true.</span></span>

### <span data-ttu-id="4d75e-113">Beispiel 2: entfernt eine Ressourcengruppen Bereitstellung mit ResourceGroupName und resourceName</span><span class="sxs-lookup"><span data-stu-id="4d75e-113">Example 2: Removes a resource group deployment with ResourceGroupName and ResourceName</span></span>

```powershell
PS C:\>Remove-AzResourceGroupDeployment -ResourceGroupName testGroup -Name testDeployment1

True
```

<span data-ttu-id="4d75e-114">Mit diesem Befehl wird eine Ressourcengruppen Bereitstellung mit dem bereitgestellten ResourceGroupName und resourceName entfernt.</span><span class="sxs-lookup"><span data-stu-id="4d75e-114">This command removes a resource group deployment with the provided ResourceGroupName and ResourceName.</span></span>
<span data-ttu-id="4d75e-115">Erfolgreiche Entfernung gibt true zurück.</span><span class="sxs-lookup"><span data-stu-id="4d75e-115">Successful removal returns true.</span></span>

## <span data-ttu-id="4d75e-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d75e-116">PARAMETERS</span></span>

### <span data-ttu-id="4d75e-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4d75e-117">-ApiVersion</span></span>
<span data-ttu-id="4d75e-118">Gibt die API-Version an, die vom Ressourcenanbieter unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="4d75e-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4d75e-119">Sie können eine andere Version als die Standard Version angeben.</span><span class="sxs-lookup"><span data-stu-id="4d75e-119">You can specify a different version than the default version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d75e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d75e-120">-DefaultProfile</span></span>
<span data-ttu-id="4d75e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="4d75e-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d75e-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4d75e-122">-Id</span></span>
<span data-ttu-id="4d75e-123">Gibt die ID der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="4d75e-123">Specifies the ID of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4d75e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4d75e-124">-Name</span></span>
<span data-ttu-id="4d75e-125">Gibt den Namen der zu entfernenden Ressourcengruppen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="4d75e-125">Specifies the name of the resource group deployment to remove.</span></span>

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

### <span data-ttu-id="4d75e-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="4d75e-126">-Pre</span></span>
<span data-ttu-id="4d75e-127">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4d75e-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4d75e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d75e-128">-ResourceGroupName</span></span>
<span data-ttu-id="4d75e-129">Gibt den Namen der zu entfernenden Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="4d75e-129">Specifies the name of the resource group to remove.</span></span>

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

### <span data-ttu-id="4d75e-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d75e-130">-Confirm</span></span>
<span data-ttu-id="4d75e-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d75e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d75e-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d75e-132">-WhatIf</span></span>
<span data-ttu-id="4d75e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d75e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d75e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d75e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d75e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d75e-135">CommonParameters</span></span>
<span data-ttu-id="4d75e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d75e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d75e-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d75e-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d75e-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d75e-138">INPUTS</span></span>

### <span data-ttu-id="4d75e-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4d75e-139">System.String</span></span>

## <span data-ttu-id="4d75e-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d75e-140">OUTPUTS</span></span>

### <span data-ttu-id="4d75e-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4d75e-141">System.Boolean</span></span>

## <span data-ttu-id="4d75e-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d75e-142">NOTES</span></span>

## <span data-ttu-id="4d75e-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d75e-143">RELATED LINKS</span></span>

[<span data-ttu-id="4d75e-144">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d75e-144">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4d75e-145">Neu – AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d75e-145">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4d75e-146">Stopp-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d75e-146">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="4d75e-147">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4d75e-147">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


