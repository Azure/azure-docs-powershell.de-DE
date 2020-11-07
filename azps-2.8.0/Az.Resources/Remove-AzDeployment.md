---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeployment.md
ms.openlocfilehash: dbc5238819c6dc7a7555dd1f95ec0ba3478f2b2b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823427"
---
# <span data-ttu-id="3d453-101">Remove-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="3d453-101">Remove-AzDeployment</span></span>

## <span data-ttu-id="3d453-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d453-102">SYNOPSIS</span></span>
<span data-ttu-id="3d453-103">Entfernt eine Bereitstellung und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="3d453-103">Removes a deployment and any associated operations</span></span>

## <span data-ttu-id="3d453-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d453-104">SYNTAX</span></span>

### <span data-ttu-id="3d453-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3d453-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzDeployment [-Name] <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d453-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="3d453-106">RemoveByDeploymentId</span></span>
```
Remove-AzDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3d453-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="3d453-107">RemoveByInputObject</span></span>
```
Remove-AzDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d453-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d453-108">DESCRIPTION</span></span>
<span data-ttu-id="3d453-109">Das Cmdlet **Remove-AzDeployment** entfernt eine Azure-Bereitstellung im Abonnement Bereich und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="3d453-109">The **Remove-AzDeployment** cmdlet removes an Azure deployment at subscription scope and any associated operations.</span></span>

## <span data-ttu-id="3d453-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d453-110">EXAMPLES</span></span>

### <span data-ttu-id="3d453-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="3d453-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzDeployment -Name "RolesDeployment"
```

<span data-ttu-id="3d453-112">Mit diesem Befehl wird die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich entfernt.</span><span class="sxs-lookup"><span data-stu-id="3d453-112">This command removes the deployment "RolesDeployment" at the current subscription scope.</span></span>

### <span data-ttu-id="3d453-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="3d453-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzDeployment -Name "RolesDeployment" | Remove-AzDeployment
```

<span data-ttu-id="3d453-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" im aktuellen Abonnement Bereich ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="3d453-114">This command gets the deployment "RolesDeployment" at the current subscription scope and removes it.</span></span>

## <span data-ttu-id="3d453-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d453-115">PARAMETERS</span></span>

### <span data-ttu-id="3d453-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3d453-116">-ApiVersion</span></span>
<span data-ttu-id="3d453-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3d453-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="3d453-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3d453-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="3d453-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d453-119">-AsJob</span></span>
<span data-ttu-id="3d453-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="3d453-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d453-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d453-121">-DefaultProfile</span></span>
<span data-ttu-id="3d453-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d453-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d453-123">-ID</span><span class="sxs-lookup"><span data-stu-id="3d453-123">-Id</span></span>
<span data-ttu-id="3d453-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="3d453-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="3d453-125">Beispiel:/Subscriptions/{subId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="3d453-125">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="3d453-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3d453-126">-InputObject</span></span>
<span data-ttu-id="3d453-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3d453-127">The deployment object.</span></span>

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

### <span data-ttu-id="3d453-128">-Name</span><span class="sxs-lookup"><span data-stu-id="3d453-128">-Name</span></span>
<span data-ttu-id="3d453-129">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="3d453-129">The name of the deployment.</span></span>

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

### <span data-ttu-id="3d453-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3d453-130">-PassThru</span></span>
<span data-ttu-id="3d453-131">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="3d453-131">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="3d453-132">-Pre</span><span class="sxs-lookup"><span data-stu-id="3d453-132">-Pre</span></span>
<span data-ttu-id="3d453-133">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="3d453-133">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="3d453-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3d453-134">-Confirm</span></span>
<span data-ttu-id="3d453-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3d453-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d453-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d453-136">-WhatIf</span></span>
<span data-ttu-id="3d453-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3d453-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d453-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3d453-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d453-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d453-139">CommonParameters</span></span>
<span data-ttu-id="3d453-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d453-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d453-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d453-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d453-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d453-142">INPUTS</span></span>

### <span data-ttu-id="3d453-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="3d453-143">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="3d453-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d453-144">OUTPUTS</span></span>

### <span data-ttu-id="3d453-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3d453-145">System.Boolean</span></span>

## <span data-ttu-id="3d453-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d453-146">NOTES</span></span>

## <span data-ttu-id="3d453-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d453-147">RELATED LINKS</span></span>
