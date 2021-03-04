---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: 7b604c22878d3d76e66a6d615deb1b46cedaad32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930080"
---
# <span data-ttu-id="0384c-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="0384c-101">Update-AzImportExport</span></span>

## <span data-ttu-id="0384c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0384c-102">SYNOPSIS</span></span>
<span data-ttu-id="0384c-103">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="0384c-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="0384c-104">Sie können diesen Vorgang aufrufen, um den Import-/Exportdienst darüber zu informieren, dass die Festplatten, die den Import- oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="0384c-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="0384c-105">Sie kann auch zum Kündigen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0384c-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="0384c-106">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0384c-106">SYNTAX</span></span>

### <span data-ttu-id="0384c-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="0384c-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="0384c-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="0384c-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="0384c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0384c-109">DESCRIPTION</span></span>
<span data-ttu-id="0384c-110">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="0384c-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="0384c-111">Sie können diesen Vorgang aufrufen, um den Import-/Exportdienst darüber zu informieren, dass die Festplatten, die den Import- oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum geliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="0384c-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="0384c-112">Sie kann auch zum Kündigen eines vorhandenen Auftrags verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0384c-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="0384c-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0384c-113">EXAMPLES</span></span>

### <span data-ttu-id="0384c-114">Beispiel 1: Aktualisieren des ImportExportauftrags nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="0384c-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="0384c-115">Dieses Cmdlet aktualisiert ImportExportauftrag nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="0384c-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="0384c-116">Beispiel 2: Aktualisieren des ImportExportauftrags nach Identität.</span><span class="sxs-lookup"><span data-stu-id="0384c-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="0384c-117">Dieses Cmdlet aktualisiert importExportauftrag nach Identität.</span><span class="sxs-lookup"><span data-stu-id="0384c-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="0384c-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0384c-118">PARAMETERS</span></span>

### <span data-ttu-id="0384c-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="0384c-119">-AcceptLanguage</span></span>
<span data-ttu-id="0384c-120">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="0384c-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="0384c-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="0384c-121">-BackupDriveManifest</span></span>
<span data-ttu-id="0384c-122">Gibt an, ob die Manifestdateien auf den Laufwerken kopiert werden sollen, um Blobs zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="0384c-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="0384c-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="0384c-123">-CancelRequested</span></span>
<span data-ttu-id="0384c-124">Wenn angegeben, muss der Wert "true" sein.</span><span class="sxs-lookup"><span data-stu-id="0384c-124">If specified, the value must be true.</span></span>
<span data-ttu-id="0384c-125">Der Dienst versucht, den Auftrag zu kündigen.</span><span class="sxs-lookup"><span data-stu-id="0384c-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="0384c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0384c-126">-DefaultProfile</span></span>
<span data-ttu-id="0384c-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0384c-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0384c-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="0384c-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="0384c-129">Der Name des Netzbetreibers, der zum Versenden der Import- oder Exportlaufwerke verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0384c-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="0384c-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="0384c-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="0384c-131">Die Anzahl der laufwerke, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0384c-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="0384c-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="0384c-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="0384c-133">Das Datum, an dem das Paket versendet wird.</span><span class="sxs-lookup"><span data-stu-id="0384c-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="0384c-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="0384c-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="0384c-135">Die Sendungsverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="0384c-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="0384c-136">-DriveList</span><span class="sxs-lookup"><span data-stu-id="0384c-136">-DriveList</span></span>
<span data-ttu-id="0384c-137">Liste der Laufwerke, die den Auftrag umfassen.</span><span class="sxs-lookup"><span data-stu-id="0384c-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="0384c-138">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu DRIVELIST-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0384c-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="0384c-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0384c-139">-InputObject</span></span>
<span data-ttu-id="0384c-140">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0384c-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0384c-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="0384c-141">-LogLevel</span></span>
<span data-ttu-id="0384c-142">Gibt an, ob die Fehlerprotokollierung oder ausführliche Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0384c-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="0384c-143">-Name</span><span class="sxs-lookup"><span data-stu-id="0384c-143">-Name</span></span>
<span data-ttu-id="0384c-144">Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="0384c-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="0384c-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0384c-145">-ResourceGroupName</span></span>
<span data-ttu-id="0384c-146">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0384c-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="0384c-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="0384c-147">-ReturnAddressCity</span></span>
<span data-ttu-id="0384c-148">Der Ortsname, der bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="0384c-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="0384c-150">Das Land oder die Region, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="0384c-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="0384c-152">E-Mail-Adresse des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="0384c-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="0384c-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="0384c-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="0384c-154">Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="0384c-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="0384c-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="0384c-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="0384c-156">Die Postleitzahl, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="0384c-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="0384c-158">Der Name des Empfängers, der die Festplatten erhält, wenn er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0384c-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="0384c-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="0384c-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="0384c-160">Das Bundesland oder die Provinz, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="0384c-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="0384c-162">Die erste Zeile der Straße, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="0384c-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="0384c-164">Die zweite Zeile der Straße, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0384c-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="0384c-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="0384c-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="0384c-166">Die Kontonummer des Kunden beim Netzbetreiber.</span><span class="sxs-lookup"><span data-stu-id="0384c-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="0384c-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="0384c-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="0384c-168">Der Name des Netzbetreibers.</span><span class="sxs-lookup"><span data-stu-id="0384c-168">The carrier's name.</span></span>

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

