---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/stop-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Stop-AzureRmDeployment.md
ms.openlocfilehash: d8f54706ed37412f6b1081311d90d032b57d2a16
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664500"
---
# <span data-ttu-id="c3485-101">Stop-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="c3485-101">Stop-AzureRmDeployment</span></span>

## <span data-ttu-id="c3485-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c3485-102">SYNOPSIS</span></span>
<span data-ttu-id="c3485-103">Cancal einer ausgeführten Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="c3485-103">Cancal a running deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3485-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3485-104">SYNTAX</span></span>

### <span data-ttu-id="c3485-105">StopByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3485-105">StopByDeploymentName (Default)</span></span>
```
Stop-AzureRmDeployment [-Name] <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3485-106">StopByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="c3485-106">StopByDeploymentId</span></span>
```
Stop-AzureRmDeployment -Id <String> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3485-107">StopByInputObject</span><span class="sxs-lookup"><span data-stu-id="c3485-107">StopByInputObject</span></span>
```
Stop-AzureRmDeployment -InputObject <PSDeployment> [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3485-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3485-108">DESCRIPTION</span></span>
<span data-ttu-id="c3485-109">Das Cmdlet " **Stop-AzureRmDeployment** " bricht eine Bereitstellung im Abonnement Bereich ab, die gestartet, aber nicht abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="c3485-109">The **Stop-AzureRmDeployment** cmdlet cancels a deployment at subscription scope that has started but not completed.</span></span>
<span data-ttu-id="c3485-110">Damit eine Bereitstellung beendet werden kann, muss die Bereitstellung einen unvollständigen Bereitstellungsstatus aufweisen, beispielsweise die Bereitstellung und nicht den Status abgeschlossen, wie bereitgestellt oder fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="c3485-110">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>

<span data-ttu-id="c3485-111">Verwenden Sie das New-AzureRmDeployment-Cmdlet, um eine Bereitstellung im Abonnement Bereich zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3485-111">To create a deployment at subscription scope, use the New-AzureRmDeployment cmdlet.</span></span>

<span data-ttu-id="c3485-112">Dieses Cmdlet beendet nur eine ausgeführte Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3485-112">This cmdlet stops only one running deployment.</span></span> <span data-ttu-id="c3485-113">Verwenden Sie den Parameter *Name* , um eine bestimmte Bereitstellung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="c3485-113">Use the *Name* parameter to stop a specific deployment.</span></span>

## <span data-ttu-id="c3485-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c3485-114">EXAMPLES</span></span>

### <span data-ttu-id="c3485-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3485-115">Example 1</span></span>
```
PS C:\>Stop-AzureRmDeployment -Name "deployment01"
```

<span data-ttu-id="c3485-116">Mit diesem Befehl wird eine ausgeführte Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c3485-116">This command cancels a running deployment "deployment01" at the current subscription scope.</span></span>

### <span data-ttu-id="c3485-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c3485-117">Example 2</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "deployment01" | Stop-AzureRmDeployment
```

<span data-ttu-id="c3485-118">Mit diesem Befehl wird die Bereitstellung "deployment01" im aktuellen Abonnement Bereich abgerufen und abgebrochen.</span><span class="sxs-lookup"><span data-stu-id="c3485-118">This command gets the deployment "deployment01" at the current subscription scope and cancels it.</span></span> 

## <span data-ttu-id="c3485-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c3485-119">PARAMETERS</span></span>

### <span data-ttu-id="c3485-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="c3485-120">-ApiVersion</span></span>
<span data-ttu-id="c3485-121">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3485-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="c3485-122">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c3485-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="c3485-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3485-123">-DefaultProfile</span></span>
<span data-ttu-id="c3485-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c3485-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3485-125">-ID</span><span class="sxs-lookup"><span data-stu-id="c3485-125">-Id</span></span>
<span data-ttu-id="c3485-126">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3485-126">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="c3485-127">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="c3485-127">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="c3485-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3485-128">-InputObject</span></span>
<span data-ttu-id="c3485-129">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="c3485-129">The deployment object.</span></span>

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

### <span data-ttu-id="c3485-130">-Name</span><span class="sxs-lookup"><span data-stu-id="c3485-130">-Name</span></span>
<span data-ttu-id="c3485-131">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="c3485-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="c3485-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3485-132">-PassThru</span></span>
<span data-ttu-id="c3485-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c3485-133">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c3485-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="c3485-134">-Pre</span></span>
<span data-ttu-id="c3485-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c3485-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="c3485-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c3485-136">-Confirm</span></span>
<span data-ttu-id="c3485-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3485-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3485-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3485-138">-WhatIf</span></span>
<span data-ttu-id="c3485-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3485-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3485-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3485-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3485-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3485-141">CommonParameters</span></span>
<span data-ttu-id="c3485-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3485-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3485-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3485-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3485-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c3485-144">INPUTS</span></span>

### <span data-ttu-id="c3485-145">System. String</span><span class="sxs-lookup"><span data-stu-id="c3485-145">System.String</span></span>

## <span data-ttu-id="c3485-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c3485-146">OUTPUTS</span></span>

### <span data-ttu-id="c3485-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c3485-147">System.Boolean</span></span>

## <span data-ttu-id="c3485-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c3485-148">NOTES</span></span>

## <span data-ttu-id="c3485-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c3485-149">RELATED LINKS</span></span>
