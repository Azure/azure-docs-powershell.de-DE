---
external help file: ''
Module Name: Az.ImportExport
online version: https://docs.microsoft.com/en-us/powershell/module/az.importexport/update-azimportexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImportExport/help/Update-AzImportExport.md
ms.openlocfilehash: d6ed55cef91dc93f0ce9101adf94d9dc6931d07c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178005"
---
# <span data-ttu-id="43d54-101">Update-AzImportExport</span><span class="sxs-lookup"><span data-stu-id="43d54-101">Update-AzImportExport</span></span>

## <span data-ttu-id="43d54-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="43d54-102">SYNOPSIS</span></span>
<span data-ttu-id="43d54-103">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="43d54-103">Updates specific properties of a job.</span></span>
<span data-ttu-id="43d54-104">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, die den Import-oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="43d54-104">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="43d54-105">Sie kann auch verwendet werden, um einen vorhandenen Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="43d54-105">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="43d54-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="43d54-106">SYNTAX</span></span>

### <span data-ttu-id="43d54-107">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="43d54-107">UpdateExpanded (Default)</span></span>
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

### <span data-ttu-id="43d54-108">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43d54-108">UpdateViaIdentityExpanded</span></span>
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

## <span data-ttu-id="43d54-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="43d54-109">DESCRIPTION</span></span>
<span data-ttu-id="43d54-110">Aktualisiert bestimmte Eigenschaften eines Auftrags.</span><span class="sxs-lookup"><span data-stu-id="43d54-110">Updates specific properties of a job.</span></span>
<span data-ttu-id="43d54-111">Sie können diesen Vorgang aufrufen, um den Import/Export-Dienst zu benachrichtigen, dass die Festplatten, die den Import-oder Exportauftrag enthalten, an das Microsoft-Rechenzentrum ausgeliefert wurden.</span><span class="sxs-lookup"><span data-stu-id="43d54-111">You can call this operation to notify the Import/Export service that the hard drives comprising the import or export job have been shipped to the Microsoft data center.</span></span>
<span data-ttu-id="43d54-112">Sie kann auch verwendet werden, um einen vorhandenen Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="43d54-112">It can also be used to cancel an existing job.</span></span>

## <span data-ttu-id="43d54-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="43d54-113">EXAMPLES</span></span>

