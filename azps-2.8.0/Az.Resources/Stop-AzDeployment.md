---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: b08f5e929ec6c3f297bc5373c5f7b82ed3b73f14
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824903"
---
# <span data-ttu-id="c1417-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c1417-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="c1417-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c1417-102">SYNOPSIS</span></span>
<span data-ttu-id="c1417-103">Abbrechen einer ausgeführten Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c1417-103">Cancel a running deployment</span></span>

## <span data-ttu-id="c1417-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1417-104">SYNTAX</span></span>

### <span data-ttu-id="c1417-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c1417-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1417-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c1417-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1417-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1417-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c1417-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c1417-108">DESCRIPTION</span></span>
<span data-ttu-id="c1417-109">Das Cmdlet " **Stop-AzDeployment** " bricht eine Bereitstellung im Abonnement Bereich ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c1417-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="c1417-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c1417-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="c1417-111">Verwenden Sie das New-AzDeployment-Cmdlet, um eine Bereitstellung im Abonnement Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c1417-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="c1417-112">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c1417-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="c1417-113">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c1417-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="c1417-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c1417-114">EXAMPLES</span></span>

### <span data-ttu-id="c1417-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c1417-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="c1417-116">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c1417-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="c1417-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c1417-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="c1417-118">Mit diesem Befehl wird die Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgerufen und abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c1417-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="c1417-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1417-119">PARAMETERS</span></span>

### <span data-ttu-id="c1417-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c1417-120">-ApiVersion</span></span>
<span data-ttu-id="c1417-121">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c1417-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c1417-122">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c1417-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c1417-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1417-123">-DefaultProfile</span></span>
<span data-ttu-id="c1417-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c1417-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1417-125">-ID</span><span class="sxs-lookup"><span data-stu-id="c1417-125">-Id</span></span>
<span data-ttu-id="c1417-126">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c1417-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c1417-127">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c1417-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c1417-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c1417-128">-InputObject</span></span>
<span data-ttu-id="c1417-129">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c1417-129">The deployment object.</span></span>

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

### <span data-ttu-id="c1417-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c1417-130">-Name</span></span>
<span data-ttu-id="c1417-131">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c1417-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="c1417-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c1417-132">-PassThru</span></span>
<span data-ttu-id="c1417-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c1417-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c1417-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c1417-134">-Pre</span></span>
<span data-ttu-id="c1417-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c1417-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c1417-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c1417-136">-Confirm</span></span>
<span data-ttu-id="c1417-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1417-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1417-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1417-138">-WhatIf</span></span>
<span data-ttu-id="c1417-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1417-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1417-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1417-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1417-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1417-141">CommonParameters</span></span>
<span data-ttu-id="c1417-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1417-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1417-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1417-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1417-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c1417-144">INPUTS</span></span>

### <span data-ttu-id="c1417-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c1417-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c1417-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c1417-146">OUTPUTS</span></span>

### <span data-ttu-id="c1417-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c1417-147">System.Boolean</span></span>

## <span data-ttu-id="c1417-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c1417-148">NOTES</span></span>

## <span data-ttu-id="c1417-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c1417-149">RELATED LINKS</span></span>
