---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: 3f2b09e047a4a7e39efe6f0f1724776f14a90d2a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459227"
---
# <span data-ttu-id="73175-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="73175-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="73175-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73175-102">SYNOPSIS</span></span>
<span data-ttu-id="73175-103">Entfernt eine Bereitstellung und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="73175-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="73175-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="73175-104">SYNTAX</span></span>

### <span data-ttu-id="73175-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="73175-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73175-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="73175-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="73175-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="73175-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73175-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="73175-108">DESCRIPTION</span></span>
<span data-ttu-id="73175-109">Das **Cmdlet "Remove-AzDeployment"** entfernt eine Azure-Bereitstellung im Abonnementbereich und alle zugehörigen Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="73175-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="73175-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="73175-110">EXAMPLES</span></span>

### <span data-ttu-id="73175-111">Beispiel 1: Entfernen einer Bereitstellung mit einem bestimmten Namen</span><span class="sxs-lookup"><span data-stu-id="73175-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="73175-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Abonnementbereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="73175-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="73175-113">Beispiel 2: Erhalten und Entfernen einer Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="73175-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="73175-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnementbereich ab und entfernt sie.</span><span class="sxs-lookup"><span data-stu-id="73175-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="73175-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="73175-115">PARAMETERS</span></span>

### <span data-ttu-id="73175-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="73175-116">-AsJob</span></span>
<span data-ttu-id="73175-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="73175-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="73175-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73175-118">-DefaultProfile</span></span>
<span data-ttu-id="73175-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73175-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="73175-120">-ID</span><span class="sxs-lookup"><span data-stu-id="73175-120">-Id</span></span>
<span data-ttu-id="73175-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="73175-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="73175-122">beispiel: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="73175-122">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73175-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="73175-123">-InputObject</span></span>
<span data-ttu-id="73175-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="73175-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73175-125">-Name</span><span class="sxs-lookup"><span data-stu-id="73175-125">-Name</span></span>
<span data-ttu-id="73175-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="73175-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73175-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="73175-127">-PassThru</span></span>
<span data-ttu-id="73175-128">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="73175-128">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="73175-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="73175-129">-Pre</span></span>
<span data-ttu-id="73175-130">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="73175-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="73175-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="73175-131">-Confirm</span></span>
<span data-ttu-id="73175-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73175-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73175-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="73175-133">-WhatIf</span></span>
<span data-ttu-id="73175-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73175-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="73175-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73175-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73175-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73175-136">CommonParameters</span></span>
<span data-ttu-id="73175-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73175-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73175-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="73175-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73175-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="73175-139">INPUTS</span></span>

### <span data-ttu-id="73175-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="73175-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="73175-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="73175-141">OUTPUTS</span></span>

### <span data-ttu-id="73175-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="73175-142">System.Boolean</span></span>

## <span data-ttu-id="73175-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="73175-143">NOTES</span></span>

## <span data-ttu-id="73175-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="73175-144">RELATED LINKS</span></span>
