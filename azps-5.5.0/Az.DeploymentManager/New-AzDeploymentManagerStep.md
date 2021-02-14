---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174553"
---
# <span data-ttu-id="f7566-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="f7566-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="f7566-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7566-102">SYNOPSIS</span></span>
<span data-ttu-id="f7566-103">Erstellt einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="f7566-103">Creates a step.</span></span>

## <span data-ttu-id="f7566-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f7566-104">SYNTAX</span></span>

### <span data-ttu-id="f7566-105">Warten (Standard)</span><span class="sxs-lookup"><span data-stu-id="f7566-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7566-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="f7566-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7566-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="f7566-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7566-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f7566-108">DESCRIPTION</span></span>
<span data-ttu-id="f7566-109">Das **Cmdlet "New-AzDeploymentManagerStep"** erstellt einen Bereitstellungsschritt, auf den in Rollouts verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f7566-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="f7566-110">Geben Sie *"Name",* *"ResourceGroupName"* und die erforderlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="f7566-110">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="f7566-111">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen mithilfe des cmdlets Set-AzDeploymentManagerStep auf den Schritt anwenden.</span><span class="sxs-lookup"><span data-stu-id="f7566-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="f7566-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f7566-112">EXAMPLES</span></span>

### <span data-ttu-id="f7566-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f7566-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="f7566-114">Erstellt einen Schritt in der ContosoResourceGroup mit dem Namen "ContosoService1WaitStep" und "USA, Mitte" als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f7566-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="f7566-115">Die Eigenschaft "Duration" stellt die Dauer für die Ausführung des Rollouts vor dem Ausführen des nächsten Schritts zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f7566-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="f7566-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f7566-116">PARAMETERS</span></span>

### <span data-ttu-id="f7566-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7566-117">-DefaultProfile</span></span>
<span data-ttu-id="f7566-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f7566-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7566-119">-Duration</span><span class="sxs-lookup"><span data-stu-id="f7566-119">-Duration</span></span>
<span data-ttu-id="f7566-120">Die Wartezeit im ISO 8601-Format.</span><span class="sxs-lookup"><span data-stu-id="f7566-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="f7566-121">Beispiel: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="f7566-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="f7566-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="f7566-122">-HealthCheckProperties</span></span>
<span data-ttu-id="f7566-123">Die Eigenschaften der Integritätsprüfung.</span><span class="sxs-lookup"><span data-stu-id="f7566-123">The health check properties.</span></span>

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

### <span data-ttu-id="f7566-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="f7566-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="f7566-125">Der Pfad zu der Datei, in der Eigenschaften der Integritätsprüfung definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f7566-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="f7566-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f7566-126">-Location</span></span>
<span data-ttu-id="f7566-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f7566-127">The location of the resource.</span></span>

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

### <span data-ttu-id="f7566-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f7566-128">-Name</span></span>
<span data-ttu-id="f7566-129">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="f7566-129">The name of the step.</span></span>

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

### <span data-ttu-id="f7566-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7566-130">-ResourceGroupName</span></span>
<span data-ttu-id="f7566-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f7566-131">The resource group.</span></span>

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

### <span data-ttu-id="f7566-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7566-132">-Tag</span></span>
<span data-ttu-id="f7566-133">Eine Hashtabelle, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="f7566-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="f7566-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f7566-134">-Confirm</span></span>
<span data-ttu-id="f7566-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7566-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7566-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f7566-136">-WhatIf</span></span>
<span data-ttu-id="f7566-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7566-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7566-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7566-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7566-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7566-139">CommonParameters</span></span>
<span data-ttu-id="f7566-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7566-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7566-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f7566-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7566-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f7566-142">INPUTS</span></span>

### <span data-ttu-id="f7566-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7566-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7566-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f7566-144">OUTPUTS</span></span>

### <span data-ttu-id="f7566-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span><span class="sxs-lookup"><span data-stu-id="f7566-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="f7566-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f7566-146">NOTES</span></span>

## <span data-ttu-id="f7566-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f7566-147">RELATED LINKS</span></span>
