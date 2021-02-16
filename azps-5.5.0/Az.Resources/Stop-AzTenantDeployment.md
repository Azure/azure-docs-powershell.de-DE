---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100145980"
---
# <span data-ttu-id="85e19-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="85e19-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="85e19-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85e19-102">SYNOPSIS</span></span>
<span data-ttu-id="85e19-103">Abbrechen einer ausgeführten Bereitstellung im Mandantenbereich</span><span class="sxs-lookup"><span data-stu-id="85e19-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="85e19-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85e19-104">SYNTAX</span></span>

### <span data-ttu-id="85e19-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85e19-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e19-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="85e19-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85e19-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="85e19-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85e19-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85e19-108">DESCRIPTION</span></span>
<span data-ttu-id="85e19-109">Das **Cmdlet "Stop-AzTenantDeployment"** bricht eine Bereitstellung ab, die im aktuellen Mandantenbereich gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="85e19-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="85e19-110">Um eine Bereitstellung zu beenden, muss die Bereitstellung einen unvollständigen Bereitstellungszustand haben, z. B. "Provisioning", und keinen abgeschlossenen Zustand, z. B. "Provisioned" oder "Failed".</span><span class="sxs-lookup"><span data-stu-id="85e19-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="85e19-111">Um eine Bereitstellung im Mandantenbereich zu erstellen, verwenden Sie das New-AzTenantDeployment-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="85e19-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="85e19-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85e19-112">EXAMPLES</span></span>

### <span data-ttu-id="85e19-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85e19-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="85e19-114">Dieser Befehl bricht eine laufende Bereitstellung "deployment01" im aktuellen Mandantenbereich ab.</span><span class="sxs-lookup"><span data-stu-id="85e19-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="85e19-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="85e19-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="85e19-116">Dieser Befehl ruft die Bereitstellung "deployment01" im aktuellen Mandantenbereich ab und bricht ihn ab.</span><span class="sxs-lookup"><span data-stu-id="85e19-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="85e19-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85e19-117">PARAMETERS</span></span>

### <span data-ttu-id="85e19-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85e19-118">-DefaultProfile</span></span>
<span data-ttu-id="85e19-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85e19-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85e19-120">-ID</span><span class="sxs-lookup"><span data-stu-id="85e19-120">-Id</span></span>
<span data-ttu-id="85e19-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="85e19-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="85e19-122">Beispiel: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="85e19-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e19-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85e19-123">-InputObject</span></span>
<span data-ttu-id="85e19-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="85e19-124">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85e19-125">-Name</span><span class="sxs-lookup"><span data-stu-id="85e19-125">-Name</span></span>
<span data-ttu-id="85e19-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="85e19-126">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85e19-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85e19-127">-PassThru</span></span>
<span data-ttu-id="85e19-128">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="85e19-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="85e19-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="85e19-129">-Pre</span></span>
<span data-ttu-id="85e19-130">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="85e19-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="85e19-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85e19-131">-Confirm</span></span>
<span data-ttu-id="85e19-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85e19-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85e19-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85e19-133">-WhatIf</span></span>
<span data-ttu-id="85e19-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85e19-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85e19-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85e19-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85e19-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85e19-136">CommonParameters</span></span>
<span data-ttu-id="85e19-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85e19-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85e19-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85e19-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85e19-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85e19-139">INPUTS</span></span>

### <span data-ttu-id="85e19-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="85e19-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="85e19-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85e19-141">OUTPUTS</span></span>

### <span data-ttu-id="85e19-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="85e19-142">System.Boolean</span></span>

## <span data-ttu-id="85e19-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85e19-143">NOTES</span></span>

## <span data-ttu-id="85e19-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85e19-144">RELATED LINKS</span></span>
