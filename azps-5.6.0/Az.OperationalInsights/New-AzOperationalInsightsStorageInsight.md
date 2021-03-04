---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937960"
---
# <span data-ttu-id="17751-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="17751-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="17751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17751-102">SYNOPSIS</span></span>
<span data-ttu-id="17751-103">Erstellt eine Speicherinblicke innerhalb eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="17751-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="17751-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="17751-104">SYNTAX</span></span>

### <span data-ttu-id="17751-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="17751-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="17751-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="17751-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17751-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17751-107">DESCRIPTION</span></span>
<span data-ttu-id="17751-108">Das **Cmdlet New-AzOperationalInsightsStorageInsight** erstellt einen neuen Speichereinblick in einem vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="17751-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="17751-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="17751-109">EXAMPLES</span></span>

### <span data-ttu-id="17751-110">Beispiel 1: Erstellen einer Speicheraufschlussansicht nach Name</span><span class="sxs-lookup"><span data-stu-id="17751-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="17751-111">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das Speicherkonto namens ContosoStorage zu erhalten, und speichert es dann in der $Storage Variablen.</span><span class="sxs-lookup"><span data-stu-id="17751-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="17751-112">Der zweite Befehl übergibt das Speicherkonto in $Storage mithilfe des Pipelineoperators an das Get-AzStorageAccountKey-Cmdlet, um den angegebenen Speicherkontoschlüssel zu erhalten, und speichert ihn dann in der variablen $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="17751-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="17751-113">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="17751-113">This example retrieves the first key.</span></span> <span data-ttu-id="17751-114">Verwenden Sie zum Abrufen des anderen Werts[1] anstelle von Wert[0].</span><span class="sxs-lookup"><span data-stu-id="17751-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="17751-115">Mit dem letzten Befehl wird eine Speichereinsicht mit dem Namen "MyStorageInsight" im Arbeitsbereich mit dem Namen "MyWorkspace" erstellt.</span><span class="sxs-lookup"><span data-stu-id="17751-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="17751-116">Diese Speicheraufschlussinformationen nutzen Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="17751-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="17751-117">Beispiel 2: Erstellen einer Speicheraufschlussansicht mithilfe eines Arbeitsbereichsobjekts</span><span class="sxs-lookup"><span data-stu-id="17751-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="17751-118">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen MyWorkspace zu erhalten, und speichert ihn dann in der $Workspace-Variable.</span><span class="sxs-lookup"><span data-stu-id="17751-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="17751-119">Der zweite Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das angegebene Speicherkonto zu erhalten, und speichert es dann in der $Storage Variablen.</span><span class="sxs-lookup"><span data-stu-id="17751-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="17751-120">Der dritte Befehl übergibt das Speicherkonto in $Storage mithilfe des Pipelineoperators an das Get-AzStorageAccountKey-Cmdlet, um den angegebenen Schlüssel zu erhalten, und speichert ihn dann in der variablen $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="17751-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="17751-121">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="17751-121">This example retrieves the first key.</span></span> <span data-ttu-id="17751-122">Verwenden Sie zum Abrufen des anderen Werts[1] anstelle von Wert[0].</span><span class="sxs-lookup"><span data-stu-id="17751-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="17751-123">Mit dem letzten Befehl wird eine Speichereinsicht namens "MyStorageInsight" in dem arbeitsbereich erstellt, der in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="17751-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="17751-124">Die Storage Insight verwendet Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="17751-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="17751-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="17751-125">PARAMETERS</span></span>

### <span data-ttu-id="17751-126">-Container</span><span class="sxs-lookup"><span data-stu-id="17751-126">-Containers</span></span>
<span data-ttu-id="17751-127">Gibt die Liste der Container an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="17751-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17751-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17751-128">-DefaultProfile</span></span>
<span data-ttu-id="17751-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="17751-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="17751-130">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="17751-130">-Force</span></span>
<span data-ttu-id="17751-131">Erzwingt die Ausführung des Befehls, ohne den Benutzer um Bestätigung zu bitten.</span><span class="sxs-lookup"><span data-stu-id="17751-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="17751-132">-Name</span><span class="sxs-lookup"><span data-stu-id="17751-132">-Name</span></span>
<span data-ttu-id="17751-133">Gibt den Namen der Speicheraufschluss-Datei an.</span><span class="sxs-lookup"><span data-stu-id="17751-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="17751-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17751-134">-ResourceGroupName</span></span>
<span data-ttu-id="17751-135">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="17751-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="17751-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="17751-136">-StorageAccountKey</span></span>
<span data-ttu-id="17751-137">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="17751-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17751-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="17751-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="17751-139">Gibt die Azure-Ressource eines Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="17751-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="17751-140">Dies kann abgerufen werden, indem das cmdlet Get-AzStorageAccount ausgeführt wird und auf den Parameter *Id* des Ergebnisses zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="17751-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17751-141">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="17751-141">-Tables</span></span>
<span data-ttu-id="17751-142">Gibt die Liste der Tabellen an, die die Daten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="17751-142">Specifies the list of tables that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="17751-143">-Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="17751-143">-Workspace</span></span>
<span data-ttu-id="17751-144">Gibt den Arbeitsbereich für die neue Storage Insight an.</span><span class="sxs-lookup"><span data-stu-id="17751-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="17751-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="17751-145">-WorkspaceName</span></span>
<span data-ttu-id="17751-146">Gibt den Namen eines vorhandenen Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="17751-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="17751-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="17751-147">-Confirm</span></span>
<span data-ttu-id="17751-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="17751-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17751-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17751-149">-WhatIf</span></span>
<span data-ttu-id="17751-150">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="17751-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17751-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="17751-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17751-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17751-152">CommonParameters</span></span>
<span data-ttu-id="17751-153">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17751-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17751-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17751-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17751-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="17751-155">INPUTS</span></span>

### <span data-ttu-id="17751-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="17751-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="17751-157">System.String</span><span class="sxs-lookup"><span data-stu-id="17751-157">System.String</span></span>

### <span data-ttu-id="17751-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="17751-158">System.String[]</span></span>

## <span data-ttu-id="17751-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="17751-159">OUTPUTS</span></span>

### <span data-ttu-id="17751-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="17751-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="17751-161">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="17751-161">NOTES</span></span>

## <span data-ttu-id="17751-162">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="17751-162">RELATED LINKS</span></span>

[<span data-ttu-id="17751-163">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="17751-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="17751-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="17751-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


