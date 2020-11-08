---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzDeployment.md
ms.openlocfilehash: fd3fc9b254fab2044ad955d7b4aeb43783d5a907
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177240"
---
# <span data-ttu-id="c6de4-101">Stop-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="c6de4-101">Stop-AzDeployment</span></span>

## <span data-ttu-id="c6de4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c6de4-102">SYNOPSIS</span></span>
<span data-ttu-id="c6de4-103">Abbrechen einer ausgeführten Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c6de4-103">Cancel a running deployment</span></span>

## <span data-ttu-id="c6de4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6de4-104">SYNTAX</span></span>

### <span data-ttu-id="c6de4-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c6de4-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6de4-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c6de4-106">StopByDeploymentId</span></span>
```
Stop-AzDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c6de4-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c6de4-107">StopByInputObject</span></span>
```
Stop-AzDeployment -InputObject <PSDeployment> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6de4-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c6de4-108">DESCRIPTION</span></span>
<span data-ttu-id="c6de4-109">Das Cmdlet " **Stop-AzDeployment** " bricht eine Bereitstellung im Abonnement Bereich ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c6de4-109">The **Stop-AzDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="c6de4-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c6de4-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="c6de4-111">Verwenden Sie das New-AzDeployment-Cmdlet, um eine Bereitstellung im Abonnement Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c6de4-111">To create a deployment at subscription scope, use the New-AzDeployment cmdlet.</span></span>

<span data-ttu-id="c6de4-112">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c6de4-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="c6de4-113">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c6de4-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="c6de4-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c6de4-114">EXAMPLES</span></span>

### <span data-ttu-id="c6de4-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c6de4-115">Example 1</span></span>
```
PS C:\>Stop-AzDeployment -Name "deployment01"
```

<span data-ttu-id="c6de4-116">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c6de4-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="c6de4-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c6de4-117">Example 2</span></span>
```
PS C:\>Get-AzDeployment -Name "deployment01" | Stop-AzDeployment
```

<span data-ttu-id="c6de4-118">Mit diesem Befehl wird die Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgerufen und abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c6de4-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="c6de4-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6de4-119">PARAMETERS</span></span>

### <span data-ttu-id="c6de4-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6de4-120">-DefaultProfile</span></span>
<span data-ttu-id="c6de4-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c6de4-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6de4-122">-ID</span><span class="sxs-lookup"><span data-stu-id="c6de4-122">-Id</span></span>
<span data-ttu-id="c6de4-123">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c6de4-123">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c6de4-124">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c6de4-124">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c6de4-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6de4-125">-InputObject</span></span>
<span data-ttu-id="c6de4-126">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c6de4-126">The deployment object.</span></span>

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

### <span data-ttu-id="c6de4-127">-Name</span><span class="sxs-lookup"><span data-stu-id="c6de4-127">-Name</span></span>
<span data-ttu-id="c6de4-128">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c6de4-128">The name of the deployment.</span></span>

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

### <span data-ttu-id="c6de4-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6de4-129">-PassThru</span></span>
<span data-ttu-id="c6de4-130">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c6de4-130">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c6de4-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="c6de4-131">-Pre</span></span>
<span data-ttu-id="c6de4-132">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c6de4-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c6de4-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c6de4-133">-Confirm</span></span>
<span data-ttu-id="c6de4-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c6de4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6de4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6de4-135">-WhatIf</span></span>
<span data-ttu-id="c6de4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c6de4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6de4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c6de4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6de4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6de4-138">CommonParameters</span></span>
<span data-ttu-id="c6de4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6de4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6de4-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c6de4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6de4-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c6de4-141">INPUTS</span></span>

### <span data-ttu-id="c6de4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="c6de4-142">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="c6de4-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c6de4-143">OUTPUTS</span></span>

### <span data-ttu-id="c6de4-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c6de4-144">System.Boolean</span></span>

## <span data-ttu-id="c6de4-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="c6de4-145">NOTES</span></span>

## <span data-ttu-id="c6de4-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c6de4-146">RELATED LINKS</span></span>
