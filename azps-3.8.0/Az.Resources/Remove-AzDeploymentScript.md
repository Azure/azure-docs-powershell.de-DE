---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzDeploymentScript.md
ms.openlocfilehash: a15804d0af664c46d443128e940e3b9f2c8a1acc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995502"
---
# <span data-ttu-id="c2002-101">Remove-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c2002-101">Remove-AzDeploymentScript</span></span>

## <span data-ttu-id="c2002-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2002-102">SYNOPSIS</span></span>
<span data-ttu-id="c2002-103">Entfernt ein Bereitstellungsskript und die zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c2002-103">Removes a deployment script and its associated resources.</span></span>


## <span data-ttu-id="c2002-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2002-104">SYNTAX</span></span>

### <span data-ttu-id="c2002-105">RemoveDeploymentScriptLogByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2002-105">RemoveDeploymentScriptLogByName (Default)</span></span>
```
Remove-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2002-106">RemoveDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c2002-106">RemoveDeploymentScriptLogByResourceId</span></span>
```
Remove-AzDeploymentScript [-Id] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2002-107">RemoveDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c2002-107">RemoveDeploymentScriptLogByInputObject</span></span>
```
Remove-AzDeploymentScript [-InputObject] <PsDeploymentScript> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2002-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2002-108">DESCRIPTION</span></span>
<span data-ttu-id="c2002-109">Das Cmdlet **Remove-AzDeploymentScript** entfernt ein Bereitstellungsskript und die zugehörigen Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="c2002-109">The **Remove-AzDeploymentScript** cmdlet removes a deployment script and its associated resources.</span></span>

## <span data-ttu-id="c2002-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2002-110">EXAMPLES</span></span>

### <span data-ttu-id="c2002-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2002-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="c2002-112">Löscht ein Bereitstellungsskript mit dem Namen MyDeploymentScript in der Ressourcengruppe DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c2002-112">Deletes a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

## <span data-ttu-id="c2002-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2002-113">PARAMETERS</span></span>

### <span data-ttu-id="c2002-114">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2002-114">-Confirm</span></span>
<span data-ttu-id="c2002-115">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2002-115">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2002-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2002-116">-DefaultProfile</span></span>
<span data-ttu-id="c2002-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2002-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2002-118">-ID</span><span class="sxs-lookup"><span data-stu-id="c2002-118">-Id</span></span>
<span data-ttu-id="c2002-119">Die vollqualifizierte Ressourcen-ID des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="c2002-119">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c2002-120">Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c2002-120">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2002-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2002-121">-InputObject</span></span>
<span data-ttu-id="c2002-122">Das PowerShell-Objekt des Bereitstellungsskripts.</span><span class="sxs-lookup"><span data-stu-id="c2002-122">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: RemoveDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2002-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c2002-123">-Name</span></span>
<span data-ttu-id="c2002-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2002-124">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2002-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2002-125">-PassThru</span></span>
<span data-ttu-id="c2002-126">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="c2002-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="c2002-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2002-127">-ResourceGroupName</span></span>
<span data-ttu-id="c2002-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2002-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: RemoveDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2002-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2002-129">-WhatIf</span></span>
<span data-ttu-id="c2002-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2002-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2002-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2002-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2002-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2002-132">CommonParameters</span></span>
<span data-ttu-id="c2002-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2002-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="c2002-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2002-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2002-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2002-135">INPUTS</span></span>

### <span data-ttu-id="c2002-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c2002-136">System.String</span></span>

### <span data-ttu-id="c2002-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c2002-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c2002-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2002-138">OUTPUTS</span></span>

### <span data-ttu-id="c2002-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c2002-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c2002-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2002-140">NOTES</span></span>

## <span data-ttu-id="c2002-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2002-141">RELATED LINKS</span></span>
