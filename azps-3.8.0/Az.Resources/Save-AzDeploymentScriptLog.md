---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzDeploymentScriptLog.md
ms.openlocfilehash: 4e32726b3e7af6608092d29fd52f7a41be042d42
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996489"
---
# <span data-ttu-id="90abd-101">Save-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="90abd-101">Save-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="90abd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="90abd-102">SYNOPSIS</span></span>
<span data-ttu-id="90abd-103">Speichert das Protokoll einer Bereitstellungsskript Ausführung auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="90abd-103">Saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="90abd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="90abd-104">SYNTAX</span></span>

### <span data-ttu-id="90abd-105">SaveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="90abd-105">SaveDeploymentScriptLogByName (Default)</span></span>
```
Save-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90abd-106">SaveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="90abd-106">SaveDeploymentScriptLogByResourceId</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="90abd-107">SaveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="90abd-107">SaveDeploymentScriptLogByInputObject</span></span>
```
Save-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript> [-OutputPath] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90abd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="90abd-108">DESCRIPTION</span></span>
<span data-ttu-id="90abd-109">Das **Save-AzDeploymentScriptLog** speichert das Protokoll einer Bereitstellung-Skriptausführung auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="90abd-109">The **Save-AzDeploymentScriptLog** saves the log of a deployment script execution to disk.</span></span>

## <span data-ttu-id="90abd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="90abd-110">EXAMPLES</span></span>

### <span data-ttu-id="90abd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="90abd-111">Example 1</span></span>
```powershell
PS C:\> Save-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -OutputPath C:\Workspace
```

<span data-ttu-id="90abd-112">Speichert das Protokoll eines Bereitstellungsskripts mit dem angegebenen Namen und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90abd-112">Saves the log of a deployment script with the given name and resource group.</span></span>

## <span data-ttu-id="90abd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="90abd-113">PARAMETERS</span></span>

### <span data-ttu-id="90abd-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="90abd-114">-Confirm</span></span>
<span data-ttu-id="90abd-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="90abd-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90abd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90abd-116">-DefaultProfile</span></span>
<span data-ttu-id="90abd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="90abd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="90abd-118">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="90abd-118">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="90abd-119">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="90abd-119">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: SaveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abd-120">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="90abd-120">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="90abd-121">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="90abd-121">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="90abd-122">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="90abd-122">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90abd-123">-Force</span><span class="sxs-lookup"><span data-stu-id="90abd-123">-Force</span></span>
<span data-ttu-id="90abd-124">Erzwingt das Überschreiben der vorhandenen Datei.</span><span class="sxs-lookup"><span data-stu-id="90abd-124">Forces the overwrite of the existing file.</span></span>

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

### <span data-ttu-id="90abd-125">-Name</span><span class="sxs-lookup"><span data-stu-id="90abd-125">-Name</span></span>
<span data-ttu-id="90abd-126">Der Name des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="90abd-126">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90abd-127">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="90abd-127">-OutputPath</span></span>
<span data-ttu-id="90abd-128">Der Verzeichnispfad zum Speichern des Bereitstellungsskript Protokolls.</span><span class="sxs-lookup"><span data-stu-id="90abd-128">The directory path to save deployment script log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90abd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90abd-129">-ResourceGroupName</span></span>
<span data-ttu-id="90abd-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="90abd-130">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: SaveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90abd-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90abd-131">-WhatIf</span></span>
<span data-ttu-id="90abd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="90abd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90abd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="90abd-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90abd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90abd-134">CommonParameters</span></span>
<span data-ttu-id="90abd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90abd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="90abd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90abd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90abd-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="90abd-137">INPUTS</span></span>

### <span data-ttu-id="90abd-138">System. String</span><span class="sxs-lookup"><span data-stu-id="90abd-138">System.String</span></span>

## <span data-ttu-id="90abd-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="90abd-139">OUTPUTS</span></span>

### <span data-ttu-id="90abd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span><span class="sxs-lookup"><span data-stu-id="90abd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLogPath</span></span>

## <span data-ttu-id="90abd-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="90abd-141">NOTES</span></span>

## <span data-ttu-id="90abd-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="90abd-142">RELATED LINKS</span></span>
