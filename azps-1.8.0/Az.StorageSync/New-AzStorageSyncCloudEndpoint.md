---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 7a8c11bc4b24415e1baf826824596bc06e1fe99a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658700"
---
# <span data-ttu-id="d10c0-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d10c0-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="d10c0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d10c0-102">SYNOPSIS</span></span>
<span data-ttu-id="d10c0-103">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt in einer Synchronisierungsgruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d10c0-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="d10c0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d10c0-104">SYNTAX</span></span>

### <span data-ttu-id="d10c0-105">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="d10c0-105">ObjectParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d10c0-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d10c0-106">StringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d10c0-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d10c0-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d10c0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d10c0-108">DESCRIPTION</span></span>
<span data-ttu-id="d10c0-109">Mit diesem Befehl wird ein Azure-Datei Synchronisierungs Endpunkt erstellt.</span><span class="sxs-lookup"><span data-stu-id="d10c0-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="d10c0-110">Ein Cloud-Endpunkt ist ein Verweis auf eine vorhandene Azure-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="d10c0-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="d10c0-111">Sie stellt die Dateifreigabe dar und definiert die Teilnahme an der Synchronisierung aller Dateien, die Teil der Synchronisierungsgruppe sind, in der der Cloud-Endpunkt erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="d10c0-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="d10c0-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d10c0-112">EXAMPLES</span></span>

### <span data-ttu-id="d10c0-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d10c0-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="d10c0-114">Ein Cloud-Endpunkt ist ein integraler Bestandteileiner Synchronisierungsgruppe, dies ist ein Beispiel für das Erstellen eines innerhalb einer vorhandenen Synchronisierungsgruppe mit dem Namen "mySyncGroupName".</span><span class="sxs-lookup"><span data-stu-id="d10c0-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="d10c0-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d10c0-115">PARAMETERS</span></span>

### <span data-ttu-id="d10c0-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d10c0-116">-AsJob</span></span>
<span data-ttu-id="d10c0-117">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d10c0-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d10c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d10c0-118">-DefaultProfile</span></span>
<span data-ttu-id="d10c0-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d10c0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d10c0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="d10c0-120">-Name</span></span>
<span data-ttu-id="d10c0-121">Der Name des Cloud-Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="d10c0-121">Name of the cloud endpoint.</span></span> <span data-ttu-id="d10c0-122">Beim Erstellen über das Azure-Portal wird Name auf den Namen der Azure-Dateifreigabe, auf die verwiesen wird, gesetzt.</span><span class="sxs-lookup"><span data-stu-id="d10c0-122">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="d10c0-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d10c0-123">-ParentObject</span></span>
<span data-ttu-id="d10c0-124">SyncGroup-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="d10c0-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="d10c0-125">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d10c0-125">-ParentResourceId</span></span>
<span data-ttu-id="d10c0-126">SyncGroup übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d10c0-126">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="d10c0-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d10c0-127">-ResourceGroupName</span></span>
<span data-ttu-id="d10c0-128">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d10c0-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="d10c0-129">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="d10c0-129">-StorageAccountResourceId</span></span>
<span data-ttu-id="d10c0-130">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="d10c0-130">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="d10c0-131">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="d10c0-131">-AzureFileShareName</span></span>
<span data-ttu-id="d10c0-132">Speicherkonto Freigabename (Azure File Freigabename)</span><span class="sxs-lookup"><span data-stu-id="d10c0-132">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="d10c0-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="d10c0-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="d10c0-134">Mandanten-ID des speicherkontos (Unternehmensverzeichnis-ID)</span><span class="sxs-lookup"><span data-stu-id="d10c0-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="d10c0-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d10c0-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="d10c0-136">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d10c0-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d10c0-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d10c0-137">-SyncGroupName</span></span>
<span data-ttu-id="d10c0-138">Der Name des SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="d10c0-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d10c0-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d10c0-139">-Confirm</span></span>
<span data-ttu-id="d10c0-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d10c0-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d10c0-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d10c0-141">-WhatIf</span></span>
<span data-ttu-id="d10c0-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d10c0-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d10c0-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d10c0-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d10c0-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d10c0-144">CommonParameters</span></span>
<span data-ttu-id="d10c0-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d10c0-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d10c0-146">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d10c0-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d10c0-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d10c0-147">INPUTS</span></span>

### <span data-ttu-id="d10c0-148">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="d10c0-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="d10c0-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d10c0-149">System.String</span></span>

## <span data-ttu-id="d10c0-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d10c0-150">OUTPUTS</span></span>

### <span data-ttu-id="d10c0-151">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="d10c0-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="d10c0-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="d10c0-152">NOTES</span></span>

## <span data-ttu-id="d10c0-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d10c0-153">RELATED LINKS</span></span>