### <span data-ttu-id="0384c-169">-State</span><span class="sxs-lookup"><span data-stu-id="0384c-169">-State</span></span>
<span data-ttu-id="0384c-170">Wenn angegeben, muss der Wert "Versand" sein, der dem Import-/Exportdienst mitteilt, dass das Paket für den Auftrag versendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0384c-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="0384c-171">Die Eigenschaften ReturnAddress und DeliveryPackage müssen entweder in dieser Anforderung oder in einer vorherigen Anforderung festgelegt worden sein, da andernfalls ein Fehler bei der Anforderung vor sich geht.</span><span class="sxs-lookup"><span data-stu-id="0384c-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="0384c-172">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0384c-172">-SubscriptionId</span></span>
<span data-ttu-id="0384c-173">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0384c-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="0384c-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="0384c-174">-Tag</span></span>
<span data-ttu-id="0384c-175">Gibt die Kategorien an, die dem Auftrag zugewiesen werden sollen</span><span class="sxs-lookup"><span data-stu-id="0384c-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="0384c-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0384c-176">-Confirm</span></span>
<span data-ttu-id="0384c-177">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0384c-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0384c-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0384c-178">-WhatIf</span></span>
<span data-ttu-id="0384c-179">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0384c-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0384c-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0384c-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0384c-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0384c-181">CommonParameters</span></span>
<span data-ttu-id="0384c-182">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0384c-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0384c-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0384c-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0384c-184">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0384c-184">INPUTS</span></span>

### <span data-ttu-id="0384c-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="0384c-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="0384c-186">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0384c-186">OUTPUTS</span></span>

### <span data-ttu-id="0384c-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span><span class="sxs-lookup"><span data-stu-id="0384c-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="0384c-188">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0384c-188">NOTES</span></span>

<span data-ttu-id="0384c-189">ALIASE</span><span class="sxs-lookup"><span data-stu-id="0384c-189">ALIASES</span></span>

<span data-ttu-id="0384c-190">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="0384c-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="0384c-191">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="0384c-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0384c-192">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="0384c-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="0384c-193">DRIVELIST <IDriveStatus[]>: Liste der Laufwerke, die den Auftrag umfassen.</span><span class="sxs-lookup"><span data-stu-id="0384c-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="0384c-194">`[BitLockerKey <String>]`: Der Zum Verschlüsseln des Laufwerks verwendete BitLocker-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="0384c-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="0384c-195">`[BytesSucceeded <Int64?>]`: Bytes, die erfolgreich für das Laufwerk übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="0384c-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="0384c-196">`[CopyStatus <String>]`: Detaillierter Status zum Datenübertragungsprozess.</span><span class="sxs-lookup"><span data-stu-id="0384c-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="0384c-197">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Übertragungszustand befindet.</span><span class="sxs-lookup"><span data-stu-id="0384c-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="0384c-198">`[DriveHeaderHash <String>]`: Der Hashwert der Laufwerkkopfüberschrift.</span><span class="sxs-lookup"><span data-stu-id="0384c-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="0384c-199">`[DriveId <String>]`: Die Seriennummer der Hardware des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="0384c-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="0384c-200">`[ErrorLogUri <String>]`: Ein URI, der auf den Blob verweist, der das Fehlerprotokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="0384c-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="0384c-201">`[ManifestFile <String>]`: Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="0384c-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="0384c-202">`[ManifestHash <String>]`: Der base16-codierte #A0 der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="0384c-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="0384c-203">`[ManifestUri <String>]`: Ein URI, der auf den Blob verweist, der die Laufwerkmanifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="0384c-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="0384c-204">`[PercentComplete <Int32?>]`: Prozentsatz abgeschlossen für das Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="0384c-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="0384c-205">`[State <DriveState?>]`: Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="0384c-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="0384c-206">`[VerboseLogUri <String>]`: Ein URI, der auf den Blob verweist, der das ausführliche Protokoll für den Datenübertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="0384c-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="0384c-207">INPUTOBJECT <IImportExportIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="0384c-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0384c-208">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="0384c-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0384c-209">`[JobName <String>]`: Der Name des Import-/Exportauftrags.</span><span class="sxs-lookup"><span data-stu-id="0384c-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="0384c-210">`[LocationName <String>]`: Der Name des Speicherorts.</span><span class="sxs-lookup"><span data-stu-id="0384c-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="0384c-211">Beispiel: West US oder westus.</span><span class="sxs-lookup"><span data-stu-id="0384c-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="0384c-212">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe innerhalb des Benutzerabonnements eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0384c-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="0384c-213">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="0384c-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="0384c-214">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0384c-214">RELATED LINKS</span></span>

