---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: ac9e061fea8c6d7737eb268feec225dff0b0924d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165073"
---
# <span data-ttu-id="5276e-101">Remove-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5276e-101">Remove-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="5276e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5276e-102">SYNOPSIS</span></span>
<span data-ttu-id="5276e-103">Entfernt eine Speicher Einsicht.</span><span class="sxs-lookup"><span data-stu-id="5276e-103">Removes a Storage Insight.</span></span>

## <span data-ttu-id="5276e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5276e-104">SYNTAX</span></span>

### <span data-ttu-id="5276e-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5276e-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5276e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5276e-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5276e-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5276e-107">DESCRIPTION</span></span>
<span data-ttu-id="5276e-108">Das Cmdlet **Remove-AzOperationalInsightsStorageInsight** löscht einen Speicher Einblick aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5276e-108">The **Remove-AzOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="5276e-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5276e-109">EXAMPLES</span></span>

### <span data-ttu-id="5276e-110">Beispiel 1: Entfernen eines Speicher Einblicks nach Namen</span><span class="sxs-lookup"><span data-stu-id="5276e-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="5276e-111">Mit diesem Befehl wird der Speicher Insight mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen "mein Workspace" in der angegebenen Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="5276e-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="5276e-112">Der Befehl gibt nicht den Parameter *Force* an, sodass Sie zur Bestätigung aufgefordert werden, bevor Sie die Speicher Einsicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="5276e-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="5276e-113">Beispiel 2: Entfernen eines Speicher Einblicks ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="5276e-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="5276e-114">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace. Mit dem zweiten Befehl wird der Speicher Insight mit dem Namen MyStorageInsight aus $Workspace entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5276e-114">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="5276e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5276e-115">PARAMETERS</span></span>

### <span data-ttu-id="5276e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5276e-116">-DefaultProfile</span></span>
<span data-ttu-id="5276e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5276e-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5276e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5276e-118">-Force</span></span>
<span data-ttu-id="5276e-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5276e-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5276e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5276e-120">-Name</span></span>
<span data-ttu-id="5276e-121">Gibt den Namen des Speicher Einblicks an.</span><span class="sxs-lookup"><span data-stu-id="5276e-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="5276e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5276e-122">-ResourceGroupName</span></span>
<span data-ttu-id="5276e-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5276e-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="5276e-124">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5276e-124">-Workspace</span></span>
<span data-ttu-id="5276e-125">Gibt den Arbeitsbereich an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="5276e-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5276e-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5276e-126">-WorkspaceName</span></span>
<span data-ttu-id="5276e-127">Gibt den Namen des Arbeitsbereichs an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="5276e-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5276e-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5276e-128">-Confirm</span></span>
<span data-ttu-id="5276e-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5276e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5276e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5276e-130">-WhatIf</span></span>
<span data-ttu-id="5276e-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5276e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5276e-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5276e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5276e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5276e-133">CommonParameters</span></span>
<span data-ttu-id="5276e-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5276e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5276e-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5276e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5276e-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5276e-136">INPUTS</span></span>

### <span data-ttu-id="5276e-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5276e-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="5276e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5276e-138">System.String</span></span>

## <span data-ttu-id="5276e-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5276e-139">OUTPUTS</span></span>

### <span data-ttu-id="5276e-140">System. void</span><span class="sxs-lookup"><span data-stu-id="5276e-140">System.Void</span></span>

## <span data-ttu-id="5276e-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="5276e-141">NOTES</span></span>

## <span data-ttu-id="5276e-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5276e-142">RELATED LINKS</span></span>

[<span data-ttu-id="5276e-143">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="5276e-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="5276e-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5276e-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


