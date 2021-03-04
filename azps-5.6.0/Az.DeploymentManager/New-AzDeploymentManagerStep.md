---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 08cde5aed74b194ede03f695eaf071d18467cb1d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923680"
---
# <span data-ttu-id="f4f8f-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f4f8f-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f4f8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4f8f-102">SYNOPSIS</span></span>
<span data-ttu-id="f4f8f-103">Erstellt einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-103">Creates a step.</span></span>

## <span data-ttu-id="f4f8f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f4f8f-104">SYNTAX</span></span>

### <span data-ttu-id="f4f8f-105">Warten (Standard)</span><span class="sxs-lookup"><span data-stu-id="f4f8f-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4f8f-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="f4f8f-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4f8f-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="f4f8f-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4f8f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4f8f-108">DESCRIPTION</span></span>
<span data-ttu-id="f4f8f-109">Das **Cmdlet New-AzDeploymentManagerStep** erstellt einen Bereitstellungsschritt, auf den in Rollouts verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f4f8f-110">Geben Sie *die Eigenschaften Name*, *ResourceGroupName* und erforderliche Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f4f8f-111">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen auf den Schritt anwenden, indem Sie das cmdlet Set-AzDeploymentManagerStep verwenden.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f4f8f-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f4f8f-112">EXAMPLES</span></span>

### <span data-ttu-id="f4f8f-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f4f8f-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f4f8f-114">Erstellt einen Schritt in der ContosoResourceGroup mit dem Namen ContosoService1WaitStep mit Central US als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f4f8f-115">Mit der Eigenschaft Dauer wird die Dauer des Rollouts vor dem Ausführen des nächsten Schritts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f4f8f-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f4f8f-116">PARAMETERS</span></span>

### <span data-ttu-id="f4f8f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4f8f-117">-DefaultProfile</span></span>
<span data-ttu-id="f4f8f-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4f8f-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="f4f8f-119">-Duration</span></span>
<span data-ttu-id="f4f8f-120">Die Wartezeit im ISO 8601-Format.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f4f8f-121">Beispiel: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f4f8f-121">E.g.: PT30M, PT1H</span></span>

```yaml
Type: System.String
Parameter Sets: Wait
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="f4f8f-122">-HealthCheckProperties</span></span>
<span data-ttu-id="f4f8f-123">Die Eigenschaften der Integritätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-123">The health check properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSHealthCheckStepProperties
Parameter Sets: HealthCheckObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="f4f8f-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="f4f8f-125">Der Pfad zu der Datei, in der Integritätsprüfungseigenschaften definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-125">The path to the file where health check properties are defined.</span></span>

```yaml
Type: System.String
Parameter Sets: HealthCheckFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f4f8f-126">-Location</span></span>
<span data-ttu-id="f4f8f-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-127">The location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f4f8f-128">-Name</span></span>
<span data-ttu-id="f4f8f-129">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-129">The name of the step.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4f8f-130">-ResourceGroupName</span></span>
<span data-ttu-id="f4f8f-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="f4f8f-132">-Tag</span></span>
<span data-ttu-id="f4f8f-133">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4f8f-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f4f8f-134">-Confirm</span></span>
<span data-ttu-id="f4f8f-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4f8f-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4f8f-136">-WhatIf</span></span>
<span data-ttu-id="f4f8f-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4f8f-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4f8f-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4f8f-139">CommonParameters</span></span>
<span data-ttu-id="f4f8f-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4f8f-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4f8f-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f4f8f-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4f8f-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f4f8f-142">INPUTS</span></span>

### <span data-ttu-id="f4f8f-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f4f8f-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f4f8f-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f4f8f-144">OUTPUTS</span></span>

### <span data-ttu-id="f4f8f-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f4f8f-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f4f8f-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f4f8f-146">NOTES</span></span>

## <span data-ttu-id="f4f8f-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f4f8f-147">RELATED LINKS</span></span>
