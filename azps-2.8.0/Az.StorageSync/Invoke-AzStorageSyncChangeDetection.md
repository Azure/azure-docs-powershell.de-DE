---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/invoke-azstoragesyncchangedetection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Invoke-AzStorageSyncChangeDetection.md
ms.openlocfilehash: c266b6623463165f14e01e55f0fec4d2d59a581f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826920"
---
# <span data-ttu-id="215df-101">Invoke-AzStorageSyncChangeDetection</span><span class="sxs-lookup"><span data-stu-id="215df-101">Invoke-AzStorageSyncChangeDetection</span></span>

## <span data-ttu-id="215df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="215df-102">SYNOPSIS</span></span>
<span data-ttu-id="215df-103">Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="215df-103">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="215df-104">Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="215df-104">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="215df-105">Es können maximal 10.000 Änderungen erkannt werden.</span><span class="sxs-lookup"><span data-stu-id="215df-105">A maximum of 10,000 changes can be detected.</span></span> <span data-ttu-id="215df-106">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb einer 10.000-Änderungs Grenze abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="215df-106">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="215df-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="215df-107">SYNTAX</span></span>

### <span data-ttu-id="215df-108">StringAndDirectoryParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="215df-108">StringAndDirectoryParameterSet (Default)</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -DirectoryPath <String> [-Recursive] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215df-109">StringAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="215df-109">StringAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215df-110">ResourceIdAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="215df-110">ResourceIdAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -DirectoryPath <String> [-Recursive] [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215df-111">ResourceIdAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="215df-111">ResourceIdAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-ResourceId] <String> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215df-112">ObjectAndDirectoryParameterSet</span><span class="sxs-lookup"><span data-stu-id="215df-112">ObjectAndDirectoryParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -DirectoryPath <String> [-Recursive]
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="215df-113">ObjectAndPathParameterSet</span><span class="sxs-lookup"><span data-stu-id="215df-113">ObjectAndPathParameterSet</span></span>
```
Invoke-AzStorageSyncChangeDetection [-InputObject] <PSCloudEndpoint> -Path <String[]> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="215df-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="215df-114">DESCRIPTION</span></span>
<span data-ttu-id="215df-115">In regelmäßigen Abständen überprüft die Azure-Dateisynchronisierung den Namespace innerhalb einer Synchronisierungs Azure-Dateifreigabe auf Änderungen, die auf andere Weise als die Synchronisierung in die Dateifreigabe eingegangen sind. Das Ziel besteht darin, diese Änderungen zu identifizieren und Sie letztendlich mit verbundenen Servern zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="215df-115">Periodically, Azure File Sync checks the namespace inside a syncing Azure file share for changes that came into the file share by other means than sync. The goal is to identify these changes and ultimately sync them to connected servers.</span></span> <span data-ttu-id="215df-116">Dieser Befehl kann verwendet werden, um das Erkennen von Namespaces-Änderungen manuell zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="215df-116">This command can be used to manually initiate the detection of namespaces changes.</span></span> <span data-ttu-id="215df-117">Sie kann auf die gesamte Freigabe, den Unterordner oder den Satz von Dateien ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="215df-117">It can be targeted to the entire share, subfolder or set of files.</span></span> <span data-ttu-id="215df-118">Wenn Ihnen der Umfang der Änderungen bekannt ist, beschränken Sie die Ausführung dieses Befehls auf Teile des Namespaces, damit die Änderungserkennung schnell und innerhalb einer 10.000-Änderungs Grenze abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="215df-118">If the scope of changes is known to you, limit the execution of this command to parts of the namespace, so change detection can finish quickly and within a 10,000 changes limit.</span></span>

## <span data-ttu-id="215df-119">Beispiele</span><span class="sxs-lookup"><span data-stu-id="215df-119">EXAMPLES</span></span>

### <span data-ttu-id="215df-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="215df-120">Example 1</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data","Reporting\Templates"
```

<span data-ttu-id="215df-121">In diesem Beispiel wird die Änderungserkennung in den Verzeichnissen "Data" und "Reporting\Templates" einer synchronisierten Azure-Dateifreigabe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="215df-121">In this example, change detection is run in the "Data" and "Reporting\Templates" directories of a syncing Azure file share.</span></span> <span data-ttu-id="215df-122">Alle Pfade sind relativ zum Stamm des Azure File Share-Namespace.</span><span class="sxs-lookup"><span data-stu-id="215df-122">All paths are relative to the root of the Azure file share namespace.</span></span>

