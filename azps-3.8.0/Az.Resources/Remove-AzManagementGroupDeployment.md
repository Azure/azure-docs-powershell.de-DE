---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996471"
---
# <span data-ttu-id="d9a57-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d9a57-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d9a57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d9a57-102">SYNOPSIS</span></span>
<span data-ttu-id="d9a57-103">Entfernt eine Bereitstellung in einer Verwaltungsgruppe und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="d9a57-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="d9a57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9a57-104">SYNTAX</span></span>

### <span data-ttu-id="d9a57-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d9a57-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9a57-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d9a57-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9a57-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="d9a57-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9a57-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d9a57-108">DESCRIPTION</span></span>
<span data-ttu-id="d9a57-109">Das Cmdlet **Remove-AzManagementGroupDeployment** entfernt eine Azure-Bereitstellung in einer Verwaltungsgruppe und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d9a57-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="d9a57-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d9a57-110">EXAMPLES</span></span>

### <span data-ttu-id="d9a57-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="d9a57-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="d9a57-112">Dieser Befehl entfernt die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG".</span><span class="sxs-lookup"><span data-stu-id="d9a57-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="d9a57-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="d9a57-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="d9a57-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG" ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="d9a57-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="d9a57-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9a57-115">PARAMETERS</span></span>

### <span data-ttu-id="d9a57-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d9a57-116">-ApiVersion</span></span>
<span data-ttu-id="d9a57-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9a57-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d9a57-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d9a57-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d9a57-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d9a57-119">-AsJob</span></span>
<span data-ttu-id="d9a57-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d9a57-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d9a57-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9a57-121">-DefaultProfile</span></span>
<span data-ttu-id="d9a57-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d9a57-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9a57-123">-ID</span><span class="sxs-lookup"><span data-stu-id="d9a57-123">-Id</span></span>
<span data-ttu-id="d9a57-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d9a57-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d9a57-125">Beispiel:/Providers/Microsoft.Management/managementGroups/{managementGroupId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d9a57-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a57-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d9a57-126">-InputObject</span></span>
<span data-ttu-id="d9a57-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d9a57-127">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d9a57-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d9a57-128">-ManagementGroupId</span></span>
<span data-ttu-id="d9a57-129">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="d9a57-129">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a57-130">-Name</span><span class="sxs-lookup"><span data-stu-id="d9a57-130">-Name</span></span>
<span data-ttu-id="d9a57-131">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="d9a57-131">The name of the deployment.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9a57-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d9a57-132">-PassThru</span></span>
<span data-ttu-id="d9a57-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="d9a57-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="d9a57-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="d9a57-134">-Pre</span></span>
<span data-ttu-id="d9a57-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a57-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d9a57-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d9a57-136">-Confirm</span></span>
<span data-ttu-id="d9a57-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d9a57-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9a57-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9a57-138">-WhatIf</span></span>
<span data-ttu-id="d9a57-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9a57-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9a57-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d9a57-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9a57-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9a57-141">CommonParameters</span></span>
<span data-ttu-id="d9a57-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9a57-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9a57-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d9a57-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9a57-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d9a57-144">INPUTS</span></span>

### <span data-ttu-id="d9a57-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d9a57-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d9a57-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d9a57-146">OUTPUTS</span></span>

### <span data-ttu-id="d9a57-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9a57-147">System.Boolean</span></span>

## <span data-ttu-id="d9a57-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d9a57-148">NOTES</span></span>

## <span data-ttu-id="d9a57-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d9a57-149">RELATED LINKS</span></span>
