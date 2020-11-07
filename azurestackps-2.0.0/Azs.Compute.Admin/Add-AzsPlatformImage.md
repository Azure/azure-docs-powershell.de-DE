---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/add-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: 127cbe1efb710fff04420590985e97ee72a196a9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842640"
---
# <span data-ttu-id="d1428-101">Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1428-101">Add-AzsPlatformImage</span></span>

## <span data-ttu-id="d1428-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1428-102">SYNOPSIS</span></span>
<span data-ttu-id="d1428-103">Erstellt ein neues Platt Form Abbild mit einem bestimmten Publisher, Angebot, SKUs und Version.</span><span class="sxs-lookup"><span data-stu-id="d1428-103">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="d1428-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1428-104">SYNTAX</span></span>

### <span data-ttu-id="d1428-105">Createexpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="d1428-105">CreateExpanded (Default)</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String>] [-BillingPartNumber <String>] [-DataDisks <IDataDisk[]>] [-OsType <OSType>]
 [-OsUri <String>] [-ProvisioningState <ProvisioningState>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1428-106">Erstellen</span><span class="sxs-lookup"><span data-stu-id="d1428-106">Create</span></span>
```
Add-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String>
 -NewImage <IPlatformImageParameters> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1428-107">CreateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1428-107">CreateViaIdentity</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> -NewImage <IPlatformImageParameters>
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1428-108">CreateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1428-108">CreateViaIdentityExpanded</span></span>
```
Add-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-BillingPartNumber <String>]
 [-DataDisks <IDataDisk[]>] [-OsType <OSType>] [-OsUri <String>] [-ProvisioningState <ProvisioningState>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1428-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1428-109">DESCRIPTION</span></span>
<span data-ttu-id="d1428-110">Erstellt ein neues Platt Form Abbild mit einem bestimmten Publisher, Angebot, SKUs und Version.</span><span class="sxs-lookup"><span data-stu-id="d1428-110">Creates a new platform image with given publisher, offer, skus and version.</span></span>

## <span data-ttu-id="d1428-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1428-111">EXAMPLES</span></span>

### <span data-ttu-id="d1428-112">Beispiel 1: Add-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1428-112">Example 1: Add-AzsPlatformImage</span></span>
```powershell
PS C:\> Add-AzsPlatformImage -Offer "asdf" -Publisher "asdf" -Sku "asdf" -Version "1.0.0" -OsType Windows -OsUri "https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https&sig=CKkE2r9MJc%2FK40PjRB5Tfz6DArxNd0akD90IvKJX95g%3D"

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
#Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="d1428-113">Hinzufügen eines Platt Form Bilds aus dem BLOB-Speicher</span><span class="sxs-lookup"><span data-stu-id="d1428-113">Add a Platform Image from Blob Storage.</span></span> <span data-ttu-id="d1428-114">Verwenden Sie die SasUri, um den Speicherort der PlatformImage anzugeben, oder verwenden Sie eine öffentlich zugängliche URL.</span><span class="sxs-lookup"><span data-stu-id="d1428-114">Use the a SasUri to specify the location of the PlatformImage, or use a publicly accessible URL.</span></span>

## <span data-ttu-id="d1428-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1428-115">PARAMETERS</span></span>

### <span data-ttu-id="d1428-116">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="d1428-116">Exception.Message</span></span>
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

### <span data-ttu-id="d1428-117">-BillingPartNumber</span><span class="sxs-lookup"><span data-stu-id="d1428-117">-BillingPartNumber</span></span>
<span data-ttu-id="d1428-118">Die Teilenummer wird verwendet, um die Software Kosten zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d1428-118">The part number is used to bill for software costs.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-119">-Datenträger</span><span class="sxs-lookup"><span data-stu-id="d1428-119">-DataDisks</span></span>
<span data-ttu-id="d1428-120">Datenträger, die vom Platt Form Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1428-120">Data disks used by the platform image.</span></span>
<span data-ttu-id="d1428-121">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Datenträgereigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d1428-121">To construct, see NOTES section for DATADISKS properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IDataDisk[]
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1428-122">-DefaultProfile</span></span>
<span data-ttu-id="d1428-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1428-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1428-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d1428-124">-InputObject</span></span>
<span data-ttu-id="d1428-125">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d1428-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: CreateViaIdentity, CreateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="d1428-126">-Location</span></span>
<span data-ttu-id="d1428-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d1428-127">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-128">-NewImage</span><span class="sxs-lookup"><span data-stu-id="d1428-128">-NewImage</span></span>
<span data-ttu-id="d1428-129">Parameter, die zum Erstellen eines neuen Platt Form Bilds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1428-129">Parameters used to create a new platform image.</span></span>
<span data-ttu-id="d1428-130">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für NEWIMAGE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="d1428-130">To construct, see NOTES section for NEWIMAGE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters
Parameter Sets: Create, CreateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d1428-131">-NoWait</span></span>
<span data-ttu-id="d1428-132">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d1428-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d1428-133">-Angebot</span><span class="sxs-lookup"><span data-stu-id="d1428-133">-Offer</span></span>
<span data-ttu-id="d1428-134">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="d1428-134">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-135">-OsType</span><span class="sxs-lookup"><span data-stu-id="d1428-135">-OsType</span></span>
<span data-ttu-id="d1428-136">Typ des Betriebssystems.</span><span class="sxs-lookup"><span data-stu-id="d1428-136">Operating system type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.OSType
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-137">-OsUri</span><span class="sxs-lookup"><span data-stu-id="d1428-137">-OsUri</span></span>
<span data-ttu-id="d1428-138">Speicherort des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="d1428-138">Location of the disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-139">-ProvisioningState</span><span class="sxs-lookup"><span data-stu-id="d1428-139">-ProvisioningState</span></span>
<span data-ttu-id="d1428-140">Bereitstellungsstatus des Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="d1428-140">Provisioning status of the platform image.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Support.ProvisioningState
Parameter Sets: CreateExpanded, CreateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-141">-Publisher</span><span class="sxs-lookup"><span data-stu-id="d1428-141">-Publisher</span></span>
<span data-ttu-id="d1428-142">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="d1428-142">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-143">-SKU</span><span class="sxs-lookup"><span data-stu-id="d1428-143">-Sku</span></span>
<span data-ttu-id="d1428-144">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="d1428-144">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-145">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d1428-145">-SubscriptionId</span></span>
<span data-ttu-id="d1428-146">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d1428-146">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d1428-147">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d1428-147">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-148">-Version</span><span class="sxs-lookup"><span data-stu-id="d1428-148">-Version</span></span>
<span data-ttu-id="d1428-149">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d1428-149">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Create, CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="d1428-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d1428-150">-Confirm</span></span>
<span data-ttu-id="d1428-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d1428-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1428-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1428-152">-WhatIf</span></span>
<span data-ttu-id="d1428-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d1428-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1428-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d1428-154">The cmdlet is not run.</span></span>

### <span data-ttu-id="d1428-155">Exception. Message</span><span class="sxs-lookup"><span data-stu-id="d1428-155">Exception.Message</span></span>

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

### <span data-ttu-id="d1428-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1428-156">CommonParameters</span></span>
<span data-ttu-id="d1428-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1428-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1428-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d1428-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1428-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1428-159">INPUTS</span></span>

### <span data-ttu-id="d1428-160">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImageParameters</span><span class="sxs-lookup"><span data-stu-id="d1428-160">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImageParameters</span></span>

### <span data-ttu-id="d1428-161">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="d1428-161">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="d1428-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1428-162">OUTPUTS</span></span>

### <span data-ttu-id="d1428-163">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="d1428-163">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="d1428-164">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1428-164">NOTES</span></span>

<span data-ttu-id="d1428-165">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d1428-165">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1428-166">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="d1428-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d1428-167">Datadisks <IDataDisk [] >: Datenlaufwerke, die vom Platt Form Abbild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1428-167">DATADISKS <IDataDisk[]>: Data disks used by the platform image.</span></span>
  - <span data-ttu-id="d1428-168">`[Lun <Int32?>]`: Logische Einheitsnummer.</span><span class="sxs-lookup"><span data-stu-id="d1428-168">`[Lun <Int32?>]`: Logical unit number.</span></span>
  - <span data-ttu-id="d1428-169">`[Uri <String>]`: Speicherort der Datenträger Vorlage</span><span class="sxs-lookup"><span data-stu-id="d1428-169">`[Uri <String>]`: Location of the disk template.</span></span>

<span data-ttu-id="d1428-170">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="d1428-170">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1428-171">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="d1428-171">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="d1428-172">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="d1428-172">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1428-173">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d1428-173">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="d1428-174">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="d1428-174">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="d1428-175">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="d1428-175">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="d1428-176">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="d1428-176">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="d1428-177">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="d1428-177">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="d1428-178">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="d1428-178">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="d1428-179">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d1428-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d1428-180">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d1428-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="d1428-181">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="d1428-181">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="d1428-182">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d1428-182">`[Version <String>]`: The version of the resource.</span></span>

<span data-ttu-id="d1428-183">NEWIMAGE <IPlatformImageParameters> : Parameter, die zum Erstellen eines neuen Platt Form Bilds verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1428-183">NEWIMAGE <IPlatformImageParameters>: Parameters used to create a new platform image.</span></span>
  - <span data-ttu-id="d1428-184">`[DataDisk <IDataDisk[]>]`: Datenlaufwerke, die vom Platt Form Bild verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d1428-184">`[DataDisk <IDataDisk[]>]`: Data disks used by the platform image.</span></span>
    - <span data-ttu-id="d1428-185">`[Lun <Int32?>]`: Logische Einheitsnummer.</span><span class="sxs-lookup"><span data-stu-id="d1428-185">`[Lun <Int32?>]`: Logical unit number.</span></span>
    - <span data-ttu-id="d1428-186">`[Uri <String>]`: Speicherort der Datenträger Vorlage</span><span class="sxs-lookup"><span data-stu-id="d1428-186">`[Uri <String>]`: Location of the disk template.</span></span>
  - <span data-ttu-id="d1428-187">`[DetailBillingPartNumber <String>]`: Die Teilenummer wird verwendet, um die Kosten für Software zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="d1428-187">`[DetailBillingPartNumber <String>]`: The part number is used to bill for software costs.</span></span>
  - <span data-ttu-id="d1428-188">`[OSDiskOstype <OSType?>]`: Betriebssystemtyp.</span><span class="sxs-lookup"><span data-stu-id="d1428-188">`[OSDiskOstype <OSType?>]`: Operating system type.</span></span>
  - <span data-ttu-id="d1428-189">`[OSDiskUri <String>]`: Speicherort des Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="d1428-189">`[OSDiskUri <String>]`: Location of the disk.</span></span>
  - <span data-ttu-id="d1428-190">`[ProvisioningState <ProvisioningState?>]`: Bereitstellungsstatus des Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="d1428-190">`[ProvisioningState <ProvisioningState?>]`: Provisioning status of the platform image.</span></span>

## <span data-ttu-id="d1428-191">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1428-191">RELATED LINKS</span></span>

