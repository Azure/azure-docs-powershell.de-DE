---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzTenantDeployment.md
ms.openlocfilehash: 6c79d4b8d853d629a3b8e0422efb6a86eee18e34
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996411"
---
# <span data-ttu-id="51cb5-101">Stop-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="51cb5-101">Stop-AzTenantDeployment</span></span>

## <span data-ttu-id="51cb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="51cb5-102">SYNOPSIS</span></span>
<span data-ttu-id="51cb5-103">Abbrechen einer ausgeführten Bereitstellung im MANDANTENBEREICH</span><span class="sxs-lookup"><span data-stu-id="51cb5-103">Cancel a running deployment at tenant scope</span></span>

## <span data-ttu-id="51cb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="51cb5-104">SYNTAX</span></span>

### <span data-ttu-id="51cb5-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="51cb5-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzTenantDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51cb5-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="51cb5-106">StopByDeploymentId</span></span>
```
Stop-AzTenantDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51cb5-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="51cb5-107">StopByInputObject</span></span>
```
Stop-AzTenantDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51cb5-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="51cb5-108">DESCRIPTION</span></span>
<span data-ttu-id="51cb5-109">Das Cmdlet " **Stop-AzTenantDeployment** " bricht eine Bereitstellung ab, die im aktuellen MANDANTENBEREICH gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51cb5-109">The **Stop-AzTenantDeployment** cmdlet cancels a deployment that has started but not completed at the current tenant scope.</span></span>
<span data-ttu-id="51cb5-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="51cb5-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="51cb5-111">Verwenden Sie das New-AzTenantDeployment-Cmdlet, um eine Bereitstellung im MANDANTENBEREICH zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="51cb5-111">To create a deployment at tenant scope, use the New-AzTenantDeployment cmdlet.</span></span>

## <span data-ttu-id="51cb5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51cb5-112">EXAMPLES</span></span>

### <span data-ttu-id="51cb5-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="51cb5-113">Example 1</span></span>
```
PS C:\>Stop-AzTenantDeployment -Name "deployment01"
```

<span data-ttu-id="51cb5-114">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" im aktuellen MANDANTENBEREICH abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51cb5-114">This command cancels a running deployment "deployment01" at the current tenant scope.</span></span>

### <span data-ttu-id="51cb5-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="51cb5-115">Example 2</span></span>
```
PS C:\>Get-AzTenantDeployment -Name "deployment01" | Stop-AzTenantDeployment
```

<span data-ttu-id="51cb5-116">Mit diesem Befehl wird die Bereitstellung "deployment01" im aktuellen MANDANTENBEREICH abgerufen und abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="51cb5-116">This command gets the deployment "deployment01" at the current tenant scope and cancels it.</span></span> 

## <span data-ttu-id="51cb5-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb5-117">PARAMETERS</span></span>

### <span data-ttu-id="51cb5-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="51cb5-118">-ApiVersion</span></span>
<span data-ttu-id="51cb5-119">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51cb5-119">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="51cb5-120">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="51cb5-120">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51cb5-121">-DefaultProfile</span></span>
<span data-ttu-id="51cb5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="51cb5-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-123">-ID</span><span class="sxs-lookup"><span data-stu-id="51cb5-123">-Id</span></span>
<span data-ttu-id="51cb5-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="51cb5-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="51cb5-125">Beispiel:/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="51cb5-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="51cb5-126">-InputObject</span></span>
<span data-ttu-id="51cb5-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="51cb5-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: StopByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-128">-Name</span><span class="sxs-lookup"><span data-stu-id="51cb5-128">-Name</span></span>
<span data-ttu-id="51cb5-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="51cb5-129">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: StopByDeploymentName
Aliases: DeploymentName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51cb5-130">-PassThru</span></span>
<span data-ttu-id="51cb5-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="51cb5-131">{{ Fill PassThru Description }}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="51cb5-132">-Pre</span></span>
<span data-ttu-id="51cb5-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="51cb5-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="51cb5-134">-Confirm</span></span>
<span data-ttu-id="51cb5-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="51cb5-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51cb5-136">-WhatIf</span></span>
<span data-ttu-id="51cb5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51cb5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51cb5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51cb5-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51cb5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51cb5-139">CommonParameters</span></span>
<span data-ttu-id="51cb5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51cb5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51cb5-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51cb5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51cb5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="51cb5-142">INPUTS</span></span>

### <span data-ttu-id="51cb5-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="51cb5-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="51cb5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="51cb5-144">OUTPUTS</span></span>

### <span data-ttu-id="51cb5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="51cb5-145">System.Boolean</span></span>

## <span data-ttu-id="51cb5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="51cb5-146">NOTES</span></span>

## <span data-ttu-id="51cb5-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="51cb5-147">RELATED LINKS</span></span>