### <span data-ttu-id="43d54-114">Beispiel 1: Aktualisieren des DataObjects-Auftrags nach Ressourcengruppe und Servername</span><span class="sxs-lookup"><span data-stu-id="43d54-114">Example 1: Update ImportExport job by resource group and server name</span></span>
```powershell
PS C:\> Update-AzImportExport -Name test-job -ResourceGroupName ImportTestRG -DeliveryPackageCarrierName pwsh -DeliveryPackageTrackingNumber pwsh20200000
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="43d54-115">Dieses Cmdlet aktualisiert DataObjects Job nach Ressourcengruppe und Servername.</span><span class="sxs-lookup"><span data-stu-id="43d54-115">This cmdlet updates ImportExport job by resource group and server name.</span></span>

### <span data-ttu-id="43d54-116">Beispiel 2: Aktualisieren des DataObjects-Auftrags nach Identität.</span><span class="sxs-lookup"><span data-stu-id="43d54-116">Example 2: Update ImportExport job by identity.</span></span>
```powershell
PS C:\> Get-AzImportExport -Name test-job -ResourceGroupName ImportTestRG | Update-AzImportExport -CancelRequested
Location Name     Type
-------- ----     ----
East US  test-job Microsoft.ImportExport/jobs
```

<span data-ttu-id="43d54-117">Dieses Cmdlet aktualisiert DataObjects Job nach Identität.</span><span class="sxs-lookup"><span data-stu-id="43d54-117">This cmdlet updates ImportExport job by identity.</span></span>

## <span data-ttu-id="43d54-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="43d54-118">PARAMETERS</span></span>

### <span data-ttu-id="43d54-119">-AcceptLanguage</span><span class="sxs-lookup"><span data-stu-id="43d54-119">-AcceptLanguage</span></span>
<span data-ttu-id="43d54-120">Gibt die bevorzugte Sprache für die Antwort an.</span><span class="sxs-lookup"><span data-stu-id="43d54-120">Specifies the preferred language for the response.</span></span>

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

### <span data-ttu-id="43d54-121">-BackupDriveManifest</span><span class="sxs-lookup"><span data-stu-id="43d54-121">-BackupDriveManifest</span></span>
<span data-ttu-id="43d54-122">Gibt an, ob die Manifestdateien auf den Laufwerken kopiert werden sollen, um BLOBs zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="43d54-122">Indicates whether the manifest files on the drives should be copied to block blobs.</span></span>

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

### <span data-ttu-id="43d54-123">-CancelRequested</span><span class="sxs-lookup"><span data-stu-id="43d54-123">-CancelRequested</span></span>
<span data-ttu-id="43d54-124">Wenn angegeben, muss der Wert "true" sein.</span><span class="sxs-lookup"><span data-stu-id="43d54-124">If specified, the value must be true.</span></span>
<span data-ttu-id="43d54-125">Der Dienst versucht, den Auftrag abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="43d54-125">The service will attempt to cancel the job.</span></span>

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

### <span data-ttu-id="43d54-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43d54-126">-DefaultProfile</span></span>
<span data-ttu-id="43d54-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="43d54-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43d54-128">-DeliveryPackageCarrierName</span><span class="sxs-lookup"><span data-stu-id="43d54-128">-DeliveryPackageCarrierName</span></span>
<span data-ttu-id="43d54-129">Der Name des Netzbetreibers, der verwendet wird, um die Import-oder Export Laufwerke zu versenden.</span><span class="sxs-lookup"><span data-stu-id="43d54-129">The name of the carrier that is used to ship the import or export drives.</span></span>

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

### <span data-ttu-id="43d54-130">-DeliveryPackageDriveCount</span><span class="sxs-lookup"><span data-stu-id="43d54-130">-DeliveryPackageDriveCount</span></span>
<span data-ttu-id="43d54-131">Die Anzahl der Laufwerke, die im Paket enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="43d54-131">The number of drives included in the package.</span></span>

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

### <span data-ttu-id="43d54-132">-DeliveryPackageShipDate</span><span class="sxs-lookup"><span data-stu-id="43d54-132">-DeliveryPackageShipDate</span></span>
<span data-ttu-id="43d54-133">Das Datum, an dem das Paket ausgeliefert wird.</span><span class="sxs-lookup"><span data-stu-id="43d54-133">The date when the package is shipped.</span></span>

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

### <span data-ttu-id="43d54-134">-DeliveryPackageTrackingNumber</span><span class="sxs-lookup"><span data-stu-id="43d54-134">-DeliveryPackageTrackingNumber</span></span>
<span data-ttu-id="43d54-135">Die Nachverfolgungsnummer des Pakets.</span><span class="sxs-lookup"><span data-stu-id="43d54-135">The tracking number of the package.</span></span>

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

### <span data-ttu-id="43d54-136">-Drivelist</span><span class="sxs-lookup"><span data-stu-id="43d54-136">-DriveList</span></span>
<span data-ttu-id="43d54-137">Liste der Laufwerke, die den Auftrag umfassen.</span><span class="sxs-lookup"><span data-stu-id="43d54-137">List of drives that comprise the job.</span></span>
<span data-ttu-id="43d54-138">Wenn Sie das Konstrukt erstellen möchten, lesen Sie den Abschnitt "Notizen" für drivelist-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43d54-138">To construct, see NOTES section for DRIVELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d54-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="43d54-139">-InputObject</span></span>
<span data-ttu-id="43d54-140">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="43d54-140">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="43d54-141">-LogLevel</span><span class="sxs-lookup"><span data-stu-id="43d54-141">-LogLevel</span></span>
<span data-ttu-id="43d54-142">Gibt an, ob die Fehlerprotokollierung oder die ausführliche Protokollierung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="43d54-142">Indicates whether error logging or verbose logging is enabled.</span></span>

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

### <span data-ttu-id="43d54-143">-Name</span><span class="sxs-lookup"><span data-stu-id="43d54-143">-Name</span></span>
<span data-ttu-id="43d54-144">Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="43d54-144">The name of the import/export job.</span></span>

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

### <span data-ttu-id="43d54-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43d54-145">-ResourceGroupName</span></span>
<span data-ttu-id="43d54-146">Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="43d54-146">The resource group name uniquely identifies the resource group within the user subscription.</span></span>

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

### <span data-ttu-id="43d54-147">-ReturnAddressCity</span><span class="sxs-lookup"><span data-stu-id="43d54-147">-ReturnAddressCity</span></span>
<span data-ttu-id="43d54-148">Der Name der Stadt, die beim Zurückgeben der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-148">The city name to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-149">-ReturnAddressCountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="43d54-149">-ReturnAddressCountryOrRegion</span></span>
<span data-ttu-id="43d54-150">Das Land oder die Region, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-150">The country or region to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-151">-ReturnAddressEmail</span><span class="sxs-lookup"><span data-stu-id="43d54-151">-ReturnAddressEmail</span></span>
<span data-ttu-id="43d54-152">Die e-Mail-Adresse des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="43d54-152">Email address of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="43d54-153">-ReturnAddressPhone</span><span class="sxs-lookup"><span data-stu-id="43d54-153">-ReturnAddressPhone</span></span>
<span data-ttu-id="43d54-154">Die Telefonnummer des Empfängers der zurückgegebenen Laufwerke.</span><span class="sxs-lookup"><span data-stu-id="43d54-154">Phone number of the recipient of the returned drives.</span></span>

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

### <span data-ttu-id="43d54-155">-ReturnAddressPostalCode</span><span class="sxs-lookup"><span data-stu-id="43d54-155">-ReturnAddressPostalCode</span></span>
<span data-ttu-id="43d54-156">Die Postleitzahl, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-156">The postal code to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-157">-ReturnAddressRecipientName</span><span class="sxs-lookup"><span data-stu-id="43d54-157">-ReturnAddressRecipientName</span></span>
<span data-ttu-id="43d54-158">Der Name des Empfängers, der die Festplatten empfängt, wenn er zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="43d54-158">The name of the recipient who will receive the hard drives when they are returned.</span></span>

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

### <span data-ttu-id="43d54-159">-ReturnAddressStateOrProvince</span><span class="sxs-lookup"><span data-stu-id="43d54-159">-ReturnAddressStateOrProvince</span></span>
<span data-ttu-id="43d54-160">Das Bundesland, das bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-160">The state or province to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-161">-ReturnAddressStreetAddress1</span><span class="sxs-lookup"><span data-stu-id="43d54-161">-ReturnAddressStreetAddress1</span></span>
<span data-ttu-id="43d54-162">Die erste Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-162">The first line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-163">-ReturnAddressStreetAddress2</span><span class="sxs-lookup"><span data-stu-id="43d54-163">-ReturnAddressStreetAddress2</span></span>
<span data-ttu-id="43d54-164">Die zweite Zeile der Straßenadresse, die bei der Rückgabe der Laufwerke verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="43d54-164">The second line of the street address to use when returning the drives.</span></span>

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

### <span data-ttu-id="43d54-165">-ReturnShippingCarrierAccountNumber</span><span class="sxs-lookup"><span data-stu-id="43d54-165">-ReturnShippingCarrierAccountNumber</span></span>
<span data-ttu-id="43d54-166">Die Kontonummer des Kunden beim Netzbetreiber.</span><span class="sxs-lookup"><span data-stu-id="43d54-166">The customer's account number with the carrier.</span></span>

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

### <span data-ttu-id="43d54-167">-ReturnShippingCarrierName</span><span class="sxs-lookup"><span data-stu-id="43d54-167">-ReturnShippingCarrierName</span></span>
<span data-ttu-id="43d54-168">Der Name des Netzbetreibers.</span><span class="sxs-lookup"><span data-stu-id="43d54-168">The carrier's name.</span></span>

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

### <span data-ttu-id="43d54-169">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="43d54-169">-State</span></span>
<span data-ttu-id="43d54-170">Wenn angegeben, muss der Wert Versand sein, wodurch der Import/Export-Dienst angewiesen wird, dass das Paket für den Auftrag ausgeliefert wurde.</span><span class="sxs-lookup"><span data-stu-id="43d54-170">If specified, the value must be Shipping, which tells the Import/Export service that the package for the job has been shipped.</span></span>
<span data-ttu-id="43d54-171">Die Eigenschaften ReturnAddress und DeliveryPackage müssen entweder in dieser Anforderung oder in einer vorherigen Anforderung gesetzt worden sein, da andernfalls die Anforderung fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="43d54-171">The ReturnAddress and DeliveryPackage properties must have been set either in this request or in a previous request, otherwise the request will fail.</span></span>

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

### <span data-ttu-id="43d54-172">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="43d54-172">-SubscriptionId</span></span>
<span data-ttu-id="43d54-173">Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="43d54-173">The subscription ID for the Azure user.</span></span>

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

### <span data-ttu-id="43d54-174">-Tag</span><span class="sxs-lookup"><span data-stu-id="43d54-174">-Tag</span></span>
<span data-ttu-id="43d54-175">Gibt die Tags an, die dem Auftrag zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="43d54-175">Specifies the tags that will be assigned to the job</span></span>

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

### <span data-ttu-id="43d54-176">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="43d54-176">-Confirm</span></span>
<span data-ttu-id="43d54-177">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="43d54-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43d54-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43d54-178">-WhatIf</span></span>
<span data-ttu-id="43d54-179">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="43d54-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43d54-180">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="43d54-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43d54-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43d54-181">CommonParameters</span></span>
<span data-ttu-id="43d54-182">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43d54-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43d54-183">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43d54-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43d54-184">Eingaben</span><span class="sxs-lookup"><span data-stu-id="43d54-184">INPUTS</span></span>

### <span data-ttu-id="43d54-185">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. IImportExportIdentity</span><span class="sxs-lookup"><span data-stu-id="43d54-185">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.IImportExportIdentity</span></span>

## <span data-ttu-id="43d54-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="43d54-186">OUTPUTS</span></span>

### <span data-ttu-id="43d54-187">Microsoft. Azure. PowerShell. Cmdlets. DataObjects. Models. Api20161101. IJobResponse</span><span class="sxs-lookup"><span data-stu-id="43d54-187">Microsoft.Azure.PowerShell.Cmdlets.ImportExport.Models.Api20161101.IJobResponse</span></span>

## <span data-ttu-id="43d54-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="43d54-188">NOTES</span></span>

<span data-ttu-id="43d54-189">Aliase</span><span class="sxs-lookup"><span data-stu-id="43d54-189">ALIASES</span></span>

<span data-ttu-id="43d54-190">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="43d54-190">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="43d54-191">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="43d54-191">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43d54-192">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="43d54-192">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="43d54-193">Drivelist <IDriveStatus [] >: Liste der Laufwerke, aus denen sich der Auftrag zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="43d54-193">DRIVELIST <IDriveStatus[]>: List of drives that comprise the job.</span></span>
  - <span data-ttu-id="43d54-194">`[BitLockerKey <String>]`: Der BitLocker-Schlüssel, der zum Verschlüsseln des Laufwerks verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43d54-194">`[BitLockerKey <String>]`: The BitLocker key used to encrypt the drive.</span></span>
  - <span data-ttu-id="43d54-195">`[BytesSucceeded <Int64?>]`: Bytes, die für das Laufwerk erfolgreich übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="43d54-195">`[BytesSucceeded <Int64?>]`: Bytes successfully transferred for the drive.</span></span>
  - <span data-ttu-id="43d54-196">`[CopyStatus <String>]`: Detaillierter Status zum Datentransferprozess.</span><span class="sxs-lookup"><span data-stu-id="43d54-196">`[CopyStatus <String>]`: Detailed status about the data transfer process.</span></span> <span data-ttu-id="43d54-197">Dieses Feld wird in der Antwort erst zurückgegeben, wenn sich das Laufwerk im Status "übertragen" befindet.</span><span class="sxs-lookup"><span data-stu-id="43d54-197">This field is not returned in the response until the drive is in the Transferring state.</span></span>
  - <span data-ttu-id="43d54-198">`[DriveHeaderHash <String>]`: Der Hashwert des Laufwerk Headers.</span><span class="sxs-lookup"><span data-stu-id="43d54-198">`[DriveHeaderHash <String>]`: The drive header hash value.</span></span>
  - <span data-ttu-id="43d54-199">`[DriveId <String>]`: Die Hardware-Seriennummer des Laufwerks ohne Leerzeichen.</span><span class="sxs-lookup"><span data-stu-id="43d54-199">`[DriveId <String>]`: The drive's hardware serial number, without spaces.</span></span>
  - <span data-ttu-id="43d54-200">`[ErrorLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das Fehlerprotokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="43d54-200">`[ErrorLogUri <String>]`: A URI that points to the blob containing the error log for the data transfer operation.</span></span>
  - <span data-ttu-id="43d54-201">`[ManifestFile <String>]`: Der relative Pfad der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="43d54-201">`[ManifestFile <String>]`: The relative path of the manifest file on the drive.</span></span> 
  - <span data-ttu-id="43d54-202">`[ManifestHash <String>]`: Der Base16-codierte MD5-Hash der Manifestdatei auf dem Laufwerk.</span><span class="sxs-lookup"><span data-stu-id="43d54-202">`[ManifestHash <String>]`: The Base16-encoded MD5 hash of the manifest file on the drive.</span></span>
  - <span data-ttu-id="43d54-203">`[ManifestUri <String>]`: Ein URI, der auf das BLOB verweist, das die Laufwerk Manifestdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="43d54-203">`[ManifestUri <String>]`: A URI that points to the blob containing the drive manifest file.</span></span> 
  - <span data-ttu-id="43d54-204">`[PercentComplete <Int32?>]`: Prozentsatz für das Laufwerk abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="43d54-204">`[PercentComplete <Int32?>]`: Percentage completed for the drive.</span></span> 
  - <span data-ttu-id="43d54-205">`[State <DriveState?>]`: Der aktuelle Zustand des Laufwerks.</span><span class="sxs-lookup"><span data-stu-id="43d54-205">`[State <DriveState?>]`: The drive's current state.</span></span> 
  - <span data-ttu-id="43d54-206">`[VerboseLogUri <String>]`: Ein URI, der auf das BLOB verweist, das das ausführliche Protokoll für den Daten Übertragungsvorgang enthält.</span><span class="sxs-lookup"><span data-stu-id="43d54-206">`[VerboseLogUri <String>]`: A URI that points to the blob containing the verbose log for the data transfer operation.</span></span> 

<span data-ttu-id="43d54-207">Inputobject <IImportExportIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="43d54-207">INPUTOBJECT <IImportExportIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43d54-208">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="43d54-208">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43d54-209">`[JobName <String>]`: Der Name des Import/Export-Auftrags.</span><span class="sxs-lookup"><span data-stu-id="43d54-209">`[JobName <String>]`: The name of the import/export job.</span></span>
  - <span data-ttu-id="43d54-210">`[LocationName <String>]`: Der Name des Standorts.</span><span class="sxs-lookup"><span data-stu-id="43d54-210">`[LocationName <String>]`: The name of the location.</span></span> <span data-ttu-id="43d54-211">Beispielsweise West-US oder westus.</span><span class="sxs-lookup"><span data-stu-id="43d54-211">For example, West US or westus.</span></span>
  - <span data-ttu-id="43d54-212">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe identifiziert die Ressourcengruppe eindeutig innerhalb des Benutzer Abonnements.</span><span class="sxs-lookup"><span data-stu-id="43d54-212">`[ResourceGroupName <String>]`: The resource group name uniquely identifies the resource group within the user subscription.</span></span>
  - <span data-ttu-id="43d54-213">`[SubscriptionId <String>]`: Die Abonnement-ID für den Azure-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="43d54-213">`[SubscriptionId <String>]`: The subscription ID for the Azure user.</span></span>

## <span data-ttu-id="43d54-214">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="43d54-214">RELATED LINKS</span></span>

