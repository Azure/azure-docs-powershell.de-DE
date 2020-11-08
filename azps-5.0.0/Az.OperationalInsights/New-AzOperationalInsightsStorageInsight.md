---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178142"
---
# <span data-ttu-id="3f976-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3f976-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="3f976-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f976-102">SYNOPSIS</span></span>
<span data-ttu-id="3f976-103">Erstellt einen Speicher Einblick in einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3f976-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="3f976-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f976-104">SYNTAX</span></span>

### <span data-ttu-id="3f976-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f976-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f976-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3f976-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f976-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f976-107">DESCRIPTION</span></span>
<span data-ttu-id="3f976-108">Das Cmdlet **New-AzOperationalInsightsStorageInsight** erstellt einen neuen Speicher Einblick in einem vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="3f976-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="3f976-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f976-109">EXAMPLES</span></span>

### <span data-ttu-id="3f976-110">Beispiel 1: Erstellen eines Speicher Einblicks anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="3f976-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3f976-111">Der erste Befehl verwendet das Get-AzStorageAccount-Cmdlet, um das Speicherkonto mit dem Namen ContosoStorage abzurufen, und speichert es dann in der $Storage-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3f976-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3f976-112">Der zweite Befehl übergibt das Speicherkonto in $Storage an das Get-AzStorageAccountKey-Cmdlet, indem es den Pipelineoperator verwendet, um den angegebenen speicherkontoschlüssel abzurufen, und speichert ihn dann in der $StorageKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3f976-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="3f976-113">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f976-113">This example retrieves the first key.</span></span> <span data-ttu-id="3f976-114">Wenn Sie die andere Person abrufen möchten, verwenden Sie den Wert [1] anstelle von Wert [0].</span><span class="sxs-lookup"><span data-stu-id="3f976-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="3f976-115">Der endgültige Befehl erstellt eine Speicher Insight mit dem Namen MyStorageInsight im Arbeitsbereich mit dem Namen myworkspace.</span><span class="sxs-lookup"><span data-stu-id="3f976-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="3f976-116">Dieser Speicher Insight verarbeitet Daten aus der WADWindowsEventLogsTable-Tabelle in der angegebenen Speicherkonto Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f976-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="3f976-117">Beispiel 2: Erstellen einer Speicher Einsicht mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="3f976-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="3f976-118">Der erste Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace.</span><span class="sxs-lookup"><span data-stu-id="3f976-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="3f976-119">Der zweite Befehl verwendet das Get-AzStorageAccount-Cmdlet zum Abrufen des angegebenen speicherkontos und speichert es dann in der $Storage-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3f976-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="3f976-120">Der dritte Befehl übergibt das Speicherkonto in $Storage an das Get-AzStorageAccountKey-Cmdlet, indem es den Pipelineoperator verwendet, um den angegebenen Schlüssel abzurufen, und speichert ihn dann in der $StorageKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="3f976-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="3f976-121">In diesem Beispiel wird der erste Schlüssel abgerufen.</span><span class="sxs-lookup"><span data-stu-id="3f976-121">This example retrieves the first key.</span></span> <span data-ttu-id="3f976-122">Wenn Sie die andere Person abrufen möchten, verwenden Sie den Wert [1] anstelle von Wert [0].</span><span class="sxs-lookup"><span data-stu-id="3f976-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="3f976-123">Der endgültige Befehl erstellt eine Speicher Insight mit dem Namen MyStorageInsight im Arbeitsbereich, der in $Workspace definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3f976-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="3f976-124">Die Speicher-Insight nutzt Daten aus der WADWindowsEventLogsTable-Tabelle in der angegebenen Speicherkonto Ressource.</span><span class="sxs-lookup"><span data-stu-id="3f976-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="3f976-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f976-125">PARAMETERS</span></span>

### <span data-ttu-id="3f976-126">-Container</span><span class="sxs-lookup"><span data-stu-id="3f976-126">-Containers</span></span>
<span data-ttu-id="3f976-127">Gibt die Liste der Container an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="3f976-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="3f976-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f976-128">-DefaultProfile</span></span>
<span data-ttu-id="3f976-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3f976-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3f976-130">-Force</span><span class="sxs-lookup"><span data-stu-id="3f976-130">-Force</span></span>
<span data-ttu-id="3f976-131">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="3f976-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3f976-132">-Name</span><span class="sxs-lookup"><span data-stu-id="3f976-132">-Name</span></span>
<span data-ttu-id="3f976-133">Gibt den Namen des Speicher Einblicks an.</span><span class="sxs-lookup"><span data-stu-id="3f976-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="3f976-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f976-134">-ResourceGroupName</span></span>
<span data-ttu-id="3f976-135">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="3f976-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="3f976-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="3f976-136">-StorageAccountKey</span></span>
<span data-ttu-id="3f976-137">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="3f976-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="3f976-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="3f976-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="3f976-139">Gibt die Azure-Ressource eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3f976-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="3f976-140">Dies kann abgerufen werden, indem Sie das Get-AzStorageAccount-Cmdlet ausführen und auf den *ID-* Parameter des Ergebnisses zugreifen.</span><span class="sxs-lookup"><span data-stu-id="3f976-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="3f976-141">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="3f976-141">-Tables</span></span>
<span data-ttu-id="3f976-142">Gibt die Liste der Tabellen an, in denen die Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3f976-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="3f976-143">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="3f976-143">-Workspace</span></span>
<span data-ttu-id="3f976-144">Gibt den Arbeitsbereich für die neue Speicher-Insight an.</span><span class="sxs-lookup"><span data-stu-id="3f976-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="3f976-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3f976-145">-WorkspaceName</span></span>
<span data-ttu-id="3f976-146">Gibt den Namen eines vorhandenen Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="3f976-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="3f976-147">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f976-147">-Confirm</span></span>
<span data-ttu-id="3f976-148">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f976-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f976-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f976-149">-WhatIf</span></span>
<span data-ttu-id="3f976-150">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f976-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f976-151">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f976-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f976-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f976-152">CommonParameters</span></span>
<span data-ttu-id="3f976-153">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f976-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f976-154">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f976-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f976-155">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f976-155">INPUTS</span></span>

### <span data-ttu-id="3f976-156">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f976-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="3f976-157">System. String</span><span class="sxs-lookup"><span data-stu-id="3f976-157">System.String</span></span>

### <span data-ttu-id="3f976-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="3f976-158">System.String[]</span></span>

## <span data-ttu-id="3f976-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f976-159">OUTPUTS</span></span>

### <span data-ttu-id="3f976-160">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="3f976-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="3f976-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f976-161">NOTES</span></span>

## <span data-ttu-id="3f976-162">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f976-162">RELATED LINKS</span></span>

[<span data-ttu-id="3f976-163">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="3f976-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="3f976-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="3f976-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


