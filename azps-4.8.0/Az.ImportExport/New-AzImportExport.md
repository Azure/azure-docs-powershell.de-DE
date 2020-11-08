---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/new-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/New-AzImportExport.md
ms.openlocfilehash: 9b0cf40b090111a6bd32bc87b6e72bc542eae5ed
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166921"
---
# <span data-ttu-id="b1503-101">New-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="b1503-101">New-AzImportExport</span></span>

## <span data-ttu-id="b1503-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b1503-102">SYNOPSIS</span></span>
<span data-ttu-id="b1503-103">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1503-103">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="b1503-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b1503-104">SYNTAX</span></span>

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

## <span data-ttu-id="b1503-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1503-105">DESCRIPTION</span></span>
<span data-ttu-id="b1503-106">Erstellt einen neuen Auftrag oder aktualisiert einen vorhandenen Auftrag im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1503-106">Creates a new job or updates an existing job in the specified subscription.</span></span>

## <span data-ttu-id="b1503-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1503-107">EXAMPLES</span></span>

### <span data-ttu-id="b1503-108">Beispiel 1: Erstellen eines neuen DataObjects-Auftrags</span><span class="sxs-lookup"><span data-stu-id="b1503-108">Example 1: Create a new ImportExport job</span></span>
```powershell
PS C:\> $driveList = @( @{ DriveId = "9CA995BA"; BitLockerKey = "238810-662376-448998-450120-652806-203390-606320-483076"; ManifestFile = "\\DriveManifest.xml"; ManifestHash = "109B21108597EF36D5785F08303F3638"; DriveHeaderHash = "" })
PS C:\> New-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -Location eastus -StorageAccountId "/subscriptions/<SubscriptionId>/resourcegroups/ImportTestRG/providers/Microsoft.Storage/storageAccounts/teststorageforimport" -JobType Import -ReturnAddressRecipientName "Some name" -ReturnAddressStreetAddress1 "Street1" -ReturnAddressCity "Redmond" -ReturnAddressStateOrProvince "WA" -ReturnAddressPostalCode "98008" -ReturnAddressCountryOrRegion "USA" -ReturnAddressPhone "4250000000" -ReturnAddressEmail test@contoso.com -DiagnosticsPath "waimportexport" -BackupDriveManifest -DriveList $driveList
Location Name     Type
-------- ----     ----
eastus   test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="b1503-109">Diese Cmdlets erstellen einen neuen DataObjects-Auftrag.</span><span class="sxs-lookup"><span data-stu-id="b1503-109">These cmdlets create a new ImportExport job.</span></span>

## <span data-ttu-id="b1503-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1503-110">PARAMETERS</span></span>

### <span data-ttu-id="b1503-111">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="b1503-111">-AcceptLanguage</span></span>
<span data-ttu-id="b1503-112">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="b1503-112">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="b1503-113">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="b1503-113">-BackupDriveManifest</span></span>
<span data-ttu-id="b1503-114">Der Standardwert ist "false".</span><span class="sxs-lookup"><span data-stu-id="b1503-114">Default value is false.</span></span>
<span data-ttu-id="b1503-115">Gibt an, ob die Manifestdateien auf den Laufwerken kopiert werden sollen, um BLOBs zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="b1503-115">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="b1503-116">-BlobListBlobPath</span><span class="sxs-lookup"><span data-stu-id="b1503-116">-BlobListBlobPath</span></span>
<span data-ttu-id="b1503-117">Eine Sammlung von Zeichenfolgen in BLOB-Pfaden.</span><span class="sxs-lookup"><span data-stu-id="b1503-117">A collection of blob-path strings.</span></span>

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

### <span data-ttu-id="b1503-118">-BlobListBlobPathPrefix</span><span class="sxs-lookup"><span data-stu-id="b1503-118">-BlobListBlobPathPrefix</span></span>
<span data-ttu-id="b1503-119">Eine Sammlung von Zeichenfolgen für BLOB-Präfixe.</span><span class="sxs-lookup"><span data-stu-id="b1503-119">A collection of blob-prefix strings.</span></span>

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

### <span data-ttu-id="b1503-120">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="b1503-120">-CancelRequested</span></span>
<span data-ttu-id="b1503-121">Gibt an, ob eine Anforderung übermittelt wurde, um den Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="b1503-121">Indicates whether a request has been submitted to cancel the job.</span></span>

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

### <span data-ttu-id="b1503-122">-ClientTenantId</span><span class="sxs-lookup"><span data-stu-id="b1503-122">-ClientTenantId</span></span>
<span data-ttu-id="b1503-123">Die Mandanten-ID des Clients, der die Anforderung vornimmt.</span><span class="sxs-lookup"><span data-stu-id="b1503-123">The tenant ID of the client making the request.</span></span>

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

### <span data-ttu-id="b1503-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1503-124">-DefaultProfile</span></span>
<span data-ttu-id="b1503-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b1503-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1503-126">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="b1503-126">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="b1503-127">Der Name des Netzbetreibers, der verwendet wird, um die Import-oder Export Laufwerke zu versenden.</span><span class="sxs-lookup"><span data-stu-id="b1503-127">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="b1503-128">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="b1503-128">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="b1503-129">Die Anzahl der Laufwerke, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b1503-129">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="b1503-130">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="b1503-130">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="b1503-131">Das Datum, an dem das Paket ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-131">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="b1503-132">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="b1503-132">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="b1503-133">Die Nachverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b1503-133">The tracking number of the package.</span></span>

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

### <span data-ttu-id="b1503-134">-DiagnosticsPath</span><span class="sxs-lookup"><span data-stu-id="b1503-134">-DiagnosticsPath</span></span>
<span data-ttu-id="b1503-135">Das virtuelle BLOB-Verzeichnis, in das die Kopierprotokolle und Sicherungen von Drive Manifest-Dateien (sofern aktiviert) gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="b1503-135">The virtual blob directory to which the copy logs and backups of drive manifest files (if enabled) will be stored.</span></span>

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

### <span data-ttu-id="b1503-136">-Drivelist</span><span class="sxs-lookup"><span data-stu-id="b1503-136">-DriveList</span></span>
<span data-ttu-id="b1503-137">Eine Liste mit bis zu zehn Laufwerken, die den Auftrag umfassen.</span><span class="sxs-lookup"><span data-stu-id="b1503-137">List of up to ten drives that comprise the job.</span></span>
<span data-ttu-id="b1503-138">Die Laufwerkliste ist ein erforderliches Element für einen Importauftrag; Sie ist für Exportaufträge nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1503-138">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
<span data-ttu-id="b1503-139">Wenn Sie das Konstrukt erstellen möchten, lesen Sie den Abschnitt "Notizen" für drivelist-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b1503-139">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="b1503-140">-ExportBlobListblobPath</span><span class="sxs-lookup"><span data-stu-id="b1503-140">-ExportBlobListblobPath</span></span>
<span data-ttu-id="b1503-141">Der relative URI für das Block-BLOB, das die Liste der BLOB-Pfade oder BLOB-Pfad Präfixe wie oben definiert enthält, beginnend mit dem Containernamen.</span><span class="sxs-lookup"><span data-stu-id="b1503-141">The relative URI to the block blob that contains the list of blob paths or blob path prefixes as defined above, beginning with the container name.</span></span>
<span data-ttu-id="b1503-142">Wenn sich das BLOB im Stammcontainer befindet, muss der URI mit $root beginnen.</span><span class="sxs-lookup"><span data-stu-id="b1503-142">If the blob is in root container, the URI must begin with $root.</span></span>

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

### <span data-ttu-id="b1503-143">-IncompleteBlobListUri</span><span class="sxs-lookup"><span data-stu-id="b1503-143">-IncompleteBlobListUri</span></span>
<span data-ttu-id="b1503-144">Ein BLOB-Pfad, der auf ein Block-BLOB verweist, das eine Liste von BLOB-Namen enthält, die aufgrund unzureichenden Speicherplatzes nicht exportiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b1503-144">A blob path that points to a block blob containing a list of blob names that were not exported due to insufficient drive space.</span></span>
<span data-ttu-id="b1503-145">Wenn alle Blobs erfolgreich exportiert wurden, wird dieses Element in der Antwort nicht berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b1503-145">If all blobs were exported successfully, then this element is not included in the response.</span></span>

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

### <span data-ttu-id="b1503-146">-JobType</span><span class="sxs-lookup"><span data-stu-id="b1503-146">-JobType</span></span>
<span data-ttu-id="b1503-147">Der Typ des Auftrags</span><span class="sxs-lookup"><span data-stu-id="b1503-147">The type of job</span></span>

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

### <span data-ttu-id="b1503-148">-Standort</span><span class="sxs-lookup"><span data-stu-id="b1503-148">-Location</span></span>
<span data-ttu-id="b1503-149">Gibt den unterstützten Azure-Speicherort an, an dem der Auftrag erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-149">Specifies the supported Azure location where the job should be created</span></span>

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

### <span data-ttu-id="b1503-150">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="b1503-150">-LogLevel</span></span>
<span data-ttu-id="b1503-151">Der Standardwert ist Error.</span><span class="sxs-lookup"><span data-stu-id="b1503-151">Default value is Error.</span></span>
<span data-ttu-id="b1503-152">Gibt an, ob die Fehlerprotokollierung oder die ausführliche Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b1503-152">Indicates whether error logging or verbose logging will be enabled.</span></span>

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

### <span data-ttu-id="b1503-153">-Name</span><span class="sxs-lookup"><span data-stu-id="b1503-153">-Name</span></span>
<span data-ttu-id="b1503-154">Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b1503-154">The name of the import/export job.</span></span>

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

### <span data-ttu-id="b1503-155">-PercentComplete</span><span class="sxs-lookup"><span data-stu-id="b1503-155">-PercentComplete</span></span>
<span data-ttu-id="b1503-156">Gesamtprozentsatz, der für den Auftrag abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="b1503-156">Overall percentage completed for the job.</span></span>

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

### <span data-ttu-id="b1503-157">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="b1503-157">-ProvisioningState</span></span>
<span data-ttu-id="b1503-158">Gibt den Bereitstellungsstatus des Auftrags an.</span><span class="sxs-lookup"><span data-stu-id="b1503-158">Specifies the provisioning state of the job.</span></span>

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

### <span data-ttu-id="b1503-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1503-159">-ResourceGroupName</span></span>
<span data-ttu-id="b1503-160">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="b1503-160">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="b1503-161">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="b1503-161">-ReturnAddressCity</span></span>
<span data-ttu-id="b1503-162">Der Name der Stadt, die beim Zurückgeben der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-162">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-163">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="b1503-163">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="b1503-164">Das Land oder die Region, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-164">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-165">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="b1503-165">-ReturnAddressEmail</span></span>
<span data-ttu-id="b1503-166">Die e-Mail-Adresse des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="b1503-166">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="b1503-167">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="b1503-167">-ReturnAddressPhone</span></span>
<span data-ttu-id="b1503-168">Die Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="b1503-168">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="b1503-169">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="b1503-169">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="b1503-170">Die Postleitzahl, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-170">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-171">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="b1503-171">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="b1503-172">Der Name des Empfängers, der die Festplatten empfängt, wenn er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-172">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="b1503-173">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="b1503-173">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="b1503-174">Das Bundesland, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-174">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-175">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="b1503-175">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="b1503-176">Die erste Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-176">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-177">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="b1503-177">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="b1503-178">Die zweite Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-178">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-179">-ReturnPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="b1503-179">-ReturnPackageCarrierName</span></span>
<span data-ttu-id="b1503-180">Der Name des Netzbetreibers, der verwendet wird, um die Import-oder Export Laufwerke zu versenden.</span><span class="sxs-lookup"><span data-stu-id="b1503-180">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="b1503-181">-ReturnPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="b1503-181">-ReturnPackageDriveCount</span></span>
<span data-ttu-id="b1503-182">Die Anzahl der Laufwerke, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="b1503-182">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="b1503-183">-ReturnPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="b1503-183">-ReturnPackageShipDate</span></span>
<span data-ttu-id="b1503-184">Das Datum, an dem das Paket ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-184">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="b1503-185">-ReturnPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="b1503-185">-ReturnPackageTrackingNumber</span></span>
<span data-ttu-id="b1503-186">Die Nachverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="b1503-186">The tracking number of the package.</span></span>

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

### <span data-ttu-id="b1503-187">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="b1503-187">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="b1503-188">Die Kontonummer des Kunden beim Netzbetreiber.</span><span class="sxs-lookup"><span data-stu-id="b1503-188">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="b1503-189">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="b1503-189">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="b1503-190">Der Name des Netzbetreibers.</span><span class="sxs-lookup"><span data-stu-id="b1503-190">The carrier's name.</span></span>

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

### <span data-ttu-id="b1503-191">-ShippingInformationCity</span><span class="sxs-lookup"><span data-stu-id="b1503-191">-ShippingInformationCity</span></span>
<span data-ttu-id="b1503-192">Der Name der Stadt, die beim Zurückgeben der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-192">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-193">-ShippingInformationCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="b1503-193">-ShippingInformationCountryOrRegion</span></span>
<span data-ttu-id="b1503-194">Das Land oder die Region, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-194">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-195">-ShippingInformationPhone</span><span class="sxs-lookup"><span data-stu-id="b1503-195">-ShippingInformationPhone</span></span>
<span data-ttu-id="b1503-196">Die Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="b1503-196">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="b1503-197">-ShippingInformationPostalCode</span><span class="sxs-lookup"><span data-stu-id="b1503-197">-ShippingInformationPostalCode</span></span>
<span data-ttu-id="b1503-198">Die Postleitzahl, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-198">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-199">-ShippingInformationRecipientName</span><span class="sxs-lookup"><span data-stu-id="b1503-199">-ShippingInformationRecipientName</span></span>
<span data-ttu-id="b1503-200">Der Name des Empfängers, der die Festplatten empfängt, wenn er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-200">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="b1503-201">-ShippingInformationStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="b1503-201">-ShippingInformationStateOrProvince</span></span>
<span data-ttu-id="b1503-202">Das Bundesland, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-202">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-203">-ShippingInformationStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="b1503-203">-ShippingInformationStreetAddress1</span></span>
<span data-ttu-id="b1503-204">Die erste Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-204">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-205">-ShippingInformationStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="b1503-205">-ShippingInformationStreetAddress2</span></span>
<span data-ttu-id="b1503-206">Die zweite Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b1503-206">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="b1503-207">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="b1503-207">-State</span></span>
<span data-ttu-id="b1503-208">Aktueller Status des Auftrags.</span><span class="sxs-lookup"><span data-stu-id="b1503-208">Current state of the job.</span></span>

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

### <span data-ttu-id="b1503-209">-StorageAccountId</span><span class="sxs-lookup"><span data-stu-id="b1503-209">-StorageAccountId</span></span>
<span data-ttu-id="b1503-210">Der Ressourcenbezeichner des speicherkontos, in das Daten importiert oder exportiert werden.</span><span class="sxs-lookup"><span data-stu-id="b1503-210">The resource identifier of the storage account where data will be imported to or exported from.</span></span>

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

### <span data-ttu-id="b1503-211">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b1503-211">-SubscriptionId</span></span>
<span data-ttu-id="b1503-212">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="b1503-212">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="b1503-213">-Tag</span><span class="sxs-lookup"><span data-stu-id="b1503-213">-Tag</span></span>
<span data-ttu-id="b1503-214">Gibt die Tags an, die dem Auftrag zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b1503-214">Specifies the tags that will be assigned to the job.</span></span>

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

### <span data-ttu-id="b1503-215">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b1503-215">-Confirm</span></span>
<span data-ttu-id="b1503-216">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1503-216">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b1503-217">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b1503-217">-WhatIf</span></span>
<span data-ttu-id="b1503-218">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-218">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b1503-219">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b1503-219">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b1503-220">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1503-220">CommonParameters</span></span>
<span data-ttu-id="b1503-221">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1503-221">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1503-222">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1503-222">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1503-223">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b1503-223">INPUTS</span></span>

## <span data-ttu-id="b1503-224">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b1503-224">OUTPUTS</span></span>

### <span data-ttu-id="b1503-225">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="b1503-225">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="b1503-226">Notizen</span><span class="sxs-lookup"><span data-stu-id="b1503-226">NOTES</span></span>

<span data-ttu-id="b1503-227">Aliase</span><span class="sxs-lookup"><span data-stu-id="b1503-227">ALIASES</span></span>

<span data-ttu-id="b1503-228">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b1503-228">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b1503-229">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="b1503-229">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b1503-230">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="b1503-230">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b1503-231">Drivelist <IDriveStatus [] >: Liste mit bis zu zehn Laufwerken, die den Auftrag umfassen.</span><span class="sxs-lookup"><span data-stu-id="b1503-231">DRIVELIST <IDriveStatus[]>: List of up to ten drives that comprise the job.</span></span> <span data-ttu-id="b1503-232">Die Laufwerkliste ist ein erforderliches Element für einen Importauftrag; Sie ist für Exportaufträge nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="b1503-232">The drive list is a required element for an import job; it is not specified for export jobs.</span></span>
  - <span data-ttu-id="b1503-233">`[BitLockerKey <String>]`: Der BitLocker-Schlüssel, der zum Verschlüsseln des Laufwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1503-233">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="b1503-234">`[BytesSucceeded <Int64?>]`: Bytes, die für das Laufwerk erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="b1503-234">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="b1503-235">`[CopyStatus <String>]`: Detaillierter Status zum Datentransferprozess.</span><span class="sxs-lookup"><span data-stu-id="b1503-235">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="b1503-236">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Status "übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="b1503-236">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="b1503-237">`[DriveHeaderHash <String>]`: Der Hashwert des Laufwerk Headers.</span><span class="sxs-lookup"><span data-stu-id="b1503-237">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="b1503-238">`[DriveId <String>]`: Die Hardware-Seriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="b1503-238">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="b1503-239">`[ErrorLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="b1503-239">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="b1503-240">`[ManifestFile <String>]`: Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="b1503-240">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="b1503-241">`[ManifestHash <String>]`: Der Base16-codierte MD5-Hash der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="b1503-241">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="b1503-242">`[ManifestUri <String>]`: Ein URI, der auf das BLOB verweist, das die Laufwerk Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="b1503-242">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="b1503-243">`[PercentComplete <Int32?>]`: Prozentsatz für das Laufwerk abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b1503-243">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="b1503-244">`[State <DriveState?>]`: Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="b1503-244">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="b1503-245">`[VerboseLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="b1503-245">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

## <span data-ttu-id="b1503-246">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b1503-246">RELATED LINKS</span></span>

