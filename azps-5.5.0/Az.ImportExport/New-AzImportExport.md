---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100155553"
---
# <span data-ttu-id="11738-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="11738-101">New-AzImportExport</span></span>

## <span data-ttu-id="11738-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11738-102">SYNOPSIS</span></span>
<span data-ttu-id="11738-103">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11738-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="11738-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="11738-104">SYNTAX</span></span>

```
New-AzImportExport -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AcceptLanguage <String>] [-ClientTenantId <String>] [-BackupDriveManifest] [-BlobListBlobPath <String[]>]
 [-BlobListBlobPathPrefix <String[]>] [-CancelRequested] [-DeliveryPackageCarrierName <String>]
 [-DeliveryPackageDriveCount <Int32>] [-DeliveryPackageShipDate <String>]
 [-DeliveryPackageTrackingNumber <String>] [-DiagnosticsPath <String>] [-DriveList <IDriveStatus[]>]
 [-ExportBlobListblobPath <String>] [-IncompleteBlobListUri <String>] [-JobType <String>] [-Location <String>]
 [-LogLevel <String>] [-PercentComplete <Int32>] [-ProvisioningState <String>] [-ReturnAddressCity <String>]
 [-ReturnAddressCountryOrRegion <String>] [-ReturnAddressEmail <String>] [-ReturnAddressPhone <String>]
 [-ReturnAddressPostalCode <String>] [-ReturnAddressRecipientName <String>]
 [-ReturnAddressStateOrProvince <String>] [-ReturnAddressStreetAddress1 <String>]
 [-ReturnAddressStreetAddress2 <String>] [-ReturnPackageCarrierName <String>]
 [-ReturnPackageDriveCount <Int32>] [-ReturnPackageShipDate <String>] [-ReturnPackageTrackingNumber <String>]
 [-ReturnShippingCarrierAccountNumber <String>] [-ReturnShippingCarrierName <String>]
 [-ShippingInformationCity <String>] [-ShippingInformationCountryOrRegion <String>]
 [-ShippingInformationPhone <String>] [-ShippingInformationPostalCode <String>]
 [-ShippingInformationRecipientName <String>] [-ShippingInformationStateOrProvince <String>]
 [-ShippingInformationStreetAddress1 <String>] [-ShippingInformationStreetAddress2 <String>] [-State <String>]
 [-StorageAccountId <String>] [-Tag <IPutJobParametersTags>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="11738-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="11738-105">DESCRIPTION</span></span>
<span data-ttu-id="11738-106">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="11738-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="11738-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="11738-107">EXAMPLES</span></span>

### <span data-ttu-id="11738-108">Beispiel 1: Erstellen eines neuen ImportExport-Auftrags</span><span class="sxs-lookup"><span data-stu-id="11738-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="11738-109">Diese Cmdlets erstellen einen neuen ImportExport-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="11738-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="11738-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="11738-110">PARAMETERS</span></span>

### <span data-ttu-id="11738-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="11738-111">-AcceptLanguage</span></span>
<span data-ttu-id="11738-112">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="11738-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="11738-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="11738-113">-BackupDriveManifest</span></span>
<span data-ttu-id="11738-114">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="11738-114">Default value is false.</span></span>
<span data-ttu-id="11738-115">Gibt an, ob die Manifestdateien auf den Laufwerken kopiert werden sollen, um BLOBs zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="11738-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="11738-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="11738-116">-BlobListBlobPath</span></span>
<span data-ttu-id="11738-117">Eine Sammlung von BLOB-Pfad-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="11738-117">A collection of blob-path strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11738-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="11738-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="11738-119">Eine Sammlung von Blob-Präfix-Zeichenfolgen.</span><span class="sxs-lookup"><span data-stu-id="11738-119">A collection of blob-prefix strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11738-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="11738-120">-CancelRequested</span></span>
<span data-ttu-id="11738-121">Gibt an, ob eine Anforderung zum Abbrechen des Auftrags übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="11738-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="11738-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="11738-122">-ClientTenantId</span></span>
<span data-ttu-id="11738-123">Die Mandanten-ID des Clients, der die Anforderung macht.</span><span class="sxs-lookup"><span data-stu-id="11738-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="11738-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11738-124">-DefaultProfile</span></span>
<span data-ttu-id="11738-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="11738-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11738-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="11738-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="11738-127">Der Name des Netzbetreibers, der zum Versenden der Import- oder Exportlaufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11738-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="11738-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="11738-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="11738-129">Die Anzahl der Laufwerke im Paket.</span><span class="sxs-lookup"><span data-stu-id="11738-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="11738-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="11738-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="11738-131">Das Datum, an dem das Paket versandt wird.</span><span class="sxs-lookup"><span data-stu-id="11738-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="11738-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="11738-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="11738-133">Die Sendungsverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="11738-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="11738-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="11738-134">-DiagnosticsPath</span></span>
<span data-ttu-id="11738-135">Das virtuelle BLOB-Verzeichnis, in dem die Kopierprotokolle und Sicherungen der Laufwerkmanifestdateien (sofern aktiviert) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="11738-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="11738-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="11738-136">-DriveList</span></span>
<span data-ttu-id="11738-137">Liste von bis zu zehn Laufwerken, aus denen der Auftrag besteht.</span><span class="sxs-lookup"><span data-stu-id="11738-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="11738-138">Die Laufwerkliste ist ein erforderliches Element für einen Importauftrag. für Exportaufträge nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="11738-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="11738-139">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu DRIVELIST-Eigenschaften und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="11738-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="11738-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="11738-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="11738-141">Der relative URI des Block-BLOB, der die Liste der BLOB-Pfade oder BLOB-Pfadpräfixe enthält, wie oben definiert, beginnend mit dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="11738-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="11738-142">Wenn sich das BLOB im Stammcontainer befindet, muss der URI mit $root.</span><span class="sxs-lookup"><span data-stu-id="11738-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="11738-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="11738-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="11738-144">Ein BLOB-Pfad, der auf einen Block-BLOB verweist, der eine Liste von BLOB-Namen enthält, die aufgrund von unzureichenden Laufwerkspeicher nicht exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="11738-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="11738-145">Wenn alle BLOBS erfolgreich exportiert wurden, wird dieses Element nicht in die Antwort einbezogen.</span><span class="sxs-lookup"><span data-stu-id="11738-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="11738-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="11738-146">-JobType</span></span>
<span data-ttu-id="11738-147">Der Typ des Auftrags</span><span class="sxs-lookup"><span data-stu-id="11738-147">The type of job</span></span>

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

### <span data-ttu-id="11738-148">-Location</span><span class="sxs-lookup"><span data-stu-id="11738-148">-Location</span></span>
<span data-ttu-id="11738-149">Gibt den unterstützten Azure-Speicherort an, an dem der Auftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="11738-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="11738-150">-LogLevel</span></span>
<span data-ttu-id="11738-151">Der Standardwert ist "Fehler".</span><span class="sxs-lookup"><span data-stu-id="11738-151">Default value is Error.</span></span>
<span data-ttu-id="11738-152">Gibt an, ob die Fehlerprotokollierung oder ausführliche Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="11738-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="11738-153">-Name</span><span class="sxs-lookup"><span data-stu-id="11738-153">-Name</span></span>
<span data-ttu-id="11738-154">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="11738-154">The name of the import/export job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: JobName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11738-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="11738-155">-PercentComplete</span></span>
<span data-ttu-id="11738-156">Gesamtprozentsatz für den Auftrag abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="11738-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="11738-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="11738-157">-ProvisioningState</span></span>
<span data-ttu-id="11738-158">Gibt den Bereitstellungszustand des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="11738-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="11738-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11738-159">-ResourceGroupName</span></span>
<span data-ttu-id="11738-160">Der Ressourcengruppenname identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="11738-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="11738-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="11738-161">-ReturnAddressCity</span></span>
<span data-ttu-id="11738-162">Der Ortsname, der für die Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="11738-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="11738-164">Das Land oder die Region, das bzw. die für die Rücksendung der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="11738-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="11738-166">E-Mail-Adresse des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="11738-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="11738-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="11738-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="11738-168">Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="11738-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="11738-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="11738-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="11738-170">Die Postleitzahl, die bei der Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="11738-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="11738-172">Der Name des Empfängers, der die Festplatten bei seiner Rückkehr erhält.</span><span class="sxs-lookup"><span data-stu-id="11738-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="11738-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="11738-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="11738-174">Das Bundesland oder die Provinz, das bzw. die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="11738-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="11738-176">Die erste Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="11738-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="11738-178">Die zweite Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="11738-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="11738-180">Der Name des Netzbetreibers, der zum Versenden der Import- oder Exportlaufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="11738-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="11738-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="11738-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="11738-182">Die Anzahl der Laufwerke im Paket.</span><span class="sxs-lookup"><span data-stu-id="11738-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="11738-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="11738-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="11738-184">Das Datum, an dem das Paket versandt wird.</span><span class="sxs-lookup"><span data-stu-id="11738-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="11738-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="11738-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="11738-186">Die Sendungsverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="11738-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="11738-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="11738-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="11738-188">Die Kontonummer des Kunden beim Netzbetreiber.</span><span class="sxs-lookup"><span data-stu-id="11738-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="11738-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="11738-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="11738-190">Der Name des Netzbetreibers.</span><span class="sxs-lookup"><span data-stu-id="11738-190">The carrier's name.</span></span>

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

### <span data-ttu-id="11738-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="11738-191">-ShippingInformationCity</span></span>
<span data-ttu-id="11738-192">Der Ortsname, der für die Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="11738-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="11738-194">Das Land oder die Region, das bzw. die für die Rücksendung der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="11738-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="11738-196">Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="11738-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="11738-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="11738-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="11738-198">Die Postleitzahl, die bei der Rücksendung der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="11738-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="11738-200">Der Name des Empfängers, der die Festplatten bei seiner Rückkehr erhält.</span><span class="sxs-lookup"><span data-stu-id="11738-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="11738-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="11738-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="11738-202">Das Bundesland oder die Provinz, das bzw. die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="11738-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="11738-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="11738-204">Die erste Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="11738-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="11738-206">Die zweite Zeile der Straße, die bei der Rückgabe der Laufwerke zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="11738-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="11738-207">-State</span><span class="sxs-lookup"><span data-stu-id="11738-207">-State</span></span>
<span data-ttu-id="11738-208">Aktueller Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="11738-208">Current state of the job.</span></span>

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

### <span data-ttu-id="11738-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="11738-209">-StorageAccountId</span></span>
<span data-ttu-id="11738-210">Die Ressourcen-ID des Speicherkontos, aus dem Daten importiert oder aus dem exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="11738-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="11738-211">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="11738-211">-SubscriptionId</span></span>
<span data-ttu-id="11738-212">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="11738-212">The subscription ID for the Azure user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11738-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="11738-213">-Tag</span></span>
<span data-ttu-id="11738-214">Gibt die Tags an, die dem Auftrag zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="11738-214">Specifies the tags that will be assigned to the job.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IPutJobParametersTags
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="11738-215">-Confirm</span><span class="sxs-lookup"><span data-stu-id="11738-215">-Confirm</span></span>
<span data-ttu-id="11738-216">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="11738-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11738-217">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="11738-217">-WhatIf</span></span>
<span data-ttu-id="11738-218">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="11738-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="11738-219">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="11738-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11738-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11738-220">CommonParameters</span></span>
<span data-ttu-id="11738-221">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11738-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11738-222">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="11738-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11738-223">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="11738-223">INPUTS</span></span>

## <span data-ttu-id="11738-224">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="11738-224">OUTPUTS</span></span>

### <span data-ttu-id="11738-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="11738-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="11738-226">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="11738-226">NOTES</span></span>

<span data-ttu-id="11738-227">ALIASE</span><span class="sxs-lookup"><span data-stu-id="11738-227">ALIASES</span></span>

<span data-ttu-id="11738-228">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="11738-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="11738-229">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="11738-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="11738-230">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="11738-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="11738-231">DRIVELIST <IDriveStatus[]>: Liste von bis zu zehn Laufwerken, aus denen dieser Auftrag besteht.</span><span class="sxs-lookup"><span data-stu-id="11738-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="11738-232">Die Laufwerkliste ist ein erforderliches Element für einen Importauftrag. für Exportaufträge nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="11738-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="11738-233">`[BitLockerKey <String>]`: Der Zum Verschlüsseln des Laufwerks verwendete BitLocker-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="11738-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="11738-234">`[BytesSucceeded <Int64?>]`: Bytes wurden erfolgreich für das Laufwerk übertragen.</span><span class="sxs-lookup"><span data-stu-id="11738-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="11738-235">`[CopyStatus <String>]`: Detaillierter Status zum Datenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="11738-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="11738-236">Dieses Feld wird erst in der Antwort zurückgegeben, wenn sich das Laufwerk im Zustand "Übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="11738-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="11738-237">`[DriveHeaderHash <String>]`: Der Hashwert für die Laufwerkkopfzeile.</span><span class="sxs-lookup"><span data-stu-id="11738-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="11738-238">`[DriveId <String>]`: Die Seriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="11738-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="11738-239">`[ErrorLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="11738-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="11738-240">`[ManifestFile <String>]`: Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="11738-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="11738-241">`[ManifestHash <String>]`: Der base16-codierte #A0 der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="11738-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="11738-242">`[ManifestUri <String>]`: Ein URI, der auf das BLOB verweist, das die Laufwerkmanifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="11738-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="11738-243">`[PercentComplete <Int32?>]`: Prozentsatz der Fertigstellung für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="11738-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="11738-244">`[State <DriveState?>]`: Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="11738-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="11738-245">`[VerboseLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="11738-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="11738-246">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="11738-246">RELATED LINKS</span></span>

