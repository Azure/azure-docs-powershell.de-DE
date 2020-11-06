---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 92261663-CF50-4EBD-85D2-C2E254F39B41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 726386fb4a455b3daab314e5f61d33122592dcf8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495813"
---
# <span data-ttu-id="5a6e4-101">Remove-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="5a6e4-101">Remove-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="5a6e4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5a6e4-102">SYNOPSIS</span></span>
<span data-ttu-id="5a6e4-103">Entfernt eine Speicher Einsicht.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-103">Removes a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a6e4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a6e4-104">SYNTAX</span></span>

### <span data-ttu-id="5a6e4-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5a6e4-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a6e4-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="5a6e4-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a6e4-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5a6e4-107">DESCRIPTION</span></span>
<span data-ttu-id="5a6e4-108">Das Cmdlet **Remove-AzureRmOperationalInsightsStorageInsight** löscht einen Speicher Einblick aus einem Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-108">The **Remove-AzureRmOperationalInsightsStorageInsight** cmdlet deletes a Storage Insight from a workspace.</span></span>

## <span data-ttu-id="5a6e4-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5a6e4-109">EXAMPLES</span></span>

### <span data-ttu-id="5a6e4-110">Beispiel 1: Entfernen eines Speicher Einblicks nach Namen</span><span class="sxs-lookup"><span data-stu-id="5a6e4-110">Example 1: Remove a Storage Insight by name</span></span>
```
PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight"
```

<span data-ttu-id="5a6e4-111">Mit diesem Befehl wird der Speicher Insight mit dem Namen MyStorageInsight aus dem Arbeitsbereich mit dem Namen "mein Workspace" in der angegebenen Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-111">This command removes the Storage Insight named MyStorageInsight from the workspace named MyWorkspace in the specified resource group.</span></span>
<span data-ttu-id="5a6e4-112">Der Befehl gibt nicht den Parameter *Force* an, sodass Sie zur Bestätigung aufgefordert werden, bevor Sie die Speicher Einsicht entfernen.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-112">The command does not specify the *Force* parameter, so it prompts you for confirmation before removing the Storage Insight.</span></span>

### <span data-ttu-id="5a6e4-113">Beispiel 2: Entfernen eines Speicher Einblicks ohne Bestätigung</span><span class="sxs-lookup"><span data-stu-id="5a6e4-113">Example 2: Remove a Storage Insight without confirmation</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Remove-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Force
```

<span data-ttu-id="5a6e4-114">Der erste Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace. Mit dem zweiten Befehl wird der Speicher Insight mit dem Namen MyStorageInsight aus $Workspace entfernt, ohne dass Sie zur Bestätigung aufgefordert werden.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-114">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.The second command removes the storage insight named MyStorageInsight from $Workspace without prompting you for confirmation.</span></span>

## <span data-ttu-id="5a6e4-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5a6e4-115">PARAMETERS</span></span>

### <span data-ttu-id="5a6e4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a6e4-116">-DefaultProfile</span></span>
<span data-ttu-id="5a6e4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5a6e4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a6e4-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5a6e4-118">-Force</span></span>
<span data-ttu-id="5a6e4-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5a6e4-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5a6e4-120">-Name</span></span>
<span data-ttu-id="5a6e4-121">Gibt den Namen des Speicher Einblicks an.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-121">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="5a6e4-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a6e4-122">-ResourceGroupName</span></span>
<span data-ttu-id="5a6e4-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="5a6e4-124">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="5a6e4-124">-Workspace</span></span>
<span data-ttu-id="5a6e4-125">Gibt den Arbeitsbereich an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-125">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5a6e4-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="5a6e4-126">-WorkspaceName</span></span>
<span data-ttu-id="5a6e4-127">Gibt den Namen des Arbeitsbereichs an, der den Speicher Einblick enthält.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-127">Specifies the name of the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="5a6e4-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5a6e4-128">-Confirm</span></span>
<span data-ttu-id="5a6e4-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a6e4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a6e4-130">-WhatIf</span></span>
<span data-ttu-id="5a6e4-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a6e4-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a6e4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a6e4-133">CommonParameters</span></span>
<span data-ttu-id="5a6e4-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a6e4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a6e4-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a6e4-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a6e4-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5a6e4-136">INPUTS</span></span>

### <span data-ttu-id="5a6e4-137">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a6e4-137">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="5a6e4-138">Parameter: Arbeitsbereich (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5a6e4-138">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="5a6e4-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5a6e4-139">System.String</span></span>

## <span data-ttu-id="5a6e4-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5a6e4-140">OUTPUTS</span></span>

### <span data-ttu-id="5a6e4-141">System. void</span><span class="sxs-lookup"><span data-stu-id="5a6e4-141">System.Void</span></span>

## <span data-ttu-id="5a6e4-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5a6e4-142">NOTES</span></span>

## <span data-ttu-id="5a6e4-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5a6e4-143">RELATED LINKS</span></span>

[<span data-ttu-id="5a6e4-144">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="5a6e4-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="5a6e4-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="5a6e4-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


