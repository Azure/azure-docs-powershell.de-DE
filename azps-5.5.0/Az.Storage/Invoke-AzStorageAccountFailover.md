---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165721"
---
# <span data-ttu-id="de44b-101">Invoke-AzStorageAccountFailover</span><span class="sxs-lookup"><span data-stu-id="de44b-101">Invoke-AzStorageAccountFailover</span></span>

## <span data-ttu-id="de44b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de44b-102">SYNOPSIS</span></span>
<span data-ttu-id="de44b-103">Ruft den Failover eines Speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="de44b-103">Invokes failover of a Storage account.</span></span>

## <span data-ttu-id="de44b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="de44b-104">SYNTAX</span></span>

### <span data-ttu-id="de44b-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="de44b-105">AccountName (Default)</span></span>
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="de44b-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="de44b-106">AccountObject</span></span>
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="de44b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="de44b-107">DESCRIPTION</span></span>
<span data-ttu-id="de44b-108">Ruft den Failover eines Speicherkontos auf.</span><span class="sxs-lookup"><span data-stu-id="de44b-108">Invokes failover of a Storage account.</span></span> <span data-ttu-id="de44b-109">Bei Verfügbarkeitsproblemen kann eine Failoveranforderung für ein Speicherkonto ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="de44b-109">Failover request can be triggered for a storage account in case of availability issues.</span></span> <span data-ttu-id="de44b-110">Der Failover erfolgt vom primären Cluster des Speicherkontos zum sekundären Cluster für RA-GRS-Konten.</span><span class="sxs-lookup"><span data-stu-id="de44b-110">The failover occurs from the storage account's primary cluster to secondary cluster for RA-GRS accounts.</span></span> <span data-ttu-id="de44b-111">Der sekundäre Cluster wird nach dem Failover primär.</span><span class="sxs-lookup"><span data-stu-id="de44b-111">The secondary cluster will become primary after failover.</span></span>
<span data-ttu-id="de44b-112">Bitte beachten Sie die folgenden Auswirkungen auf Ihr Speicherkonto, bevor Sie den Failover starten: 1.1.</span><span class="sxs-lookup"><span data-stu-id="de44b-112">Please understand the following impact to your storage account before you initiate the failover: 1.1.</span></span> <span data-ttu-id="de44b-113">Überprüfen Sie die Letzte Synchronisierungszeit mit GET BLOB Service Stats ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , GET Table Service Stats ( und GET Queue Service Stats ( für Ihr https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) Konto).</span><span class="sxs-lookup"><span data-stu-id="de44b-113">Please check the Last Sync Time using GET Blob Service Stats (https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats), GET Table Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) and GET Queue Service Stats (https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) for your account.</span></span> <span data-ttu-id="de44b-114">Dies sind die Daten, die verloren gehen können, wenn Sie den Failover initiieren.</span><span class="sxs-lookup"><span data-stu-id="de44b-114">This is the data you may lose if you initiate the failover.</span></span>
<span data-ttu-id="de44b-115">2. Nach dem Failover wird der Speicherkontotyp in einen lokal redundanten Speicher (LRS) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="de44b-115">2.After the failover, your storage account type will be converted to locally redundant storage(LRS).</span></span> <span data-ttu-id="de44b-116">Sie können Ihr Konto so konvertieren, dass georedundanter Speicher (Geo redundant Storage, GRS) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="de44b-116">You can convert your account to use geo-redundant storage(GRS).</span></span>
<span data-ttu-id="de44b-117">3. Sobald Sie GRS für Ihr Speicherkonto erneut aktivieren, repliziert Microsoft Daten in die neue sekundäre Region.</span><span class="sxs-lookup"><span data-stu-id="de44b-117">3.Once you re-enable GRS for your storage account, Microsoft will replicate data to your new secondary region.</span></span> <span data-ttu-id="de44b-118">Die Replikationszeit hängt von der Menge der zu replizierenden Daten ab.</span><span class="sxs-lookup"><span data-stu-id="de44b-118">Replication time is dependent on the amount of data to replicate.</span></span> <span data-ttu-id="de44b-119">Beachten Sie, dass für das Bootstrap Bandbreitengebühren anfallen.</span><span class="sxs-lookup"><span data-stu-id="de44b-119">Please note that there are bandwidth charges for the bootstrap.</span></span> <span data-ttu-id="de44b-120"> https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span><span class="sxs-lookup"><span data-stu-id="de44b-120">https://azure.microsoft.com/en-us/pricing/details/bandwidth/</span></span>

## <span data-ttu-id="de44b-121">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="de44b-121">EXAMPLES</span></span>

### <span data-ttu-id="de44b-122">Beispiel 1: Aufrufen des Failover eines Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="de44b-122">Example 1: Invoke failover of a Storage account</span></span>
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

<span data-ttu-id="de44b-123">Dieser Befehl überprüft die letzte Synchronisierungszeit eines Speicherkontos und ruft dann den Failover des Kontos auf. Der sekundäre Cluster wird nach dem Failover primär.</span><span class="sxs-lookup"><span data-stu-id="de44b-123">This command check the last sync time of a Storage account then invokes failover of it, the secondary cluster will become primary after failover.</span></span> <span data-ttu-id="de44b-124">Da failover eine lange Zeit dauert, empfehlen Sie, ihn im Back-End mit dem Parameter "-Asjob" auszuführen, und warten Sie dann, bis der Auftrag abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="de44b-124">Since failover takes a long time, suggest to run it in the backend with -Asjob parameter, and then wait for the job complete.</span></span>

## <span data-ttu-id="de44b-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de44b-125">PARAMETERS</span></span>

### <span data-ttu-id="de44b-126">-AsJob</span><span class="sxs-lookup"><span data-stu-id="de44b-126">-AsJob</span></span>
<span data-ttu-id="de44b-127">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="de44b-127">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="de44b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de44b-128">-DefaultProfile</span></span>
<span data-ttu-id="de44b-129">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="de44b-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de44b-130">-Force</span><span class="sxs-lookup"><span data-stu-id="de44b-130">-Force</span></span>
<span data-ttu-id="de44b-131">Erzwingen des Failovers des Kontos</span><span class="sxs-lookup"><span data-stu-id="de44b-131">Force to Failover the Account</span></span>

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

### <span data-ttu-id="de44b-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="de44b-132">-InputObject</span></span>
<span data-ttu-id="de44b-133">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="de44b-133">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="de44b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="de44b-134">-Name</span></span>
<span data-ttu-id="de44b-135">Name des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="de44b-135">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de44b-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de44b-136">-ResourceGroupName</span></span>
<span data-ttu-id="de44b-137">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="de44b-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="de44b-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="de44b-138">-Confirm</span></span>
<span data-ttu-id="de44b-139">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="de44b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="de44b-140">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="de44b-140">-WhatIf</span></span>
<span data-ttu-id="de44b-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="de44b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="de44b-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="de44b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="de44b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de44b-143">CommonParameters</span></span>
<span data-ttu-id="de44b-144">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de44b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de44b-145">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de44b-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de44b-146">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="de44b-146">INPUTS</span></span>

### <span data-ttu-id="de44b-147">System.String</span><span class="sxs-lookup"><span data-stu-id="de44b-147">System.String</span></span>

## <span data-ttu-id="de44b-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="de44b-148">OUTPUTS</span></span>

### <span data-ttu-id="de44b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="de44b-149">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="de44b-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="de44b-150">NOTES</span></span>

## <span data-ttu-id="de44b-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="de44b-151">RELATED LINKS</span></span>
