---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzManagementGroupDeployment.md
ms.openlocfilehash: 96c4f9147875198716d530ee065177472233e465
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177234"
---
# <span data-ttu-id="82cf1-101">Stop-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="82cf1-101">Stop-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="82cf1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="82cf1-102">SYNOPSIS</span></span>
<span data-ttu-id="82cf1-103">Abbrechen einer ausgeführten Bereitstellung in einer Verwaltungsgruppe</span><span class="sxs-lookup"><span data-stu-id="82cf1-103">Cancel a running deployment at a management group</span></span>

## <span data-ttu-id="82cf1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="82cf1-104">SYNTAX</span></span>

### <span data-ttu-id="82cf1-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="82cf1-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf1-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="82cf1-106">StopByDeploymentId</span></span>
```
Stop-AzManagementGroupDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="82cf1-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="82cf1-107">StopByInputObject</span></span>
```
Stop-AzManagementGroupDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82cf1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="82cf1-108">DESCRIPTION</span></span>
<span data-ttu-id="82cf1-109">Das Cmdlet " **Stop-AzManagementGroupDeployment** " bricht eine Bereitstellung ab, die in einer Verwaltungsgruppe gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="82cf1-109">The **Stop-AzManagementGroupDeployment** cmdlet cancels a deployment that has started but not completed at a management group.</span></span>
<span data-ttu-id="82cf1-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="82cf1-111">Verwenden Sie das New-AzManagementGroupDeployment-Cmdlet, um eine Bereitstellung in einer Verwaltungsgruppe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-111">To create a deployment at a management group, use the New-AzManagementGroupDeployment cmdlet.</span></span>

## <span data-ttu-id="82cf1-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="82cf1-112">EXAMPLES</span></span>

### <span data-ttu-id="82cf1-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="82cf1-113">Example 1</span></span>
```
PS C:\>Stop-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01"
```

<span data-ttu-id="82cf1-114">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" in der Verwaltungsgruppe "myMG" abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-114">This command cancels a running deployment "deployment01" at the management group "myMG".</span></span>

### <span data-ttu-id="82cf1-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="82cf1-115">Example 2</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "deployment01" | Stop-AzManagementGroupDeployment
```

<span data-ttu-id="82cf1-116">Dieser Befehl ruft die Bereitstellung "deployment01" in der Verwaltungsgruppe "myMG" ab und bricht Sie ab.</span><span class="sxs-lookup"><span data-stu-id="82cf1-116">This command gets the deployment "deployment01" at the management group "myMG" and cancels it.</span></span> 

## <span data-ttu-id="82cf1-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="82cf1-117">PARAMETERS</span></span>

### <span data-ttu-id="82cf1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82cf1-118">-DefaultProfile</span></span>
<span data-ttu-id="82cf1-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="82cf1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82cf1-120">-ID</span><span class="sxs-lookup"><span data-stu-id="82cf1-120">-Id</span></span>
<span data-ttu-id="82cf1-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="82cf1-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="82cf1-122">Beispiel:/Providers/Microsoft.Management/managementGroups/{managementGroupId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="82cf1-122">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="82cf1-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="82cf1-123">-InputObject</span></span>
<span data-ttu-id="82cf1-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="82cf1-124">The deployment object.</span></span>

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

### <span data-ttu-id="82cf1-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="82cf1-125">-ManagementGroupId</span></span>
<span data-ttu-id="82cf1-126">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="82cf1-126">The management group id.</span></span>

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

### <span data-ttu-id="82cf1-127">-Name</span><span class="sxs-lookup"><span data-stu-id="82cf1-127">-Name</span></span>
<span data-ttu-id="82cf1-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="82cf1-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="82cf1-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82cf1-129">-PassThru</span></span>
<span data-ttu-id="82cf1-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="82cf1-130">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="82cf1-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="82cf1-131">-Pre</span></span>
<span data-ttu-id="82cf1-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="82cf1-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="82cf1-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="82cf1-133">-Confirm</span></span>
<span data-ttu-id="82cf1-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="82cf1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82cf1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82cf1-135">-WhatIf</span></span>
<span data-ttu-id="82cf1-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="82cf1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82cf1-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82cf1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82cf1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82cf1-138">CommonParameters</span></span>
<span data-ttu-id="82cf1-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82cf1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82cf1-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="82cf1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82cf1-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="82cf1-141">INPUTS</span></span>

### <span data-ttu-id="82cf1-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="82cf1-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="82cf1-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="82cf1-143">OUTPUTS</span></span>

### <span data-ttu-id="82cf1-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="82cf1-144">System.Boolean</span></span>

## <span data-ttu-id="82cf1-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="82cf1-145">NOTES</span></span>

## <span data-ttu-id="82cf1-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="82cf1-146">RELATED LINKS</span></span>
