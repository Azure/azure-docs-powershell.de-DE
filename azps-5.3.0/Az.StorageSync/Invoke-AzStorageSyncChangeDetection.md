---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: 9b7c539074f38b730a8ab5cd767a62fb44216ef6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460135"
---
# <span data-ttu-id="0485e-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="0485e-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="0485e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0485e-102">SYNOPSIS</span></span>
<span data-ttu-id="0485e-103">Mit diesem Befehl kann die Erkennung von Namespaceänderungen manuell initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="0485e-104">Es kann auf die gesamte Freigabe, den Unterordner oder eine Gruppe von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="0485e-105">Es können maximal 10.000 Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="0485e-106">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespace, damit die Änderungserkennung schnell und innerhalb des Grenzwerts von 10.000 Elemente abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0485e-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="0485e-107">Das Invoke-AzStorageSyncChangeDetection erkennt die folgenden Änderungen in der Azure-Dateifreigabe nicht:</span><span class="sxs-lookup"><span data-stu-id="0485e-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="0485e-108">Gelöschte Dateien.</span><span class="sxs-lookup"><span data-stu-id="0485e-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="0485e-109">Dateien, die aus der Freigabe verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="0485e-110">Dateien, die gelöscht und unter demselben Namen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0485e-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="0485e-111">Diese Änderungen werden erkannt, wenn der [Änderungserkennungsauftrag ausgeführt](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) wird.</span><span class="sxs-lookup"><span data-stu-id="0485e-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs-change-detection) runs.</span></span>

## <span data-ttu-id="0485e-112">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0485e-112">SYNTAX</span></span>

### <span data-ttu-id="0485e-113">StringAndDirectoryParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0485e-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0485e-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="0485e-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0485e-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="0485e-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0485e-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="0485e-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0485e-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="0485e-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0485e-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="0485e-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0485e-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0485e-119">DESCRIPTION</span></span>
<span data-ttu-id="0485e-120">In regelmäßigen Abständen überprüft die Azure File Sync den Namespace in einer synchronisierenden Azure-Dateifreigabe auf Änderungen, die über die Synchronisierung in der Dateifreigabe vorgenommen wurden. Das Ziel besteht in der Identifizierung dieser Änderungen und schließlich deren Synchronisierung mit verbundenen Servern.</span><span class="sxs-lookup"><span data-stu-id="0485e-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="0485e-121">Mit diesem Befehl kann die Erkennung von Namespaceänderungen manuell initiiert werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="0485e-122">Es kann auf die gesamte Freigabe, den Unterordner oder eine Gruppe von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="0485e-123">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespace, damit die Änderungserkennung schnell und innerhalb des Grenzwerts von 10.000 Elementen abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="0485e-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="0485e-124">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0485e-124">EXAMPLES</span></span>

### <span data-ttu-id="0485e-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0485e-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="0485e-126">In diesem Beispiel wird die Änderungserkennung in den Verzeichnissen "Daten" und "Reporting\Templates" einer synchronisierenden Azure-Dateifreigabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0485e-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="0485e-127">Alle Pfade sind relativ zum Stamm des Azure-Dateifreigabe-Namespace.</span><span class="sxs-lookup"><span data-stu-id="0485e-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="0485e-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0485e-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="0485e-129">In diesem Beispiel wird die Änderungserkennung für eine Reihe von Dateien ausgeführt, deren Änderung dem Befehlsaufrufer bekannt ist.</span><span class="sxs-lookup"><span data-stu-id="0485e-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="0485e-130">Das Ziel besteht in der Erkennung und Synchronisierung dieser Änderungen durch die Azure-Dateisynchronisierung.</span><span class="sxs-lookup"><span data-stu-id="0485e-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="0485e-131">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0485e-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="0485e-132">In diesem Beispiel wird die Änderungserkennung für das Verzeichnis "Beispiele" ausgeführt und erkennt rekursiv Änderungen in Unterverzeichnissen.</span><span class="sxs-lookup"><span data-stu-id="0485e-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="0485e-133">Beachten Sie, dass das Cmdlet fehlschlägt, wenn der Pfad mehr als 10.000 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="0485e-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="0485e-134">Wenn der Pfad mehr als 10.000 Elemente enthält, führen Sie den Befehl für Unterteile des Namespace aus.</span><span class="sxs-lookup"><span data-stu-id="0485e-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="0485e-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0485e-135">PARAMETERS</span></span>

### <span data-ttu-id="0485e-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0485e-136">-AsJob</span></span>
<span data-ttu-id="0485e-137">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="0485e-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0485e-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0485e-138">-DefaultProfile</span></span>
<span data-ttu-id="0485e-139">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0485e-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0485e-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="0485e-140">-DirectoryPath</span></span>
<span data-ttu-id="0485e-141">Verzeichnis, in dem die Änderungserkennung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0485e-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="0485e-142">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0485e-142">-InputObject</span></span>
<span data-ttu-id="0485e-143">CloudEndpoint-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="0485e-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="0485e-144">-Name</span><span class="sxs-lookup"><span data-stu-id="0485e-144">-Name</span></span>
<span data-ttu-id="0485e-145">Der Name von CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="0485e-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="0485e-146">Der Name ist eine GUID, nicht der Anzeigename im Portal.</span><span class="sxs-lookup"><span data-stu-id="0485e-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="0485e-147">Verwenden Sie das cmdlet "CloudEndpointName", Get-AzStorageSyncCloudEndpoint CloudEndpointName.</span><span class="sxs-lookup"><span data-stu-id="0485e-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="0485e-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0485e-148">-PassThru</span></span>
<span data-ttu-id="0485e-149">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="0485e-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="0485e-150">Wenn Sie den Parameter "PassThru" angeben, schreibt das Cmdlet nach erfolgreicher Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="0485e-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="0485e-151">-Path</span><span class="sxs-lookup"><span data-stu-id="0485e-151">-Path</span></span>
<span data-ttu-id="0485e-152">Pfad, in dem die Änderungserkennung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0485e-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="0485e-153">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="0485e-153">-Recursive</span></span>
<span data-ttu-id="0485e-154">Geben Sie an, ob die Verzeichnisänderungserkennung rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="0485e-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="0485e-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0485e-155">-ResourceGroupName</span></span>
<span data-ttu-id="0485e-156">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="0485e-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="0485e-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0485e-157">-ResourceId</span></span>
<span data-ttu-id="0485e-158">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0485e-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="0485e-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="0485e-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="0485e-160">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="0485e-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="0485e-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="0485e-161">-SyncGroupName</span></span>
<span data-ttu-id="0485e-162">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="0485e-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="0485e-163">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0485e-163">-Confirm</span></span>
<span data-ttu-id="0485e-164">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0485e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0485e-165">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="0485e-165">-WhatIf</span></span>
<span data-ttu-id="0485e-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0485e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0485e-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0485e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0485e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0485e-168">CommonParameters</span></span>
<span data-ttu-id="0485e-169">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0485e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0485e-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0485e-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0485e-171">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0485e-171">INPUTS</span></span>

### <span data-ttu-id="0485e-172">System.String</span><span class="sxs-lookup"><span data-stu-id="0485e-172">System.String</span></span>

### <span data-ttu-id="0485e-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="0485e-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="0485e-174">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0485e-174">OUTPUTS</span></span>

### <span data-ttu-id="0485e-175">System.Void</span><span class="sxs-lookup"><span data-stu-id="0485e-175">System.Void</span></span>

## <span data-ttu-id="0485e-176">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="0485e-176">NOTES</span></span>

## <span data-ttu-id="0485e-177">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="0485e-177">RELATED LINKS</span></span>
