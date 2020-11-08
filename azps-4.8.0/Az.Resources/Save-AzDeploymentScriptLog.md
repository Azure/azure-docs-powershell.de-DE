---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 25f20b56ef7da59851d4726ad573c07d4da259e1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165636"
---
# <span data-ttu-id="fbbf6-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="fbbf6-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="fbbf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fbbf6-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbf6-103">Speichert das Protokoll einer Bereitstellungsskript Ausführung auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fbbf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fbbf6-104">SYNTAX</span></span>

### <span data-ttu-id="fbbf6-105">SaveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="fbbf6-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fbbf6-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="fbbf6-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [[-Tail] <Int32>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fbbf6-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="fbbf6-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [-OutputPath] <String>
 [[-Tail] <Int32>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fbbf6-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbbf6-108">DESCRIPTION</span></span>
<span data-ttu-id="fbbf6-109">Das **Save-AzDeploymentScriptLog** speichert das Protokoll einer Bereitstellung-Skriptausführung auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="fbbf6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fbbf6-110">EXAMPLES</span></span>

### <span data-ttu-id="fbbf6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbbf6-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="fbbf6-112">Speichert das Protokoll eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-112">Saves the log of a deployment script with the given name and resource group.</span></span>

### <span data-ttu-id="fbbf6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fbbf6-113">Example 2</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace -Tail 3
```

<span data-ttu-id="fbbf6-114">Speichert die letzten 3 Zeilen des Protokolls eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-114">Saves the last 3 lines of the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="fbbf6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="fbbf6-115">PARAMETERS</span></span>

### <span data-ttu-id="fbbf6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbf6-116">-DefaultProfile</span></span>
<span data-ttu-id="fbbf6-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbf6-118">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="fbbf6-118">-DeploymentScriptObject</span></span>
<span data-ttu-id="fbbf6-119">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-119">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="fbbf6-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="fbbf6-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="fbbf6-121">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="fbbf6-122">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="fbbf6-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="fbbf6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="fbbf6-123">-Force</span></span>
<span data-ttu-id="fbbf6-124">Erzwingt das Überschreiben der vorhandenen Datei.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="fbbf6-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fbbf6-125">-Name</span></span>
<span data-ttu-id="fbbf6-126">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-126">The name of the deployment script.</span></span>

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

### <span data-ttu-id="fbbf6-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="fbbf6-127">-OutputPath</span></span>
<span data-ttu-id="fbbf6-128">Der Verzeichnispfad zum Speichern des Bereitstellungsskript Protokolls.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-128">The directory path to save deployment script log.</span></span>

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

### <span data-ttu-id="fbbf6-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbf6-129">-ResourceGroupName</span></span>
<span data-ttu-id="fbbf6-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="fbbf6-131">-Tail</span><span class="sxs-lookup"><span data-stu-id="fbbf6-131">-Tail</span></span>
<span data-ttu-id="fbbf6-132">Ausgabe auf letzte n Zeilen begrenzen</span><span class="sxs-lookup"><span data-stu-id="fbbf6-132">Limit output to last n lines</span></span>

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

### <span data-ttu-id="fbbf6-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="fbbf6-133">-Confirm</span></span>
<span data-ttu-id="fbbf6-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbf6-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fbbf6-135">-WhatIf</span></span>
<span data-ttu-id="fbbf6-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbf6-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbf6-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbf6-138">CommonParameters</span></span>
<span data-ttu-id="fbbf6-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbf6-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbf6-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fbbf6-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbf6-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fbbf6-141">INPUTS</span></span>

### <span data-ttu-id="fbbf6-142">System. String</span><span class="sxs-lookup"><span data-stu-id="fbbf6-142">System.String</span></span>

## <span data-ttu-id="fbbf6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fbbf6-143">OUTPUTS</span></span>

### <span data-ttu-id="fbbf6-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="fbbf6-144">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="fbbf6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="fbbf6-145">NOTES</span></span>

## <span data-ttu-id="fbbf6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fbbf6-146">RELATED LINKS</span></span>
