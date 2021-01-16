---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358755"
---
# <span data-ttu-id="08b54-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="08b54-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="08b54-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08b54-102">SYNOPSIS</span></span>
<span data-ttu-id="08b54-103">Speichert das Protokoll der Ausführung eines Bereitstellungsskripts auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="08b54-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="08b54-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="08b54-104">SYNTAX</span></span>

### <span data-ttu-id="08b54-105">SaveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="08b54-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="08b54-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="08b54-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="08b54-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="08b54-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="08b54-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="08b54-108">DESCRIPTION</span></span>
<span data-ttu-id="08b54-109">Im **Save-AzDeploymentScriptLog** wird das Protokoll der Ausführung eines Bereitstellungsskripts auf dem Datenträger gespeichert.</span><span class="sxs-lookup"><span data-stu-id="08b54-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="08b54-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="08b54-110">EXAMPLES</span></span>

### <span data-ttu-id="08b54-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08b54-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="08b54-112">Speichert das Protokoll eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08b54-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="08b54-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="08b54-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="08b54-114">Speichert die letzten drei Zeilen des Protokolls eines Bereitstellungsskripts unter dem angegebenen Namen und der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08b54-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="08b54-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08b54-115">PARAMETERS</span></span>

### <span data-ttu-id="08b54-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08b54-116">-DefaultProfile</span></span>
<span data-ttu-id="08b54-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08b54-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08b54-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="08b54-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="08b54-119">Das Bereitstellungsskript-PowerShell-Objekt.</span><span class="sxs-lookup"><span data-stu-id="08b54-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="08b54-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="08b54-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="08b54-121">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="08b54-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="08b54-122">Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="08b54-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="08b54-123">-Force</span><span class="sxs-lookup"><span data-stu-id="08b54-123">-Force</span></span>
<span data-ttu-id="08b54-124">Erzwingt das Überschreiben der vorhandenen Datei.</span><span class="sxs-lookup"><span data-stu-id="08b54-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="08b54-125">-Name</span><span class="sxs-lookup"><span data-stu-id="08b54-125">-Name</span></span>
<span data-ttu-id="08b54-126">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="08b54-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="08b54-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="08b54-127">-OutputPath</span></span>
<span data-ttu-id="08b54-128">Der Verzeichnispfad zum Speichern des Bereitstellungsskriptprotokolls.</span><span class="sxs-lookup"><span data-stu-id="08b54-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="08b54-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08b54-129">-ResourceGroupName</span></span>
<span data-ttu-id="08b54-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08b54-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="08b54-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="08b54-131">-Tail</span></span>
<span data-ttu-id="08b54-132">Ausgabe auf letzte n Zeilen beschränken</span><span class="sxs-lookup"><span data-stu-id="08b54-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="08b54-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="08b54-133">-Confirm</span></span>
<span data-ttu-id="08b54-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08b54-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="08b54-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="08b54-135">-WhatIf</span></span>
<span data-ttu-id="08b54-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08b54-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08b54-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08b54-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="08b54-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08b54-138">CommonParameters</span></span>
<span data-ttu-id="08b54-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08b54-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08b54-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="08b54-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08b54-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="08b54-141">INPUTS</span></span>

### <span data-ttu-id="08b54-142">System.String</span><span class="sxs-lookup"><span data-stu-id="08b54-142">System.String</span></span>

## <span data-ttu-id="08b54-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="08b54-143">OUTPUTS</span></span>

### <span data-ttu-id="08b54-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="08b54-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="08b54-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="08b54-145">NOTES</span></span>

## <span data-ttu-id="08b54-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="08b54-146">RELATED LINKS</span></span>
