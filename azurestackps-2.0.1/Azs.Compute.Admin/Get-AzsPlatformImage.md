---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsplatformimage
schema: 2.0.0
ms.openlocfilehash: d91e930c486fea5c7a17e5a8f7d8f8d30a88b351
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005476"
---
# <span data-ttu-id="89165-101">Get-AzsPlatformImage</span><span class="sxs-lookup"><span data-stu-id="89165-101">Get-AzsPlatformImage</span></span>

## <span data-ttu-id="89165-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="89165-102">SYNOPSIS</span></span>
<span data-ttu-id="89165-103">Gibt das spezifische Platt Form Bild zurück, das Publisher, offer, SKUs und Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="89165-103">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="89165-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="89165-104">SYNTAX</span></span>

### <span data-ttu-id="89165-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="89165-105">List (Default)</span></span>
```
Get-AzsPlatformImage [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="89165-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="89165-106">Get</span></span>
```
Get-AzsPlatformImage -Offer <String> -Publisher <String> -Sku <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="89165-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="89165-107">GetViaIdentity</span></span>
```
Get-AzsPlatformImage -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="89165-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="89165-108">DESCRIPTION</span></span>
<span data-ttu-id="89165-109">Gibt das spezifische Platt Form Bild zurück, das Publisher, offer, SKUs und Version entspricht.</span><span class="sxs-lookup"><span data-stu-id="89165-109">Returns the specific platform image matching publisher, offer, skus and version.</span></span>

## <span data-ttu-id="89165-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="89165-110">EXAMPLES</span></span>

### <span data-ttu-id="89165-111">Beispiel 1: Abrufen aller Platt Form Bilder</span><span class="sxs-lookup"><span data-stu-id="89165-111">Example 1: Get All Platform Images</span></span>
```powershell
PS C:\> Get-AzsPlatformImage

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/loc
                    al/artifactTypes/platformImage/publishers/asdf/offers/asdf/skus/asdf/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=r
                    wdlacup&se=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="89165-112">Rufen Sie eine Liste aller Platt Form Bilder ab, indem Sie alle Parameter leer lassen.</span><span class="sxs-lookup"><span data-stu-id="89165-112">Get a list of all Platform Images by leaving all parameters blank.</span></span>

### <span data-ttu-id="89165-113">Beispiel 2: Abrufen eines bestimmten Platt Form Bilds</span><span class="sxs-lookup"><span data-stu-id="89165-113">Example 2: Get Specific Platform Image</span></span>
```powershell
PS C:\> Get-AzsPlatformImage -Offer ExampleOffer -Publisher ExamplePublisher -Location local -Sku ExampleSku -Version 1.0.0

BillingPartNumber :
DataDisks         :
Id                : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Admin/locations/local/artifa
                    ctTypes/platformImage/publishers/ExamplePublisher/offers/ExampleOffer/skus/ExampleSku/versions/1.0.0
Location          : local
Name              :
OsType            : Windows
OsUri             : https://asdf.blob.local.azurestack.external/asdf/UbuntuServer.vhd?sv=2017-04-17&ss=bqt&srt=sco&sp=rwdlacup&s
                    e=2020-02-13T13:25:58Z&st=2020-02-13T05:25:58Z&spr=https
ProvisioningState : Succeeded
Type              : Microsoft.Compute.Admin/locations/artifactTypes/publishers/offers/skus/versions
```

<span data-ttu-id="89165-114">Geben Sie das Angebot, den Herausgeber, den Standort, die SKU und die Version an, um ein Platt Form Abbild abzurufen.</span><span class="sxs-lookup"><span data-stu-id="89165-114">Specify the Offer, Publisher, Location, Sku, and Version to retrieve a Platform Image.</span></span>

## <span data-ttu-id="89165-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="89165-115">PARAMETERS</span></span>

### <span data-ttu-id="89165-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89165-116">-DefaultProfile</span></span>
<span data-ttu-id="89165-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="89165-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89165-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="89165-118">-InputObject</span></span>
<span data-ttu-id="89165-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="89165-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="89165-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="89165-120">-Location</span></span>
<span data-ttu-id="89165-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="89165-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-122">-Angebot</span><span class="sxs-lookup"><span data-stu-id="89165-122">-Offer</span></span>
<span data-ttu-id="89165-123">Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="89165-123">Name of the offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-124">-Publisher</span><span class="sxs-lookup"><span data-stu-id="89165-124">-Publisher</span></span>
<span data-ttu-id="89165-125">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="89165-125">Name of the publisher.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-126">-SKU</span><span class="sxs-lookup"><span data-stu-id="89165-126">-Sku</span></span>
<span data-ttu-id="89165-127">Der Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="89165-127">Name of the SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="89165-128">-SubscriptionId</span></span>
<span data-ttu-id="89165-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="89165-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="89165-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="89165-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-131">-Version</span><span class="sxs-lookup"><span data-stu-id="89165-131">-Version</span></span>
<span data-ttu-id="89165-132">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="89165-132">The version of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="89165-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89165-133">CommonParameters</span></span>
<span data-ttu-id="89165-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89165-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89165-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="89165-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89165-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="89165-136">INPUTS</span></span>

### <span data-ttu-id="89165-137">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="89165-137">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="89165-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="89165-138">OUTPUTS</span></span>

### <span data-ttu-id="89165-139">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IPlatformImage</span><span class="sxs-lookup"><span data-stu-id="89165-139">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IPlatformImage</span></span>



## <span data-ttu-id="89165-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="89165-140">NOTES</span></span>

<span data-ttu-id="89165-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="89165-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="89165-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="89165-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="89165-143">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="89165-143">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="89165-144">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="89165-144">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="89165-145">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="89165-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="89165-146">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="89165-146">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="89165-147">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="89165-147">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="89165-148">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="89165-148">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="89165-149">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="89165-149">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="89165-150">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="89165-150">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="89165-151">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="89165-151">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="89165-152">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="89165-152">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="89165-153">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="89165-153">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="89165-154">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="89165-154">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="89165-155">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="89165-155">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="89165-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="89165-156">RELATED LINKS</span></span>

