---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azscomputequota
schema: 2.0.0
ms.openlocfilehash: 81a7a64f1880e2ed9acb2fedd3f90df614f1619d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006897"
---
# <span data-ttu-id="874a1-101">Get-AzsComputeQuota</span><span class="sxs-lookup"><span data-stu-id="874a1-101">Get-AzsComputeQuota</span></span>

## <span data-ttu-id="874a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="874a1-102">SYNOPSIS</span></span>
<span data-ttu-id="874a1-103">Abrufen eines vorhandenen Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="874a1-103">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="874a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="874a1-104">SYNTAX</span></span>

### <span data-ttu-id="874a1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="874a1-105">List (Default)</span></span>
```
Get-AzsComputeQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="874a1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="874a1-106">Get</span></span>
```
Get-AzsComputeQuota -Name <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="874a1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="874a1-107">GetViaIdentity</span></span>
```
Get-AzsComputeQuota -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="874a1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="874a1-108">DESCRIPTION</span></span>
<span data-ttu-id="874a1-109">Abrufen eines vorhandenen Compute-Kontingents</span><span class="sxs-lookup"><span data-stu-id="874a1-109">Get an existing Compute Quota.</span></span>

## <span data-ttu-id="874a1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="874a1-110">EXAMPLES</span></span>

### <span data-ttu-id="874a1-111">Beispiel 1: Abrufen aller Compute-Kontingente</span><span class="sxs-lookup"><span data-stu-id="874a1-111">Example 1: Get All Compute Quotas</span></span>
```powershell
PS C:\> Get-AzsComputeQuota

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ascancompquota433
Location                           : local
Name                               : ascancompquota433
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 100
VirtualMachineCount                : 100
```

<span data-ttu-id="874a1-112">Führen `Get-AzsComputeQuota` Sie keine Parameter aus, um eine Liste aller Compute-Kontingente abzurufen.</span><span class="sxs-lookup"><span data-stu-id="874a1-112">Run `Get-AzsComputeQuota` with no parameters to get a list of all Compute Quotas.</span></span>

### <span data-ttu-id="874a1-113">Beispiel 2: Abrufen des Compute-Kontingents nach Name</span><span class="sxs-lookup"><span data-stu-id="874a1-113">Example 2: Get Compute Quota by Name</span></span>
```powershell
PS C:\> Get-AzsComputeQuota -Name ExampleComputeQuotaWithDefaultParameters

AvailabilitySetCount               : 10
CoresLimit                         : 100
Id                                 : /subscriptions/3ae476e5-83d3-429d-a450-2f4f2fc67c5e/providers/Microsoft.Compute.Ad
                                     min/locations/local/quotas/ExampleComputeQuotaWithDefaultParameters
Location                           : local
Name                               : ExampleComputeQuotaWithDefaultParameters
PremiumManagedDiskAndSnapshotSize  : 2048
StandardManagedDiskAndSnapshotSize : 2048
Type                               : Microsoft.Compute.Admin/quotas
VMScaleSetCount                    : 0
VirtualMachineCount                : 100
```

<span data-ttu-id="874a1-114">Geben Sie den Namen des Kontingents in der Befehlszeile an, um ein bestimmtes Kontingent abzurufen.</span><span class="sxs-lookup"><span data-stu-id="874a1-114">Specify the Quota's name on the command line to retrieve a specific quota.</span></span>

## <span data-ttu-id="874a1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="874a1-115">PARAMETERS</span></span>

### <span data-ttu-id="874a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="874a1-116">-DefaultProfile</span></span>
<span data-ttu-id="874a1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="874a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="874a1-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="874a1-118">-InputObject</span></span>
<span data-ttu-id="874a1-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="874a1-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="874a1-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="874a1-120">-Location</span></span>
<span data-ttu-id="874a1-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="874a1-121">Location of the resource.</span></span>

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

### <span data-ttu-id="874a1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="874a1-122">-Name</span></span>
<span data-ttu-id="874a1-123">Der Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="874a1-123">Name of the quota.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: QuotaName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="874a1-124">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="874a1-124">-SubscriptionId</span></span>
<span data-ttu-id="874a1-125">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="874a1-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="874a1-126">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="874a1-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="874a1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="874a1-127">CommonParameters</span></span>
<span data-ttu-id="874a1-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="874a1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="874a1-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="874a1-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="874a1-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="874a1-130">INPUTS</span></span>

### <span data-ttu-id="874a1-131">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="874a1-131">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="874a1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="874a1-132">OUTPUTS</span></span>

### <span data-ttu-id="874a1-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180209. IQuota</span><span class="sxs-lookup"><span data-stu-id="874a1-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20180209.IQuota</span></span>



## <span data-ttu-id="874a1-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="874a1-134">NOTES</span></span>

<span data-ttu-id="874a1-135">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="874a1-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="874a1-136">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="874a1-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="874a1-137">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="874a1-137">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="874a1-138">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="874a1-138">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="874a1-139">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="874a1-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="874a1-140">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="874a1-140">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="874a1-141">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="874a1-141">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="874a1-142">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="874a1-142">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="874a1-143">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="874a1-143">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="874a1-144">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="874a1-144">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="874a1-145">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="874a1-145">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="874a1-146">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="874a1-146">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="874a1-147">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="874a1-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="874a1-148">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="874a1-148">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="874a1-149">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="874a1-149">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="874a1-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="874a1-150">RELATED LINKS</span></span>

