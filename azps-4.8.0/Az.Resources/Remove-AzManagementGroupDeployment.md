---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzManagementGroupDeployment.md
ms.openlocfilehash: f9348090c3dd397573d6ef9d36fcad2aee3b55aa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007856"
---
# <span data-ttu-id="621bf-101">Remove-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="621bf-101">Remove-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="621bf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="621bf-102">SYNOPSIS</span></span>
<span data-ttu-id="621bf-103">Entfernt eine Bereitstellung in einer Verwaltungsgruppe und alle zugeordneten Vorgänge</span><span class="sxs-lookup"><span data-stu-id="621bf-103">Removes a deployment at a management group and any associated operations</span></span>

## <span data-ttu-id="621bf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="621bf-104">SYNTAX</span></span>

### <span data-ttu-id="621bf-105">RemoveByDeploymentName (Standard)</span><span class="sxs-lookup"><span data-stu-id="621bf-105">RemoveByDeploymentName (Default)</span></span>
```
Remove-AzManagementGroupDeployment [-ManagementGroupId] <String> [-Name] <String> [-AsJob] [-PassThru]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="621bf-106">RemoveByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="621bf-106">RemoveByDeploymentId</span></span>
```
Remove-AzManagementGroupDeployment -Id <String> [-AsJob] [-PassThru] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="621bf-107">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="621bf-107">RemoveByInputObject</span></span>
```
Remove-AzManagementGroupDeployment -InputObject <PSDeployment> [-AsJob] [-PassThru] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="621bf-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="621bf-108">DESCRIPTION</span></span>
<span data-ttu-id="621bf-109">Das Cmdlet **Remove-AzManagementGroupDeployment** entfernt eine Azure-Bereitstellung in einer Verwaltungsgruppe und alle zugeordneten Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="621bf-109">The **Remove-AzManagementGroupDeployment** cmdlet removes an Azure deployment at a management group and any associated operations.</span></span>

## <span data-ttu-id="621bf-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="621bf-110">EXAMPLES</span></span>

### <span data-ttu-id="621bf-111">Beispiel 1: Entfernen einer Bereitstellung mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="621bf-111">Example 1: Remove a deployment with a given name</span></span>
```
PS C:\>Remove-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment"
```

<span data-ttu-id="621bf-112">Dieser Befehl entfernt die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG".</span><span class="sxs-lookup"><span data-stu-id="621bf-112">This command removes the deployment "RolesDeployment" at the management group "myMG".</span></span>

### <span data-ttu-id="621bf-113">Beispiel 2: Abrufen einer Bereitstellung und entfernen</span><span class="sxs-lookup"><span data-stu-id="621bf-113">Example 2: Get a deployment and remove it</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG" -Name "RolesDeployment" | Remove-AzManagementGroupDeployment
```

<span data-ttu-id="621bf-114">Dieser Befehl ruft die Bereitstellung "RolesDeployment" in der Verwaltungsgruppe "myMG" ab und entfernt Sie.</span><span class="sxs-lookup"><span data-stu-id="621bf-114">This command gets the deployment "RolesDeployment" at the management group "myMG" and removes it.</span></span>

## <span data-ttu-id="621bf-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="621bf-115">PARAMETERS</span></span>

### <span data-ttu-id="621bf-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="621bf-116">-ApiVersion</span></span>
<span data-ttu-id="621bf-117">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="621bf-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="621bf-118">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="621bf-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="621bf-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="621bf-119">-AsJob</span></span>
<span data-ttu-id="621bf-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="621bf-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="621bf-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="621bf-121">-DefaultProfile</span></span>
<span data-ttu-id="621bf-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="621bf-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="621bf-123">-ID</span><span class="sxs-lookup"><span data-stu-id="621bf-123">-Id</span></span>
<span data-ttu-id="621bf-124">Die vollqualifizierte Ressourcen-ID der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="621bf-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="621bf-125">Beispiel:/Providers/Microsoft.Management/managementGroups/{managementGroupId}/Providers/Microsoft.Resources/Deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="621bf-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="621bf-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="621bf-126">-InputObject</span></span>
<span data-ttu-id="621bf-127">Das Bereitstellungsobjekt.</span><span class="sxs-lookup"><span data-stu-id="621bf-127">The deployment object.</span></span>

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

### <span data-ttu-id="621bf-128">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="621bf-128">-ManagementGroupId</span></span>
<span data-ttu-id="621bf-129">Die Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="621bf-129">The management group id.</span></span>

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

### <span data-ttu-id="621bf-130">-Name</span><span class="sxs-lookup"><span data-stu-id="621bf-130">-Name</span></span>
<span data-ttu-id="621bf-131">Der Name der Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="621bf-131">The name of the deployment.</span></span>

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

### <span data-ttu-id="621bf-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="621bf-132">-PassThru</span></span>
<span data-ttu-id="621bf-133">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="621bf-133">{{ Fill PassThru Description }}</span></span>

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

### <span data-ttu-id="621bf-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="621bf-134">-Pre</span></span>
<span data-ttu-id="621bf-135">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="621bf-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="621bf-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="621bf-136">-Confirm</span></span>
<span data-ttu-id="621bf-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="621bf-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="621bf-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="621bf-138">-WhatIf</span></span>
<span data-ttu-id="621bf-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="621bf-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="621bf-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="621bf-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="621bf-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="621bf-141">CommonParameters</span></span>
<span data-ttu-id="621bf-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="621bf-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="621bf-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="621bf-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="621bf-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="621bf-144">INPUTS</span></span>

### <span data-ttu-id="621bf-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="621bf-145">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="621bf-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="621bf-146">OUTPUTS</span></span>

### <span data-ttu-id="621bf-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="621bf-147">System.Boolean</span></span>

## <span data-ttu-id="621bf-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="621bf-148">NOTES</span></span>

## <span data-ttu-id="621bf-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="621bf-149">RELATED LINKS</span></span>
