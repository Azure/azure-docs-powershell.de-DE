---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003335"
---
# <span data-ttu-id="170e3-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="170e3-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="170e3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="170e3-102">SYNOPSIS</span></span>
<span data-ttu-id="170e3-103">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="170e3-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="170e3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="170e3-104">SYNTAX</span></span>

### <span data-ttu-id="170e3-105">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="170e3-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="170e3-106">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="170e3-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="170e3-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="170e3-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="170e3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="170e3-108">DESCRIPTION</span></span>
<span data-ttu-id="170e3-109">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="170e3-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="170e3-110">Ein Cloud-Endpunkt ist ein Verweis auf eine vorhandene Azure-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="170e3-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="170e3-111">Sie stellt die Dateifreigabe dar und definiert die Teilnahme an der Synchronisierung aller Dateien, die Teil der Synchronisierungsgruppe sind, in der der Cloud-Endpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="170e3-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="170e3-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="170e3-112">EXAMPLES</span></span>

### <span data-ttu-id="170e3-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="170e3-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="170e3-114">Ein Cloud-Endpunkt ist ein integraler Bestandteileiner Synchronisierungsgruppe, dies ist ein Beispiel für das Erstellen eines innerhalb einer vorhandenen Synchronisierungsgruppe mit dem Namen "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="170e3-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="170e3-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="170e3-115">PARAMETERS</span></span>

### <span data-ttu-id="170e3-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="170e3-116">-AsJob</span></span>
<span data-ttu-id="170e3-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="170e3-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="170e3-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="170e3-118">-AzureFileShareName</span></span>
<span data-ttu-id="170e3-119">Speicherkonto Freigabename (Azure File Freigabename)</span><span class="sxs-lookup"><span data-stu-id="170e3-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="170e3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="170e3-120">-DefaultProfile</span></span>
<span data-ttu-id="170e3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="170e3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="170e3-122">-Name</span><span class="sxs-lookup"><span data-stu-id="170e3-122">-Name</span></span>
<span data-ttu-id="170e3-123">Der Name des Cloud-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="170e3-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="170e3-124">Beim Erstellen über das Azure-Portal wird Name auf den Namen der Azure-Dateifreigabe, auf die verwiesen wird, gesetzt.</span><span class="sxs-lookup"><span data-stu-id="170e3-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="170e3-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="170e3-125">-ParentObject</span></span>
<span data-ttu-id="170e3-126">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="170e3-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="170e3-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="170e3-127">-ParentResourceId</span></span>
<span data-ttu-id="170e3-128">SyncGroup übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="170e3-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="170e3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="170e3-129">-ResourceGroupName</span></span>
<span data-ttu-id="170e3-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="170e3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="170e3-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="170e3-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="170e3-132">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="170e3-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="170e3-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="170e3-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="170e3-134">Mandanten-ID des speicherkontos (Unternehmensverzeichnis-ID)</span><span class="sxs-lookup"><span data-stu-id="170e3-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="170e3-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="170e3-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="170e3-136">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="170e3-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="170e3-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="170e3-137">-SyncGroupName</span></span>
<span data-ttu-id="170e3-138">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="170e3-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="170e3-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="170e3-139">-Confirm</span></span>
<span data-ttu-id="170e3-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="170e3-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="170e3-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="170e3-141">-WhatIf</span></span>
<span data-ttu-id="170e3-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="170e3-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="170e3-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="170e3-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="170e3-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="170e3-144">CommonParameters</span></span>
<span data-ttu-id="170e3-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="170e3-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="170e3-146">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="170e3-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="170e3-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="170e3-147">INPUTS</span></span>

### <span data-ttu-id="170e3-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="170e3-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="170e3-149">System. String</span><span class="sxs-lookup"><span data-stu-id="170e3-149">System.String</span></span>

## <span data-ttu-id="170e3-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="170e3-150">OUTPUTS</span></span>

### <span data-ttu-id="170e3-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="170e3-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="170e3-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="170e3-152">NOTES</span></span>

## <span data-ttu-id="170e3-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="170e3-153">RELATED LINKS</span></span>
