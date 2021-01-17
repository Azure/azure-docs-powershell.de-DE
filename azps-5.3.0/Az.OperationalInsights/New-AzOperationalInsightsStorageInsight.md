---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473302"
---
# <span data-ttu-id="44d26-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="44d26-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="44d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44d26-102">SYNOPSIS</span></span>
<span data-ttu-id="44d26-103">Erstellt speicherinteblicke innerhalb eines Arbeitsbereichs.</span><span class="sxs-lookup"><span data-stu-id="44d26-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="44d26-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="44d26-104">SYNTAX</span></span>

### <span data-ttu-id="44d26-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="44d26-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="44d26-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="44d26-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="44d26-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="44d26-107">DESCRIPTION</span></span>
<span data-ttu-id="44d26-108">Das **Cmdlet "New-AzOperationalInsightsStorageInsight"** erstellt einen neuen Speichereinblick in einem vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="44d26-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="44d26-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="44d26-109">EXAMPLES</span></span>

### <span data-ttu-id="44d26-110">Beispiel 1: Erstellen eines Speicherinblicks nach Name</span><span class="sxs-lookup"><span data-stu-id="44d26-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="44d26-111">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das Speicherkonto "ContosoStorage" zu erhalten, und speichert es dann in der $Storage Variable.</span><span class="sxs-lookup"><span data-stu-id="44d26-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="44d26-112">Der zweite Befehl übergibt das Speicherkonto in $Storage an das Get-AzStorageAccountKey-Cmdlet, indem der Pipelineoperator verwendet wird, um den angegebenen Speicherkontoschlüssel zu erhalten, und speichert ihn dann in der $StorageKey-Variable.</span><span class="sxs-lookup"><span data-stu-id="44d26-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="44d26-113">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="44d26-113">This example retrieves the first key.</span></span> <span data-ttu-id="44d26-114">Verwenden Sie "Value[1]" anstelle von "Value[0]." (Wert[0].</span><span class="sxs-lookup"><span data-stu-id="44d26-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="44d26-115">Der letzte Befehl erstellt einen Speichereinblick mit dem Namen "MyStorageInsight" im Arbeitsbereich "MyWorkspace".</span><span class="sxs-lookup"><span data-stu-id="44d26-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="44d26-116">Dieser Speicherblick verbraucht Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="44d26-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="44d26-117">Beispiel 2: Erstellen eines Speicherinblicks mithilfe eines Arbeitsbereichsobjekts</span><span class="sxs-lookup"><span data-stu-id="44d26-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="44d26-118">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace Cmdlet, um den Arbeitsbereich "MyWorkspace" zu erhalten, und speichert ihn dann in der $Workspace Variable.</span><span class="sxs-lookup"><span data-stu-id="44d26-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="44d26-119">Der zweite Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das angegebene Speicherkonto zu erhalten, und speichert es dann in $Storage Variable.</span><span class="sxs-lookup"><span data-stu-id="44d26-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="44d26-120">Der dritte Befehl übergibt das Speicherkonto in $Storage an das Get-AzStorageAccountKey-Cmdlet, indem er den angegebenen Schlüssel mithilfe des Pipelineoperators abgibt, und speichert ihn dann in der $StorageKey-Variable.</span><span class="sxs-lookup"><span data-stu-id="44d26-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="44d26-121">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="44d26-121">This example retrieves the first key.</span></span> <span data-ttu-id="44d26-122">Verwenden Sie "Value[1]" anstelle von "Value[0]." (Wert[0].</span><span class="sxs-lookup"><span data-stu-id="44d26-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="44d26-123">Der letzte Befehl erstellt einen Speichereinblick mit dem Namen "MyStorageInsight" in dem arbeitsbereich, der in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="44d26-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="44d26-124">Der Storage Insight verwendet Daten aus der Tabelle WADWindowsEventLogsTable in der angegebenen Speicherkontoressource.</span><span class="sxs-lookup"><span data-stu-id="44d26-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="44d26-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44d26-125">PARAMETERS</span></span>

### <span data-ttu-id="44d26-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="44d26-126">-Containers</span></span>
<span data-ttu-id="44d26-127">Gibt die Liste der Container an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="44d26-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="44d26-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44d26-128">-DefaultProfile</span></span>
<span data-ttu-id="44d26-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="44d26-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="44d26-130">-Force</span><span class="sxs-lookup"><span data-stu-id="44d26-130">-Force</span></span>
<span data-ttu-id="44d26-131">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="44d26-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="44d26-132">-Name</span><span class="sxs-lookup"><span data-stu-id="44d26-132">-Name</span></span>
<span data-ttu-id="44d26-133">Gibt den Namen der Speicherinblicke an.</span><span class="sxs-lookup"><span data-stu-id="44d26-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="44d26-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44d26-134">-ResourceGroupName</span></span>
<span data-ttu-id="44d26-135">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="44d26-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="44d26-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="44d26-136">-StorageAccountKey</span></span>
<span data-ttu-id="44d26-137">Gibt den Zugriffsschlüssel für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="44d26-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="44d26-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="44d26-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="44d26-139">Gibt die Azure-Ressource eines Speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="44d26-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="44d26-140">Dies kann abgerufen werden, indem das Get-AzStorageAccount ausgeführt wird und auf den Parameter *"Id"* des Ergebnisses zugegriffen wird.</span><span class="sxs-lookup"><span data-stu-id="44d26-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="44d26-141">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="44d26-141">-Tables</span></span>
<span data-ttu-id="44d26-142">Gibt die Liste der Tabellen an, in der die Daten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="44d26-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="44d26-143">-Workspace</span><span class="sxs-lookup"><span data-stu-id="44d26-143">-Workspace</span></span>
<span data-ttu-id="44d26-144">Gibt den Arbeitsbereich für den neuen Speicherblick an.</span><span class="sxs-lookup"><span data-stu-id="44d26-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="44d26-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="44d26-145">-WorkspaceName</span></span>
<span data-ttu-id="44d26-146">Gibt den Namen eines vorhandenen Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="44d26-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="44d26-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="44d26-147">-Confirm</span></span>
<span data-ttu-id="44d26-148">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="44d26-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44d26-149">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="44d26-149">-WhatIf</span></span>
<span data-ttu-id="44d26-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d26-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44d26-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="44d26-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44d26-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44d26-152">CommonParameters</span></span>
<span data-ttu-id="44d26-153">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44d26-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44d26-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="44d26-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44d26-155">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="44d26-155">INPUTS</span></span>

### <span data-ttu-id="44d26-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="44d26-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="44d26-157">System.String</span><span class="sxs-lookup"><span data-stu-id="44d26-157">System.String</span></span>

### <span data-ttu-id="44d26-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="44d26-158">System.String[]</span></span>

## <span data-ttu-id="44d26-159">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="44d26-159">OUTPUTS</span></span>

### <span data-ttu-id="44d26-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="44d26-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="44d26-161">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="44d26-161">NOTES</span></span>

## <span data-ttu-id="44d26-162">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="44d26-162">RELATED LINKS</span></span>

[<span data-ttu-id="44d26-163">Azure Operational Insights-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="44d26-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="44d26-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="44d26-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


