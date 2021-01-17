---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472435"
---
# <span data-ttu-id="14e03-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="14e03-101">Update-AzImportExport</span></span>

## <span data-ttu-id="14e03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14e03-102">SYNOPSIS</span></span>
<span data-ttu-id="14e03-103">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="14e03-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="14e03-104">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, auf denen der Import- oder Exportauftrag ausgeführt wurde, an das Microsoft-Rechenzentrum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="14e03-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="14e03-105">Sie kann auch zum Abbrechen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14e03-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="14e03-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14e03-106">SYNTAX</span></span>

### <span data-ttu-id="14e03-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="14e03-107">UpdateExpanded (Default)</span></span>
```
Update-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-BackupDriveManifest] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>] [-LogLevel <String>]
 [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>]
 [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnShippingCarrierAccountNumber <String>]
 [-ReturnShippingCarrierName <String>] [-State <String>] [-Tag <IUpdateJobParametersTags>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="14e03-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="14e03-108">UpdateViaIdentityExpanded</span></span>
```
Update-AzImportExport -InputObject <IImportExportIdentity> [-AcceptLanguage <String>] [-BackupDriveManifest]
 [-CancelRequested] [-DeliveryPackageCarrierName <String>] [-DeliveryPackageDriveCount <Int32>]
 [-DeliveryPackageShipDate <String>] [-DeliveryPackageTrackingNumber <String>] [-DriveList <IDriveStatus[]>]
 [-LogLevel <String>] [-ReturnAddressCity <String>] [-ReturnAddressCountryOrRegion <String>]
 [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>] [-ReturnAddressPostalCode <String>]
 [-ReturnAddressRecipientName <String>] [-ReturnAddressStateOrProvince <String>]
 [-ReturnAddressStreetAddress1 <String>] [-ReturnAddressStreetAddress2 <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>] [-State <String>]
 [-Tag <IUpdateJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="14e03-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="14e03-109">DESCRIPTION</span></span>
<span data-ttu-id="14e03-110">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="14e03-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="14e03-111">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, auf denen der Import- oder Exportauftrag ausgeführt wurde, an das Microsoft-Rechenzentrum gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="14e03-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="14e03-112">Sie kann auch zum Abbrechen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14e03-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="14e03-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="14e03-113">EXAMPLES</span></span>

### <span data-ttu-id="14e03-114">Beispiel 1: Aktualisieren des ImportExport-Auftrags nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="14e03-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14e03-115">Dieses Cmdlet aktualisiert den ImportExport-Auftrag nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="14e03-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="14e03-116">Beispiel 2: Aktualisieren des ImportExport-Auftrags nach Identität.</span><span class="sxs-lookup"><span data-stu-id="14e03-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="14e03-117">Dieses Cmdlet aktualisiert den ImportExport-Auftrag nach Identität.</span><span class="sxs-lookup"><span data-stu-id="14e03-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="14e03-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14e03-118">PARAMETERS</span></span>

### <span data-ttu-id="14e03-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="14e03-119">-AcceptLanguage</span></span>
<span data-ttu-id="14e03-120">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="14e03-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="14e03-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="14e03-121">-BackupDriveManifest</span></span>
<span data-ttu-id="14e03-122">Gibt an, ob die Manifestdateien auf den Laufwerken kopiert werden sollen, um BLOBs zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="14e03-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="14e03-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="14e03-123">-CancelRequested</span></span>
<span data-ttu-id="14e03-124">Bei Angabe muss der Wert "true" sein.</span><span class="sxs-lookup"><span data-stu-id="14e03-124">If specified, the value must be true.</span></span>
<span data-ttu-id="14e03-125">Der Dienst versucht, den Auftrag zu stornieren.</span><span class="sxs-lookup"><span data-stu-id="14e03-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="14e03-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14e03-126">-DefaultProfile</span></span>
<span data-ttu-id="14e03-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14e03-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="14e03-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="14e03-129">Der Name des Netzbetreibers, der zum Versenden der Import- oder Exportlaufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14e03-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="14e03-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="14e03-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="14e03-131">Die Anzahl der Laufwerke im Paket.</span><span class="sxs-lookup"><span data-stu-id="14e03-131">The number of drives included in the package.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="14e03-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="14e03-133">Das Datum, an dem das Paket versandt wird.</span><span class="sxs-lookup"><span data-stu-id="14e03-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="14e03-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="14e03-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="14e03-135">Die Sendungsverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="14e03-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="14e03-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="14e03-136">-DriveList</span></span>
<span data-ttu-id="14e03-137">Liste der Laufwerke, aus denen der Auftrag besteht.</span><span class="sxs-lookup"><span data-stu-id="14e03-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="14e03-138">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu DRIVELIST-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="14e03-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IDriveStatus[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14e03-139">-InputObject</span></span>
<span data-ttu-id="14e03-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="14e03-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="14e03-141">-LogLevel</span></span>
<span data-ttu-id="14e03-142">Gibt an, ob die Fehlerprotokollierung oder ausführliche Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="14e03-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="14e03-143">-Name</span><span class="sxs-lookup"><span data-stu-id="14e03-143">-Name</span></span>
<span data-ttu-id="14e03-144">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="14e03-144">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14e03-145">-ResourceGroupName</span></span>
<span data-ttu-id="14e03-146">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="14e03-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="14e03-147">-ReturnAddressCity</span></span>
<span data-ttu-id="14e03-148">Der Ortsname, der für die Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14e03-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="14e03-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="14e03-150">Das Land oder die Region, das bzw. die für die Rücksendung der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="14e03-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="14e03-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="14e03-152">E-Mail-Adresse des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="14e03-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="14e03-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="14e03-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="14e03-154">Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="14e03-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="14e03-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="14e03-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="14e03-156">Die Postleitzahl, die bei der Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14e03-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="14e03-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="14e03-158">Der Name des Empfängers, der die Festplatten bei seiner Rückkehr erhält.</span><span class="sxs-lookup"><span data-stu-id="14e03-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="14e03-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="14e03-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="14e03-160">Das Bundesland oder die Provinz, das bzw. die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="14e03-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="14e03-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="14e03-162">Die erste Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="14e03-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="14e03-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="14e03-164">Die zweite Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="14e03-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="14e03-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="14e03-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="14e03-166">Die Kontonummer des Kunden beim Netzbetreiber.</span><span class="sxs-lookup"><span data-stu-id="14e03-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="14e03-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="14e03-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="14e03-168">Der Name des Netzbetreibers.</span><span class="sxs-lookup"><span data-stu-id="14e03-168">The carrier's name.</span></span>

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

### <span data-ttu-id="14e03-169">-State</span><span class="sxs-lookup"><span data-stu-id="14e03-169">-State</span></span>
<span data-ttu-id="14e03-170">Falls angegeben, muss der Wert "Versand" sein, der dem Import/Export-Dienst mitteilt, dass das Paket für den Auftrag versandt wurde.</span><span class="sxs-lookup"><span data-stu-id="14e03-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="14e03-171">Die Eigenschaften "ReturnAddress" und "DeliveryPackage" müssen entweder in dieser Anforderung oder in einer vorherigen Anforderung festgelegt worden sein, andernfalls kann die Anforderung fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="14e03-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="14e03-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="14e03-172">-SubscriptionId</span></span>
<span data-ttu-id="14e03-173">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="14e03-173">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="14e03-174">-Tag</span></span>
<span data-ttu-id="14e03-175">Gibt die Tags an, die dem Auftrag zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="14e03-175">Specifies the tags that will be assigned to the job</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IUpdateJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14e03-176">-Confirm</span><span class="sxs-lookup"><span data-stu-id="14e03-176">-Confirm</span></span>
<span data-ttu-id="14e03-177">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="14e03-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14e03-178">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="14e03-178">-WhatIf</span></span>
<span data-ttu-id="14e03-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="14e03-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14e03-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="14e03-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14e03-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14e03-181">CommonParameters</span></span>
<span data-ttu-id="14e03-182">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14e03-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14e03-183">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14e03-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14e03-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="14e03-184">INPUTS</span></span>

### <span data-ttu-id="14e03-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="14e03-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="14e03-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="14e03-186">OUTPUTS</span></span>

### <span data-ttu-id="14e03-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="14e03-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="14e03-188">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="14e03-188">NOTES</span></span>

<span data-ttu-id="14e03-189">ALIASE</span><span class="sxs-lookup"><span data-stu-id="14e03-189">ALIASES</span></span>

<span data-ttu-id="14e03-190">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="14e03-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="14e03-191">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="14e03-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="14e03-192">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="14e03-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="14e03-193">DRIVELIST <IDriveStatus[]>: Liste der Laufwerke, aus denen der Auftrag besteht.</span><span class="sxs-lookup"><span data-stu-id="14e03-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="14e03-194">`[BitLockerKey <String>]`: Der Zum Verschlüsseln des Laufwerks verwendete BitLocker-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="14e03-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="14e03-195">`[BytesSucceeded <Int64?>]`: Bytes wurden erfolgreich für das Laufwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="14e03-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="14e03-196">`[CopyStatus <String>]`: Detaillierter Status zum Datenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="14e03-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="14e03-197">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Zustand "Übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="14e03-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="14e03-198">`[DriveHeaderHash <String>]`: Hashwert der Laufwerkkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="14e03-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="14e03-199">`[DriveId <String>]`: Die Seriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="14e03-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="14e03-200">`[ErrorLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="14e03-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="14e03-201">`[ManifestFile <String>]`: Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="14e03-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="14e03-202">`[ManifestHash <String>]`: Der base16-codierte #A0 der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="14e03-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="14e03-203">`[ManifestUri <String>]`: Ein URI, der auf das BLOB verweist, das die Laufwerkmanifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="14e03-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="14e03-204">`[PercentComplete <Int32?>]`: Prozentsatz der Fertigstellung für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="14e03-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="14e03-205">`[State <DriveState?>]`: Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="14e03-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="14e03-206">`[VerboseLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="14e03-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="14e03-207">INPUTOBJECT <IImportExportIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="14e03-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="14e03-208">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="14e03-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="14e03-209">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="14e03-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="14e03-210">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="14e03-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="14e03-211">Beispielsweise "USA, Westen" oder "Westus".</span><span class="sxs-lookup"><span data-stu-id="14e03-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="14e03-212">`[ResourceGroupName <String>]`: Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="14e03-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="14e03-213">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="14e03-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="14e03-214">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="14e03-214">RELATED LINKS</span></span>