### <span data-ttu-id="215df-123">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="215df-123">Example 2</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -Path "Data\results.xslx","Reporting\Templates\generated.pptx"
```

<span data-ttu-id="215df-124">In diesem Beispiel wird die Änderungserkennung für eine Reihe von Dateien ausgeführt, die dem Befehls Aufrufer bekannt sind, dass Sie sich geändert haben.</span><span class="sxs-lookup"><span data-stu-id="215df-124">In this example, change detection is run for a set of files that are known to the command caller to have changed.</span></span> <span data-ttu-id="215df-125">Das Ziel besteht darin, diese Änderungen auch durch Azure-Dateisynchronisierung zu erkennen und zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="215df-125">The goal is to have Azure file sync detect and sync these changes as well.</span></span>

### <span data-ttu-id="215df-126">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="215df-126">Example 3</span></span>
```powershell
PS C:\> Invoke-AzStorageSyncChangeDetection -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -CloudEndpointName "myCloudEndpointName" -DirectoryPath "Examples" -Recursive
```

<span data-ttu-id="215df-127">In diesem Beispiel wird die Änderungserkennung für das Verzeichnis "examples" ausgeführt, und es werden Änderungen in Unterverzeichnissen rekursiv erkannt.</span><span class="sxs-lookup"><span data-stu-id="215df-127">In this example, change detection is run for the "Examples" directory and will recursively detect changes in subdirectories.</span></span> <span data-ttu-id="215df-128">Beachten Sie, dass dieser Befehl bis zu 10.000 Änderungen erkennen kann, bevor er automatisch abgebrochen wird.</span><span class="sxs-lookup"><span data-stu-id="215df-128">Keep in mind that this command can detect up to 10,000 changes before it is automatically aborted.</span></span> <span data-ttu-id="215df-129">Wenn Sie vermuten, dass mehr als 10.000 Änderungen aufgetreten sind, führen Sie den Befehl für Unterteile des Namespaces aus.</span><span class="sxs-lookup"><span data-stu-id="215df-129">If you suspect more than 10,000 changes to have occurred, run the command on sub-parts of the namespace.</span></span>

## <span data-ttu-id="215df-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="215df-130">PARAMETERS</span></span>

### <span data-ttu-id="215df-131">-AsJob</span><span class="sxs-lookup"><span data-stu-id="215df-131">-AsJob</span></span>
<span data-ttu-id="215df-132">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="215df-132">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="215df-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="215df-133">-DefaultProfile</span></span>
<span data-ttu-id="215df-134">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="215df-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="215df-135">-DirectoryPath</span><span class="sxs-lookup"><span data-stu-id="215df-135">-DirectoryPath</span></span>
<span data-ttu-id="215df-136">Verzeichnis, in dem die Änderungserkennung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215df-136">Directory where change detection will be performed.</span></span>

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

### <span data-ttu-id="215df-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="215df-137">-InputObject</span></span>
<span data-ttu-id="215df-138">CloudEndpoint-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="215df-138">CloudEndpoint Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="215df-139">-Name</span><span class="sxs-lookup"><span data-stu-id="215df-139">-Name</span></span>
<span data-ttu-id="215df-140">Der Name des CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="215df-140">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="215df-141">-PassThru</span><span class="sxs-lookup"><span data-stu-id="215df-141">-PassThru</span></span>
<span data-ttu-id="215df-142">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="215df-142">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="215df-143">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="215df-143">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="215df-144">-Path</span><span class="sxs-lookup"><span data-stu-id="215df-144">-Path</span></span>
<span data-ttu-id="215df-145">Pfad, in dem die Änderungserkennung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215df-145">Path where change detection will be performed.</span></span>

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

### <span data-ttu-id="215df-146">-Rekursiv</span><span class="sxs-lookup"><span data-stu-id="215df-146">-Recursive</span></span>
<span data-ttu-id="215df-147">Gibt an, ob die Verzeichnis Änderungserkennung rekursiv ist.</span><span class="sxs-lookup"><span data-stu-id="215df-147">Indication whether directory change detection is recursive.</span></span>

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

### <span data-ttu-id="215df-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="215df-148">-ResourceGroupName</span></span>
<span data-ttu-id="215df-149">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="215df-149">Resource Group Name.</span></span>

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

### <span data-ttu-id="215df-150">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="215df-150">-ResourceId</span></span>
<span data-ttu-id="215df-151">CloudEndpoint-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="215df-151">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="215df-152">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="215df-152">-StorageSyncServiceName</span></span>
<span data-ttu-id="215df-153">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="215df-153">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="215df-154">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="215df-154">-SyncGroupName</span></span>
<span data-ttu-id="215df-155">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="215df-155">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="215df-156">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="215df-156">-Confirm</span></span>
<span data-ttu-id="215df-157">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="215df-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="215df-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="215df-158">-WhatIf</span></span>
<span data-ttu-id="215df-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="215df-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="215df-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="215df-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="215df-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="215df-161">CommonParameters</span></span>
<span data-ttu-id="215df-162">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="215df-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="215df-163">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="215df-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="215df-164">Eingaben</span><span class="sxs-lookup"><span data-stu-id="215df-164">INPUTS</span></span>

### <span data-ttu-id="215df-165">System. String</span><span class="sxs-lookup"><span data-stu-id="215df-165">System.String</span></span>

### <span data-ttu-id="215df-166">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="215df-166">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="215df-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="215df-167">OUTPUTS</span></span>

### <span data-ttu-id="215df-168">System. void</span><span class="sxs-lookup"><span data-stu-id="215df-168">System.Void</span></span>

## <span data-ttu-id="215df-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="215df-169">NOTES</span></span>

## <span data-ttu-id="215df-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="215df-170">RELATED LINKS</span></span>
