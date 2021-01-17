---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459188"
---
# <span data-ttu-id="f7eaf-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="f7eaf-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="f7eaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7eaf-102">SYNOPSIS</span></span>
<span data-ttu-id="f7eaf-103">Abbrechen einer laufenden Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="f7eaf-103">Cancel a running deployment</span></span>

## <span data-ttu-id="f7eaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7eaf-104">SYNTAX</span></span>

### <span data-ttu-id="f7eaf-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7eaf-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7eaf-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="f7eaf-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7eaf-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7eaf-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7eaf-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7eaf-108">DESCRIPTION</span></span>
<span data-ttu-id="f7eaf-109">Das **Cmdlet "Stop-AzDeployment"** bricht eine Bereitstellung im Abonnementbereich ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="f7eaf-110">Um eine Bereitstellung zu beenden, muss die Bereitstellung einen unvollständigen Bereitstellungszustand haben, z. B. "Provisioning", und keinen abgeschlossenen Zustand, z. B. "Provisioned" oder "Failed".</span><span class="sxs-lookup"><span data-stu-id="f7eaf-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="f7eaf-111">Um eine Bereitstellung im Abonnementbereich zu erstellen, verwenden Sie das New-AzDeployment Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="f7eaf-112">Dieses Cmdlet stoppt nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="f7eaf-113">Verwenden Sie den *Parameter "Name",* um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="f7eaf-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7eaf-114">EXAMPLES</span></span>

### <span data-ttu-id="f7eaf-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7eaf-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="f7eaf-116">Dieser Befehl bricht eine laufende Bereitstellung "deployment01" im aktuellen Abonnementbereich ab.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="f7eaf-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f7eaf-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="f7eaf-118">Dieser Befehl ruft die Bereitstellung "deployment01" im aktuellen Abonnementbereich ab und bricht sie ab.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="f7eaf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7eaf-119">PARAMETERS</span></span>

### <span data-ttu-id="f7eaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7eaf-120">-DefaultProfile</span></span>
<span data-ttu-id="f7eaf-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7eaf-122">-ID</span><span class="sxs-lookup"><span data-stu-id="f7eaf-122">-Id</span></span>
<span data-ttu-id="f7eaf-123">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="f7eaf-124">beispiel: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="f7eaf-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="f7eaf-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7eaf-125">-InputObject</span></span>
<span data-ttu-id="f7eaf-126">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-126">The deployment object.</span></span>

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

### <span data-ttu-id="f7eaf-127">-Name</span><span class="sxs-lookup"><span data-stu-id="f7eaf-127">-Name</span></span>
<span data-ttu-id="f7eaf-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="f7eaf-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f7eaf-129">-PassThru</span></span>
<span data-ttu-id="f7eaf-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f7eaf-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f7eaf-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="f7eaf-131">-Pre</span></span>
<span data-ttu-id="f7eaf-132">Gibt bei Festlegung an, dass das Cmdlet Vorabversions-API-Versionen verwenden sollte, wenn automatisch ermittelt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f7eaf-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7eaf-133">-Confirm</span></span>
<span data-ttu-id="f7eaf-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7eaf-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7eaf-135">-WhatIf</span></span>
<span data-ttu-id="f7eaf-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7eaf-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7eaf-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7eaf-138">CommonParameters</span></span>
<span data-ttu-id="f7eaf-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7eaf-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7eaf-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7eaf-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7eaf-141">INPUTS</span></span>

### <span data-ttu-id="f7eaf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f7eaf-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f7eaf-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7eaf-143">OUTPUTS</span></span>

### <span data-ttu-id="f7eaf-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f7eaf-144">System.Boolean</span></span>

## <span data-ttu-id="f7eaf-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7eaf-145">NOTES</span></span>

## <span data-ttu-id="f7eaf-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7eaf-146">RELATED LINKS</span></span>
