---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 7eece12130095889c5da574a4d0a3ec8d0b0bed2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937883"
---
# <span data-ttu-id="98421-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="98421-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="98421-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98421-102">SYNOPSIS</span></span>
<span data-ttu-id="98421-103">Entfernt eine Speicherinblicke.</span><span class="sxs-lookup"><span data-stu-id="98421-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="98421-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98421-104">SYNTAX</span></span>

### <span data-ttu-id="98421-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="98421-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98421-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="98421-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98421-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98421-107">DESCRIPTION</span></span>
<span data-ttu-id="98421-108">Das **Cmdlet Remove-AzOperationalInsightsStorageInsight** löscht einen Speichereinblick aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="98421-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="98421-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98421-109">EXAMPLES</span></span>

### <span data-ttu-id="98421-110">Beispiel 1: Entfernen einer Speicheraufschlussansicht nach Name</span><span class="sxs-lookup"><span data-stu-id="98421-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="98421-111">Mit diesem Befehl wird die Storage Insight mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen MyWorkspace in der angegebenen Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="98421-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="98421-112">Der Befehl gibt den *Parameter* Erzwingen nicht an, daher werden Sie zur Bestätigung aufgefordert, bevor Sie die Storage Insight entfernen.</span><span class="sxs-lookup"><span data-stu-id="98421-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="98421-113">Beispiel 2: Entfernen einer Speicheraufschlussansicht ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="98421-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="98421-114">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und speichert ihn dann in der $Workspace-Variable. Mit dem zweiten Befehl wird die Speichereinsicht mit dem Namen "MyStorageInsight" aus $Workspace entfernt, ohne Sie zur Bestätigung auffordern zu müssen.</span><span class="sxs-lookup"><span data-stu-id="98421-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="98421-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98421-115">PARAMETERS</span></span>

### <span data-ttu-id="98421-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98421-116">-DefaultProfile</span></span>
<span data-ttu-id="98421-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98421-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98421-118">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="98421-118">-Force</span></span>
<span data-ttu-id="98421-119">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="98421-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="98421-120">-Name</span><span class="sxs-lookup"><span data-stu-id="98421-120">-Name</span></span>
<span data-ttu-id="98421-121">Gibt den Namen der Speicheraufschluss-Datei an.</span><span class="sxs-lookup"><span data-stu-id="98421-121">Specifies the name of the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98421-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98421-122">-ResourceGroupName</span></span>
<span data-ttu-id="98421-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="98421-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98421-124">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="98421-124">-Workspace</span></span>
<span data-ttu-id="98421-125">Gibt den Arbeitsbereich an, der die Storage Insight enthält.</span><span class="sxs-lookup"><span data-stu-id="98421-125">Specifies the workspace that contains the Storage Insight.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98421-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="98421-126">-WorkspaceName</span></span>
<span data-ttu-id="98421-127">Gibt den Namen des Arbeitsbereichs an, der die Speicheraufschluss-Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="98421-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98421-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98421-128">-Confirm</span></span>
<span data-ttu-id="98421-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98421-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98421-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98421-130">-WhatIf</span></span>
<span data-ttu-id="98421-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98421-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98421-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98421-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98421-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98421-133">CommonParameters</span></span>
<span data-ttu-id="98421-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98421-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98421-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98421-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98421-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98421-136">INPUTS</span></span>

### <span data-ttu-id="98421-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="98421-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="98421-138">System.String</span><span class="sxs-lookup"><span data-stu-id="98421-138">System.String</span></span>

## <span data-ttu-id="98421-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98421-139">OUTPUTS</span></span>

### <span data-ttu-id="98421-140">System.Void</span><span class="sxs-lookup"><span data-stu-id="98421-140">System.Void</span></span>

## <span data-ttu-id="98421-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98421-141">NOTES</span></span>

## <span data-ttu-id="98421-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98421-142">RELATED LINKS</span></span>

[<span data-ttu-id="98421-143">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="98421-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="98421-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="98421-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


