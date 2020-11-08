---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerstep
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerStep.md
ms.openlocfilehash: 077cdeef04e9a7b0eeec80e6d6ce4c17717826ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008008"
---
# <span data-ttu-id="b4331-101">New-AzDeploymentManagerStep</span><span class="sxs-lookup"><span data-stu-id="b4331-101">New-AzDeploymentManagerStep</span></span>

## <span data-ttu-id="b4331-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b4331-102">SYNOPSIS</span></span>
<span data-ttu-id="b4331-103">Erstellt einen Schritt.</span><span class="sxs-lookup"><span data-stu-id="b4331-103">Creates a step.</span></span>

## <span data-ttu-id="b4331-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b4331-104">SYNTAX</span></span>

### <span data-ttu-id="b4331-105">Warten (Standard)</span><span class="sxs-lookup"><span data-stu-id="b4331-105">Wait (Default)</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String> -Duration <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4331-106">HealthCheckFile</span><span class="sxs-lookup"><span data-stu-id="b4331-106">HealthCheckFile</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckPropertiesFile <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4331-107">HealthCheckObject</span><span class="sxs-lookup"><span data-stu-id="b4331-107">HealthCheckObject</span></span>
```
New-AzDeploymentManagerStep -ResourceGroupName <String> -Name <String> -Location <String>
 -HealthCheckProperties <PSHealthCheckStepProperties> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4331-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b4331-108">DESCRIPTION</span></span>
<span data-ttu-id="b4331-109">Das Cmdlet **New-AzDeploymentManagerStep** erstellt einen Bereitstellungsschritt, auf den in Rollouts verwiesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="b4331-109">The **New-AzDeploymentManagerStep** cmdlet creates a deployment step that can be referenced in rollouts.</span></span>
<span data-ttu-id="b4331-110">Geben Sie den *Namen* , die *ResourceGroupName* und die erforderlichen Eigenschaften an.</span><span class="sxs-lookup"><span data-stu-id="b4331-110">Specify the *Name* , *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="b4331-111">Sie können das zurückgegebene Objekt lokal ändern und dann die Änderungen auf den Schritt mithilfe des Set-AzDeploymentManagerStep-Cmdlets anwenden.</span><span class="sxs-lookup"><span data-stu-id="b4331-111">You can modify the returned object locally and then apply the changes to the step by using the Set-AzDeploymentManagerStep cmdlet.</span></span>

## <span data-ttu-id="b4331-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b4331-112">EXAMPLES</span></span>

### <span data-ttu-id="b4331-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b4331-113">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerStep -ResourceGroupName ContosoResourceGroup -Name ContosoService1WaitStep -Location "Central US" -Duration PT20M
```

<span data-ttu-id="b4331-114">Erstellt einen Schritt im ContosoResourceGroup mit dem Namen ContosoService1WaitStep mit dem zentralen US-Standort als Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b4331-114">Creates a step in the ContosoResourceGroup with the name ContosoService1WaitStep with Central US as the location of the resource.</span></span> <span data-ttu-id="b4331-115">Die Duration-Eigenschaft gibt die Dauer an, die das Rollout wartet, bevor der nächste Schritt ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4331-115">The Duration property provides the duration the rollout will wait before running the next step.</span></span>

## <span data-ttu-id="b4331-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="b4331-116">PARAMETERS</span></span>

### <span data-ttu-id="b4331-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4331-117">-DefaultProfile</span></span>
<span data-ttu-id="b4331-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b4331-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4331-119">-Dauer</span><span class="sxs-lookup"><span data-stu-id="b4331-119">-Duration</span></span>
<span data-ttu-id="b4331-120">Die Dauer, die im ISO 8601-Format gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b4331-120">The duration to wait in ISO 8601 format.</span></span>
<span data-ttu-id="b4331-121">Z. b.: PT30M, PT1H</span><span class="sxs-lookup"><span data-stu-id="b4331-121">E.g.: PT30M, PT1H</span></span>

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

### <span data-ttu-id="b4331-122">-HealthCheckProperties</span><span class="sxs-lookup"><span data-stu-id="b4331-122">-HealthCheckProperties</span></span>
<span data-ttu-id="b4331-123">Die Integritäts Prüfeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b4331-123">The health check properties.</span></span>

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

### <span data-ttu-id="b4331-124">-HealthCheckPropertiesFile</span><span class="sxs-lookup"><span data-stu-id="b4331-124">-HealthCheckPropertiesFile</span></span>
<span data-ttu-id="b4331-125">Der Pfad zu der Datei, in der Integritäts Prüfeigenschaften definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b4331-125">The path to the file where health check properties are defined.</span></span>

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

### <span data-ttu-id="b4331-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="b4331-126">-Location</span></span>
<span data-ttu-id="b4331-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b4331-127">The location of the resource.</span></span>

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

### <span data-ttu-id="b4331-128">-Name</span><span class="sxs-lookup"><span data-stu-id="b4331-128">-Name</span></span>
<span data-ttu-id="b4331-129">Der Name des Schritts.</span><span class="sxs-lookup"><span data-stu-id="b4331-129">The name of the step.</span></span>

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

### <span data-ttu-id="b4331-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4331-130">-ResourceGroupName</span></span>
<span data-ttu-id="b4331-131">Die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b4331-131">The resource group.</span></span>

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

### <span data-ttu-id="b4331-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="b4331-132">-Tag</span></span>
<span data-ttu-id="b4331-133">Eine Hashtabelle, die Ressourcenkategorien darstellt.</span><span class="sxs-lookup"><span data-stu-id="b4331-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b4331-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b4331-134">-Confirm</span></span>
<span data-ttu-id="b4331-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b4331-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4331-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4331-136">-WhatIf</span></span>
<span data-ttu-id="b4331-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b4331-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4331-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b4331-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4331-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4331-139">CommonParameters</span></span>
<span data-ttu-id="b4331-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b4331-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4331-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b4331-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4331-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b4331-142">INPUTS</span></span>

### <span data-ttu-id="b4331-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="b4331-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b4331-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b4331-144">OUTPUTS</span></span>

### <span data-ttu-id="b4331-145">Microsoft. Azure. Commands. deploymentmanager. Models. PSStepResource</span><span class="sxs-lookup"><span data-stu-id="b4331-145">Microsoft.Azure.Commands.DeploymentManager.Models.PSStepResource</span></span>

## <span data-ttu-id="b4331-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="b4331-146">NOTES</span></span>

## <span data-ttu-id="b4331-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b4331-147">RELATED LINKS</span></span>
