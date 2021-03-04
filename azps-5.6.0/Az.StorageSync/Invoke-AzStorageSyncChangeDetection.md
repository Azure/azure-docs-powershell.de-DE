---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: d55ffe30554c70b9d7b8fa1ed90380c6a5b181cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948328"
---
# <span data-ttu-id="f6286-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="f6286-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="f6286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6286-102">SYNOPSIS</span></span>
<span data-ttu-id="f6286-103">Dieser Befehl kann verwendet werden, um die Erkennung von Namespaceänderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="f6286-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="f6286-104">Sie kann auf die gesamte Freigabe, den Unterordner oder die gesamte Gruppe von Dateien ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="f6286-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="f6286-105">Es können maximal 10.000 Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="f6286-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="f6286-106">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb der 10.000-Elementgrenze abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6286-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="f6286-107">Das Invoke-AzStorageSyncChangeDetection-Cmdlet erkennt die folgenden Änderungen in der Azure-Dateifreigabe nicht:</span><span class="sxs-lookup"><span data-stu-id="f6286-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="f6286-108">Gelöschte Dateien.</span><span class="sxs-lookup"><span data-stu-id="f6286-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="f6286-109">Dateien, die aus der Freigabe verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="f6286-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="f6286-110">Dateien, die gelöscht und unter demselben Namen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="f6286-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="f6286-111">Diese Änderungen werden erkannt, wenn der [Änderungserkennungsauftrag ausgeführt](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="f6286-112">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6286-112">SYNTAX</span></span>

### <span data-ttu-id="f6286-113">StringAndDirectoryParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6286-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6286-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6286-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6286-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6286-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6286-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6286-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6286-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6286-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6286-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6286-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6286-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6286-119">DESCRIPTION</span></span>
<span data-ttu-id="f6286-120">In regelmäßigen Abständen überprüft Azure File Sync den -Namespace in einer synchronisierenden Azure-Dateifreigabe auf Änderungen, die auf anderem Wegen als der Synchronisierung in die Dateifreigabe einfingen. Ziel ist es, diese Änderungen zu identifizieren und schließlich mit verbundenen Servern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="f6286-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="f6286-121">Dieser Befehl kann verwendet werden, um die Erkennung von Namespaceänderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="f6286-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="f6286-122">Sie kann auf die gesamte Freigabe, den Unterordner oder die gesamte Gruppe von Dateien ausgerichtet sein.</span><span class="sxs-lookup"><span data-stu-id="f6286-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="f6286-123">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb des Grenzwerts von 10.000 Elementen abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f6286-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="f6286-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6286-124">EXAMPLES</span></span>

### <span data-ttu-id="f6286-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6286-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="f6286-126">In diesem Beispiel wird die Änderungserkennung in den Verzeichnissen "Daten" und "Reporting\Templates" einer synchronisierenden Azure-Dateifreigabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6286-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="f6286-127">Alle Pfade sind relativ zum Stamm des Azure-Dateifreigabenamespaces.</span><span class="sxs-lookup"><span data-stu-id="f6286-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="f6286-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6286-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="f6286-129">In diesem Beispiel wird die Änderungserkennung für eine Reihe von Dateien ausgeführt, die dem Befehlsaufrufer als geändert bekannt sind.</span><span class="sxs-lookup"><span data-stu-id="f6286-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="f6286-130">Ziel ist es, dass die Azure-Dateisynchronisierung auch diese Änderungen erkennt und synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f6286-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="f6286-131">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f6286-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="f6286-132">In diesem Beispiel wird die Änderungserkennung für das Verzeichnis "Beispiele" ausgeführt und erkennt Rekursiv Änderungen in Unterverzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="f6286-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="f6286-133">Denken Sie daran, dass das Cmdlet fehlschlägt, wenn der Pfad mehr als 10.000 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="f6286-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="f6286-134">Wenn der Pfad mehr als 10.000 Elemente enthält, führen Sie den Befehl für Unterteile des Namespaces aus.</span><span class="sxs-lookup"><span data-stu-id="f6286-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="f6286-135">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6286-135">PARAMETERS</span></span>

### <span data-ttu-id="f6286-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6286-136">-AsJob</span></span>
<span data-ttu-id="f6286-137">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f6286-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6286-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6286-138">-DefaultProfile</span></span>
<span data-ttu-id="f6286-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6286-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6286-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="f6286-140">-DirectoryPath</span></span>
<span data-ttu-id="f6286-141">Verzeichnis, in dem die Änderungserkennung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-141">Directory where change detection will be performed.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f6286-142">-InputObject</span></span>
<span data-ttu-id="f6286-143">CloudEndpoint-Objekt, das normalerweise über den -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: ObjectAndDirectoryParameterSet, ObjectAndPathParameterSet
Aliases: CloudEndpoint

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-144">-Name</span><span class="sxs-lookup"><span data-stu-id="f6286-144">-Name</span></span>
<span data-ttu-id="f6286-145">Name des CloudEndpoints.</span><span class="sxs-lookup"><span data-stu-id="f6286-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="f6286-146">Der Name ist eine GUID und nicht der Anzeigename, der im Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="f6286-147">Um den CloudEndpointName zu erhalten, verwenden Sie das Get-AzStorageSyncCloudEndpoint Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f6286-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6286-148">-PassThru</span></span>
<span data-ttu-id="f6286-149">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="f6286-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="f6286-150">Wenn Sie den Parameter PassThru angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="f6286-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="f6286-151">-Path</span><span class="sxs-lookup"><span data-stu-id="f6286-151">-Path</span></span>
<span data-ttu-id="f6286-152">Pfad, in dem die Änderungserkennung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-152">Path where change detection will be performed.</span></span>

```yaml
Type: System.String[]
Parameter Sets: StringAndPathParameterSet, ResourceIdAndPathParameterSet, ObjectAndPathParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-153">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="f6286-153">-Recursive</span></span>
<span data-ttu-id="f6286-154">Geben Sie an, ob die Verzeichnisänderungserkennung rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="f6286-154">Indication whether directory change detection is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: StringAndDirectoryParameterSet, ResourceIdAndDirectoryParameterSet, ObjectAndDirectoryParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6286-155">-ResourceGroupName</span></span>
<span data-ttu-id="f6286-156">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="f6286-156">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6286-157">-ResourceId</span></span>
<span data-ttu-id="f6286-158">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="f6286-158">CloudEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdAndDirectoryParameterSet, ResourceIdAndPathParameterSet
Aliases: CloudEndpointId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="f6286-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="f6286-160">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="f6286-160">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="f6286-161">-SyncGroupName</span></span>
<span data-ttu-id="f6286-162">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="f6286-162">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringAndDirectoryParameterSet, StringAndPathParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6286-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6286-163">-Confirm</span></span>
<span data-ttu-id="f6286-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6286-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6286-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6286-165">-WhatIf</span></span>
<span data-ttu-id="f6286-166">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6286-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6286-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6286-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6286-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6286-168">CommonParameters</span></span>
<span data-ttu-id="f6286-169">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6286-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6286-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6286-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6286-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6286-171">INPUTS</span></span>

### <span data-ttu-id="f6286-172">System.String</span><span class="sxs-lookup"><span data-stu-id="f6286-172">System.String</span></span>

### <span data-ttu-id="f6286-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="f6286-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="f6286-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6286-174">OUTPUTS</span></span>

### <span data-ttu-id="f6286-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="f6286-175">System.Void</span></span>

## <span data-ttu-id="f6286-176">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6286-176">NOTES</span></span>

## <span data-ttu-id="f6286-177">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6286-177">RELATED LINKS</span></span>
