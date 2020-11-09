---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: f76a399d9d2e592bbea10a9e304d8f6875eea227
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302917"
---
# <span data-ttu-id="6353b-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="6353b-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="6353b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6353b-102">SYNOPSIS</span></span>
<span data-ttu-id="6353b-103">Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="6353b-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="6353b-104">Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6353b-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="6353b-105">Es können maximal 10.000-Elemente erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="6353b-105">A maximum of 10,000 items can be detected.</span></span> <span data-ttu-id="6353b-106">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb des 10.000-Element Limits abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6353b-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 item limit.</span></span>

> [!Note]  
> <span data-ttu-id="6353b-107">Mit dem Invoke-AzStorageSyncChangeDetection-Cmdlet werden die folgenden Änderungen in der Azure-Dateifreigabe nicht erkannt:</span><span class="sxs-lookup"><span data-stu-id="6353b-107">The Invoke-AzStorageSyncChangeDetection cmdlet will not detect the following changes in the Azure file share:</span></span>
> - <span data-ttu-id="6353b-108">Dateien, die gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="6353b-108">Files that are deleted.</span></span> 
> - <span data-ttu-id="6353b-109">Dateien, die aus der Freigabe verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6353b-109">Files that are moved out of the share.</span></span>
> - <span data-ttu-id="6353b-110">Dateien, die gelöscht und mit demselben Namen erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="6353b-110">Files that are deleted and created with the same name.</span></span>  
> 
>  <span data-ttu-id="6353b-111">Diese Änderungen werden erkannt, wenn der [Änderungs erkennungsauftrag](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6353b-111">These changes will be detected when the [change detection job](https://docs.microsoft.com/azure/storage/files/storage-sync-files-troubleshoot?tabs=portal1%2Cazure-portal#afs->change-detection) runs.</span></span>

## <span data-ttu-id="6353b-112">Syntax</span><span class="sxs-lookup"><span data-stu-id="6353b-112">SYNTAX</span></span>

### <span data-ttu-id="6353b-113">StringAndDirectoryParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6353b-113">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6353b-114">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="6353b-114">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6353b-115">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="6353b-115">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6353b-116">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="6353b-116">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6353b-117">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="6353b-117">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6353b-118">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="6353b-118">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6353b-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6353b-119">DESCRIPTION</span></span>
<span data-ttu-id="6353b-120">In regelmäßigen Abständen überprüft die Azure-Dateisynchronisierung den Namespace innerhalb einer Synchronisierungs Azure-Dateifreigabe auf Änderungen, die auf andere Weise als die Synchronisierung in die Dateifreigabe eingegangen sind. Das Ziel besteht darin, diese Änderungen zu identifizieren und Sie letztendlich mit verbundenen Servern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6353b-120">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="6353b-121">Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="6353b-121">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="6353b-122">Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="6353b-122">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="6353b-123">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb der 10.000-Elementgrenze abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="6353b-123">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within the 10,000 items limit.</span></span>

## <span data-ttu-id="6353b-124">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6353b-124">EXAMPLES</span></span>

### <span data-ttu-id="6353b-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6353b-125">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="6353b-126">In diesem Beispiel wird die Änderungserkennung in den Verzeichnissen "Data" und "Reporting\Templates" einer synchronisierten Azure-Dateifreigabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6353b-126">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="6353b-127">Alle Pfade sind relativ zum Stamm des Azure File Share-Namespace.</span><span class="sxs-lookup"><span data-stu-id="6353b-127">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="6353b-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6353b-128">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="6353b-129">In diesem Beispiel wird die Änderungserkennung für eine Reihe von Dateien ausgeführt, die dem Befehls Aufrufer bekannt sind, dass Sie sich geändert haben.</span><span class="sxs-lookup"><span data-stu-id="6353b-129">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="6353b-130">Das Ziel besteht darin, diese Änderungen auch durch Azure-Dateisynchronisierung zu erkennen und zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="6353b-130">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="6353b-131">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="6353b-131">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "b38fc242-8100-4807-89d0-399cef5863bf" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="6353b-132">In diesem Beispiel wird die Änderungserkennung für das Verzeichnis "examples" ausgeführt, und es werden Änderungen in Unterverzeichnissen rekursiv erkannt.</span><span class="sxs-lookup"><span data-stu-id="6353b-132">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="6353b-133">Beachten Sie, dass das Cmdlet fehlerhaft ist, wenn der Pfad mehr als 10.000 Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="6353b-133">Keep in mind the cmdlet will fail if the path contains more than 10,000 items.</span></span> <span data-ttu-id="6353b-134">Wenn der Pfad mehr als 10.000 Elemente enthält, führen Sie den Befehl für Unterteile des Namespaces aus.</span><span class="sxs-lookup"><span data-stu-id="6353b-134">If the path contains more than 10,000 items, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="6353b-135">Parameter</span><span class="sxs-lookup"><span data-stu-id="6353b-135">PARAMETERS</span></span>

### <span data-ttu-id="6353b-136">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6353b-136">-AsJob</span></span>
<span data-ttu-id="6353b-137">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6353b-137">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6353b-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6353b-138">-DefaultProfile</span></span>
<span data-ttu-id="6353b-139">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6353b-139">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6353b-140">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="6353b-140">-DirectoryPath</span></span>
<span data-ttu-id="6353b-141">Verzeichnis, in dem die Änderungserkennung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6353b-141">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="6353b-142">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6353b-142">-InputObject</span></span>
<span data-ttu-id="6353b-143">CloudEndpoint-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="6353b-143">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="6353b-144">-Name</span><span class="sxs-lookup"><span data-stu-id="6353b-144">-Name</span></span>
<span data-ttu-id="6353b-145">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="6353b-145">Name of the CloudEndpoint.</span></span> <span data-ttu-id="6353b-146">Der Name ist eine GUID, nicht der Anzeigename, der im Portal angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="6353b-146">The name is a GUID, not the friendly name that's displayed in the portal.</span></span> <span data-ttu-id="6353b-147">Verwenden Sie zum Abrufen der CloudEndpointName das Get-AzStorageSyncCloudEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6353b-147">To get the CloudEndpointName, use the Get-AzStorageSyncCloudEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6353b-148">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6353b-148">-PassThru</span></span>
<span data-ttu-id="6353b-149">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="6353b-149">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="6353b-150">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6353b-150">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="6353b-151">-Path</span><span class="sxs-lookup"><span data-stu-id="6353b-151">-Path</span></span>
<span data-ttu-id="6353b-152">Pfad, in dem die Änderungserkennung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6353b-152">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="6353b-153">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="6353b-153">-Recursive</span></span>
<span data-ttu-id="6353b-154">Gibt an, ob die Verzeichnis Änderungserkennung rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="6353b-154">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="6353b-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6353b-155">-ResourceGroupName</span></span>
<span data-ttu-id="6353b-156">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6353b-156">Resource Group Name.</span></span>

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

### <span data-ttu-id="6353b-157">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6353b-157">-ResourceId</span></span>
<span data-ttu-id="6353b-158">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6353b-158">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="6353b-159">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="6353b-159">-StorageSyncServiceName</span></span>
<span data-ttu-id="6353b-160">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="6353b-160">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="6353b-161">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="6353b-161">-SyncGroupName</span></span>
<span data-ttu-id="6353b-162">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="6353b-162">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="6353b-163">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6353b-163">-Confirm</span></span>
<span data-ttu-id="6353b-164">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6353b-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6353b-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6353b-165">-WhatIf</span></span>
<span data-ttu-id="6353b-166">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6353b-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6353b-167">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6353b-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6353b-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6353b-168">CommonParameters</span></span>
<span data-ttu-id="6353b-169">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6353b-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6353b-170">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6353b-170">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6353b-171">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6353b-171">INPUTS</span></span>

### <span data-ttu-id="6353b-172">System. String</span><span class="sxs-lookup"><span data-stu-id="6353b-172">System.String</span></span>

### <span data-ttu-id="6353b-173">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6353b-173">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="6353b-174">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6353b-174">OUTPUTS</span></span>

### <span data-ttu-id="6353b-175">System. void</span><span class="sxs-lookup"><span data-stu-id="6353b-175">System.Void</span></span>

## <span data-ttu-id="6353b-176">Notizen</span><span class="sxs-lookup"><span data-stu-id="6353b-176">NOTES</span></span>

## <span data-ttu-id="6353b-177">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6353b-177">RELATED LINKS</span></span>
