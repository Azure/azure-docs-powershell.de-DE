---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: bda1d2e79e7ef67e69d7b425761750a95c2f3777
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177232"
---
# <span data-ttu-id="fc260-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="fc260-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="fc260-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fc260-102">SYNOPSIS</span></span>
<span data-ttu-id="fc260-103">Abbrechen einer ausgeführten Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="fc260-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="fc260-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc260-104">SYNTAX</span></span>

### <span data-ttu-id="fc260-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fc260-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc260-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="fc260-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc260-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="fc260-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc260-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fc260-108">DESCRIPTION</span></span>
<span data-ttu-id="fc260-109">Das Cmdlet " **Stop-AzTenantDeployment** " bricht eine Bereitstellung ab, die im aktuellen MANDANTENBEREICH gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="fc260-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="fc260-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="fc260-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="fc260-111">Verwenden Sie das New-AzTenantDeployment-Cmdlet, um eine Bereitstellung im MANDANTENBEREICH zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fc260-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="fc260-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fc260-112">EXAMPLES</span></span>

### <span data-ttu-id="fc260-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fc260-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="fc260-114">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" im aktuellen MANDANTENBEREICH abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fc260-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="fc260-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fc260-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="fc260-116">Mit diesem Befehl wird die Bereitstellung "deployment01" im aktuellen MANDANTENBEREICH abgerufen und abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="fc260-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="fc260-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc260-117">PARAMETERS</span></span>

### <span data-ttu-id="fc260-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc260-118">-DefaultProfile</span></span>
<span data-ttu-id="fc260-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fc260-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc260-120">-ID</span><span class="sxs-lookup"><span data-stu-id="fc260-120">-Id</span></span>
<span data-ttu-id="fc260-121">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fc260-121">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="fc260-122">Beispiel:/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="fc260-122">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="fc260-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc260-123">-InputObject</span></span>
<span data-ttu-id="fc260-124">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="fc260-124">The deployment object.</span></span>

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

### <span data-ttu-id="fc260-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fc260-125">-Name</span></span>
<span data-ttu-id="fc260-126">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="fc260-126">The name of the deployment.</span></span>

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

### <span data-ttu-id="fc260-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc260-127">-PassThru</span></span>
<span data-ttu-id="fc260-128">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="fc260-128">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="fc260-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="fc260-129">-Pre</span></span>
<span data-ttu-id="fc260-130">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="fc260-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="fc260-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fc260-131">-Confirm</span></span>
<span data-ttu-id="fc260-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc260-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc260-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc260-133">-WhatIf</span></span>
<span data-ttu-id="fc260-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fc260-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc260-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fc260-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc260-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc260-136">CommonParameters</span></span>
<span data-ttu-id="fc260-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc260-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc260-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc260-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc260-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fc260-139">INPUTS</span></span>

### <span data-ttu-id="fc260-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="fc260-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="fc260-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fc260-141">OUTPUTS</span></span>

### <span data-ttu-id="fc260-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc260-142">System.Boolean</span></span>

## <span data-ttu-id="fc260-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="fc260-143">NOTES</span></span>

## <span data-ttu-id="fc260-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fc260-144">RELATED LINKS</span></span>
