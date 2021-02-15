---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174316"
---
# <span data-ttu-id="45ec6-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="45ec6-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="45ec6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45ec6-102">SYNOPSIS</span></span>
<span data-ttu-id="45ec6-103">Abbrechen einer laufenden Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="45ec6-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="45ec6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="45ec6-104">SYNTAX</span></span>

### <span data-ttu-id="45ec6-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="45ec6-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ec6-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="45ec6-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="45ec6-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="45ec6-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45ec6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="45ec6-108">DESCRIPTION</span></span>
<span data-ttu-id="45ec6-109">Das **Cmdlet "Stop-AzManagementGroupDeployment"** bricht eine Bereitstellung ab, die in einer Verwaltungsgruppe gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="45ec6-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="45ec6-110">Um eine Bereitstellung zu beenden, muss die Bereitstellung einen unvollständigen Bereitstellungszustand haben, z. B. "Provisioning", und keinen abgeschlossenen Zustand, z. B. "Provisioned" oder "Failed".</span><span class="sxs-lookup"><span data-stu-id="45ec6-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="45ec6-111">Verwenden Sie zum Erstellen einer Bereitstellung in einer Verwaltungsgruppe das New-AzManagementGroupDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45ec6-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="45ec6-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="45ec6-112">EXAMPLES</span></span>

### <span data-ttu-id="45ec6-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="45ec6-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="45ec6-114">Dieser Befehl bricht eine laufende Bereitstellung "deployment01" in der Verwaltungsgruppe "myMG" ab.</span><span class="sxs-lookup"><span data-stu-id="45ec6-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="45ec6-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="45ec6-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="45ec6-116">Dieser Befehl ruft die Bereitstellung "deployment01" bei der Verwaltungsgruppe "myMG" ab und bricht ihn ab.</span><span class="sxs-lookup"><span data-stu-id="45ec6-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="45ec6-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45ec6-117">PARAMETERS</span></span>

### <span data-ttu-id="45ec6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45ec6-118">-DefaultProfile</span></span>
<span data-ttu-id="45ec6-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="45ec6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45ec6-120">-ID</span><span class="sxs-lookup"><span data-stu-id="45ec6-120">-Id</span></span>
<span data-ttu-id="45ec6-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="45ec6-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="45ec6-122">beispiel: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="45ec6-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="45ec6-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45ec6-123">-InputObject</span></span>
<span data-ttu-id="45ec6-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="45ec6-124">The deployment object.</span></span>

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

### <span data-ttu-id="45ec6-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="45ec6-125">-ManagementGroupId</span></span>
<span data-ttu-id="45ec6-126">Die ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="45ec6-126">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ec6-127">-Name</span><span class="sxs-lookup"><span data-stu-id="45ec6-127">-Name</span></span>
<span data-ttu-id="45ec6-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="45ec6-128">The name of the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45ec6-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45ec6-129">-PassThru</span></span>
<span data-ttu-id="45ec6-130">{{ Fill PassThru Description }}</span><span class="sxs-lookup"><span data-stu-id="45ec6-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="45ec6-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="45ec6-131">-Pre</span></span>
<span data-ttu-id="45ec6-132">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="45ec6-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="45ec6-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="45ec6-133">-Confirm</span></span>
<span data-ttu-id="45ec6-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45ec6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45ec6-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="45ec6-135">-WhatIf</span></span>
<span data-ttu-id="45ec6-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45ec6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45ec6-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45ec6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45ec6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45ec6-138">CommonParameters</span></span>
<span data-ttu-id="45ec6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45ec6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45ec6-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="45ec6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45ec6-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="45ec6-141">INPUTS</span></span>

### <span data-ttu-id="45ec6-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="45ec6-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="45ec6-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="45ec6-143">OUTPUTS</span></span>

### <span data-ttu-id="45ec6-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="45ec6-144">System.Boolean</span></span>

## <span data-ttu-id="45ec6-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="45ec6-145">NOTES</span></span>

## <span data-ttu-id="45ec6-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="45ec6-146">RELATED LINKS</span></span>
