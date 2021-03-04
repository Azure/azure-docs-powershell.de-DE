---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 876414b754a259d253dc56e5d92c570aa8f48318
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940992"
---
# <span data-ttu-id="911fa-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="911fa-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="911fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="911fa-102">SYNOPSIS</span></span>
<span data-ttu-id="911fa-103">Speichert das Protokoll einer Ausführung eines Bereitstellungsskripts auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="911fa-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="911fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="911fa-104">SYNTAX</span></span>

### <span data-ttu-id="911fa-105">SaveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="911fa-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="911fa-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="911fa-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="911fa-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="911fa-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="911fa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="911fa-108">DESCRIPTION</span></span>
<span data-ttu-id="911fa-109">Das **Save-AzDeploymentScriptLog** speichert das Protokoll einer Ausführung eines Bereitstellungsskripts auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="911fa-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="911fa-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="911fa-110">EXAMPLES</span></span>

### <span data-ttu-id="911fa-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="911fa-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="911fa-112">Speichert das Protokoll eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="911fa-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="911fa-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="911fa-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="911fa-114">Speichert die letzten drei Zeilen des Protokolls eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="911fa-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="911fa-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="911fa-115">PARAMETERS</span></span>

### <span data-ttu-id="911fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="911fa-116">-DefaultProfile</span></span>
<span data-ttu-id="911fa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="911fa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="911fa-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="911fa-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="911fa-119">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="911fa-119">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="911fa-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="911fa-121">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="911fa-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="911fa-122">Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="911fa-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-123">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="911fa-123">-Force</span></span>
<span data-ttu-id="911fa-124">Erzwingt das Überschreiben der vorhandenen Datei.</span><span class="sxs-lookup"><span data-stu-id="911fa-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="911fa-125">-Name</span><span class="sxs-lookup"><span data-stu-id="911fa-125">-Name</span></span>
<span data-ttu-id="911fa-126">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="911fa-126">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="911fa-127">-OutputPath</span></span>
<span data-ttu-id="911fa-128">Der Verzeichnispfad zum Speichern des Bereitstellungsskriptprotokolls.</span><span class="sxs-lookup"><span data-stu-id="911fa-128">The directory path to save deployment script log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="911fa-129">-ResourceGroupName</span></span>
<span data-ttu-id="911fa-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="911fa-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="911fa-131">-Tail</span></span>
<span data-ttu-id="911fa-132">Ausgabe auf letzte n Zeilen beschränken</span><span class="sxs-lookup"><span data-stu-id="911fa-132">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="911fa-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="911fa-133">-Confirm</span></span>
<span data-ttu-id="911fa-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="911fa-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="911fa-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="911fa-135">-WhatIf</span></span>
<span data-ttu-id="911fa-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="911fa-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="911fa-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="911fa-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="911fa-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="911fa-138">CommonParameters</span></span>
<span data-ttu-id="911fa-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="911fa-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="911fa-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="911fa-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="911fa-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="911fa-141">INPUTS</span></span>

### <span data-ttu-id="911fa-142">System.String</span><span class="sxs-lookup"><span data-stu-id="911fa-142">System.String</span></span>

## <span data-ttu-id="911fa-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="911fa-143">OUTPUTS</span></span>

### <span data-ttu-id="911fa-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="911fa-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="911fa-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="911fa-145">NOTES</span></span>

## <span data-ttu-id="911fa-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="911fa-146">RELATED LINKS</span></span>
