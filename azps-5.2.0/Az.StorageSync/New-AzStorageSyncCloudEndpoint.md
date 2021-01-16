---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366679"
---
# <span data-ttu-id="02ccd-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="02ccd-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="02ccd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02ccd-102">SYNOPSIS</span></span>
<span data-ttu-id="02ccd-103">Mit diesem Befehl wird ein Azure File Sync-Cloudendpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="02ccd-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="02ccd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="02ccd-104">SYNTAX</span></span>

### <span data-ttu-id="02ccd-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02ccd-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02ccd-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ccd-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02ccd-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="02ccd-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02ccd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02ccd-108">DESCRIPTION</span></span>
<span data-ttu-id="02ccd-109">Mit diesem Befehl wird ein Azure File Sync-Cloudendpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="02ccd-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="02ccd-110">Ein Cloudendpunkt ist ein Verweis auf eine vorhandene Azure-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="02ccd-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="02ccd-111">Sie stellt die Dateifreigabe dar und definiert ihre Teilnahme an der Synchronisierung aller Dateien, die Teil der Synchronisierungsgruppe sind, in der der Cloudendpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="02ccd-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="02ccd-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="02ccd-112">EXAMPLES</span></span>

### <span data-ttu-id="02ccd-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02ccd-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="02ccd-114">Ein Cloudendpunkt ist ein integrales Mitglied einer Synchronisierungsgruppe. Dies ist ein Beispiel für die Erstellung eines Endpunkts innerhalb einer vorhandenen Synchronisierungsgruppe mit dem Namen "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="02ccd-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="02ccd-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02ccd-115">PARAMETERS</span></span>

### <span data-ttu-id="02ccd-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02ccd-116">-AsJob</span></span>
<span data-ttu-id="02ccd-117">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="02ccd-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02ccd-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="02ccd-118">-AzureFileShareName</span></span>
<span data-ttu-id="02ccd-119">Freigabename des Speicherkontos (Azure-Dateifreigabename)</span><span class="sxs-lookup"><span data-stu-id="02ccd-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02ccd-120">-DefaultProfile</span></span>
<span data-ttu-id="02ccd-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="02ccd-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02ccd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="02ccd-122">-Name</span></span>
<span data-ttu-id="02ccd-123">Name des Cloudendpunkts.</span><span class="sxs-lookup"><span data-stu-id="02ccd-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="02ccd-124">Wenn er über das Azure-Portal erstellt wird, wird "Name" auf den Namen der Azure-Dateifreigabe festgelegt, auf die verweisen wird.</span><span class="sxs-lookup"><span data-stu-id="02ccd-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02ccd-125">-ParentObject</span></span>
<span data-ttu-id="02ccd-126">SyncGroup-Objekt, das normalerweise über den Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="02ccd-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="02ccd-127">-ParentResourceId</span></span>
<span data-ttu-id="02ccd-128">Übergeordnete Ressourcen-ID der Synchronisierungsgruppe</span><span class="sxs-lookup"><span data-stu-id="02ccd-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02ccd-129">-ResourceGroupName</span></span>
<span data-ttu-id="02ccd-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="02ccd-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="02ccd-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="02ccd-132">Ressourcen-ID des Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="02ccd-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="02ccd-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="02ccd-134">Mandanten-ID des Speicherkontos (Firmenverzeichnis-ID)</span><span class="sxs-lookup"><span data-stu-id="02ccd-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="02ccd-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="02ccd-136">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="02ccd-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="02ccd-137">-SyncGroupName</span></span>
<span data-ttu-id="02ccd-138">Name der Synchronisierungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="02ccd-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02ccd-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02ccd-139">-Confirm</span></span>
<span data-ttu-id="02ccd-140">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02ccd-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02ccd-141">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="02ccd-141">-WhatIf</span></span>
<span data-ttu-id="02ccd-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02ccd-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02ccd-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02ccd-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02ccd-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02ccd-144">CommonParameters</span></span>
<span data-ttu-id="02ccd-145">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02ccd-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02ccd-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02ccd-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02ccd-147">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="02ccd-147">INPUTS</span></span>

### <span data-ttu-id="02ccd-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="02ccd-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="02ccd-149">System.String</span><span class="sxs-lookup"><span data-stu-id="02ccd-149">System.String</span></span>

## <span data-ttu-id="02ccd-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="02ccd-150">OUTPUTS</span></span>

### <span data-ttu-id="02ccd-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="02ccd-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="02ccd-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="02ccd-152">NOTES</span></span>

## <span data-ttu-id="02ccd-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="02ccd-153">RELATED LINKS</span></span>
