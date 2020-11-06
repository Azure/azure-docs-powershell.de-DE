---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 2f27a2aef23e008294a932d57538d0acec0d249a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496989"
---
# <span data-ttu-id="a32c8-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a32c8-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="a32c8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a32c8-102">SYNOPSIS</span></span>
<span data-ttu-id="a32c8-103">Erstellt einen Speicher Einblick in einen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a32c8-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a32c8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a32c8-104">SYNTAX</span></span>

### <span data-ttu-id="a32c8-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a32c8-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a32c8-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a32c8-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a32c8-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a32c8-107">DESCRIPTION</span></span>
<span data-ttu-id="a32c8-108">Das Cmdlet **New-AzureRmOperationalInsightsStorageInsight** erstellt einen neuen Speicher Einblick in einem vorhandenen Arbeitsbereich.</span><span class="sxs-lookup"><span data-stu-id="a32c8-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="a32c8-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a32c8-109">EXAMPLES</span></span>

### <span data-ttu-id="a32c8-110">Beispiel 1: Erstellen eines Speicher Einblicks anhand des Namens</span><span class="sxs-lookup"><span data-stu-id="a32c8-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a32c8-111">Der erste Befehl verwendet das Get-AzureRmStorageAccount-Cmdlet, um das Speicherkonto mit dem Namen ContosoStorage abzurufen, und speichert es dann in der $Storage-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="a32c8-112">Der zweite Befehl übergibt das Speicherkonto in $Storage an das Get-AzureRmStorageAccountKey-Cmdlet, indem es den Pipelineoperator verwendet, um den angegebenen speicherkontoschlüssel abzurufen, und speichert ihn dann in der $StorageKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="a32c8-113">Der endgültige Befehl erstellt eine Speicher Insight mit dem Namen MyStorageInsight im Arbeitsbereich mit dem Namen myworkspace.</span><span class="sxs-lookup"><span data-stu-id="a32c8-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="a32c8-114">Dieser Speicher Insight verarbeitet Daten aus der WADWindowsEventLogsTable-Tabelle in der angegebenen Speicherkonto Ressource.</span><span class="sxs-lookup"><span data-stu-id="a32c8-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="a32c8-115">Beispiel 2: Erstellen einer Speicher Einsicht mithilfe eines Workspace-Objekts</span><span class="sxs-lookup"><span data-stu-id="a32c8-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="a32c8-116">Der erste Befehl verwendet das Get-AzureRmOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und speichert ihn dann in der Variablen $Workspace.</span><span class="sxs-lookup"><span data-stu-id="a32c8-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="a32c8-117">Der zweite Befehl verwendet das Get-AzureRmStorageAccount-Cmdlet zum Abrufen des angegebenen speicherkontos und speichert es dann in der $Storage-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>

<span data-ttu-id="a32c8-118">Der dritte Befehl übergibt das Speicherkonto in $Storage an das Get-AzureRmStorageAccountKey-Cmdlet, indem es den Pipelineoperator verwendet, um den angegebenen Schlüssel abzurufen, und speichert ihn dann in der $StorageKey-Variablen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>

<span data-ttu-id="a32c8-119">Der endgültige Befehl erstellt eine Speicher Insight mit dem Namen MyStorageInsight im Arbeitsbereich, der in $Workspace definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a32c8-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="a32c8-120">Die Speicher-Insight nutzt Daten aus der WADWindowsEventLogsTable-Tabelle in der angegebenen Speicherkonto Ressource.</span><span class="sxs-lookup"><span data-stu-id="a32c8-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="a32c8-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="a32c8-121">PARAMETERS</span></span>

### <span data-ttu-id="a32c8-122">-Container</span><span class="sxs-lookup"><span data-stu-id="a32c8-122">-Containers</span></span>
<span data-ttu-id="a32c8-123">Gibt die Liste der Container an, die die Daten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a32c8-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="a32c8-124">-Force</span><span class="sxs-lookup"><span data-stu-id="a32c8-124">-Force</span></span>
<span data-ttu-id="a32c8-125">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="a32c8-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a32c8-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a32c8-126">-Name</span></span>
<span data-ttu-id="a32c8-127">Gibt den Namen des Speicher Einblicks an.</span><span class="sxs-lookup"><span data-stu-id="a32c8-127">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="a32c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a32c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="a32c8-129">Gibt den Namen einer Azure-Ressourcengruppe an, die einen Arbeitsbereich enthält.</span><span class="sxs-lookup"><span data-stu-id="a32c8-129">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="a32c8-130">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="a32c8-130">-StorageAccountKey</span></span>
<span data-ttu-id="a32c8-131">Gibt die Zugriffstaste für das Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="a32c8-131">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="a32c8-132">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="a32c8-132">-StorageAccountResourceId</span></span>
<span data-ttu-id="a32c8-133">Gibt die Azure-Ressource eines speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="a32c8-133">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="a32c8-134">Dies kann abgerufen werden, indem Sie das Get-AzureRmStorageAccount-Cmdlet ausführen und auf den *ID-* Parameter des Ergebnisses zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-134">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="a32c8-135">-Tabellen</span><span class="sxs-lookup"><span data-stu-id="a32c8-135">-Tables</span></span>
<span data-ttu-id="a32c8-136">Gibt die Liste der Tabellen an, in denen die Daten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a32c8-136">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="a32c8-137">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="a32c8-137">-Workspace</span></span>
<span data-ttu-id="a32c8-138">Gibt den Arbeitsbereich für die neue Speicher-Insight an.</span><span class="sxs-lookup"><span data-stu-id="a32c8-138">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="a32c8-139">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a32c8-139">-WorkspaceName</span></span>
<span data-ttu-id="a32c8-140">Gibt den Namen eines vorhandenen Arbeitsbereichs an.</span><span class="sxs-lookup"><span data-stu-id="a32c8-140">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="a32c8-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a32c8-141">-Confirm</span></span>
<span data-ttu-id="a32c8-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a32c8-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32c8-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32c8-143">-WhatIf</span></span>
<span data-ttu-id="a32c8-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a32c8-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32c8-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a32c8-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32c8-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32c8-146">-DefaultProfile</span></span>
<span data-ttu-id="a32c8-147">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a32c8-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a32c8-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32c8-148">CommonParameters</span></span>
<span data-ttu-id="a32c8-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32c8-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32c8-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32c8-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32c8-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a32c8-151">INPUTS</span></span>

### <span data-ttu-id="a32c8-152">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="a32c8-152">PSWorkspace</span></span>
<span data-ttu-id="a32c8-153">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a32c8-153">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="a32c8-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a32c8-154">OUTPUTS</span></span>

### <span data-ttu-id="a32c8-155">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="a32c8-155">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="a32c8-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="a32c8-156">NOTES</span></span>

## <span data-ttu-id="a32c8-157">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a32c8-157">RELATED LINKS</span></span>

[<span data-ttu-id="a32c8-158">Azure-Cmdlets für operationelle Einblicke</span><span class="sxs-lookup"><span data-stu-id="a32c8-158">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="a32c8-159">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="a32c8-159">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


