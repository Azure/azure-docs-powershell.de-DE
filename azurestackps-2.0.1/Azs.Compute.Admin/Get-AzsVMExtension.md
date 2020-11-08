---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/get-azsvmextension
schema: 2.0.0
ms.openlocfilehash: c2214f01b35e68ba22f9dbfc6fe9e602badb9ba9
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005578"
---
# <span data-ttu-id="8bd83-101">Get-AzsVMExtension</span><span class="sxs-lookup"><span data-stu-id="8bd83-101">Get-AzsVMExtension</span></span>

## <span data-ttu-id="8bd83-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8bd83-102">SYNOPSIS</span></span>
<span data-ttu-id="8bd83-103">Gibt den angeforderten Virtual Machine Extension-Bildabgleich mit Publisher, Typ, Version zurück.</span><span class="sxs-lookup"><span data-stu-id="8bd83-103">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="8bd83-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8bd83-104">SYNTAX</span></span>

### <span data-ttu-id="8bd83-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="8bd83-105">List (Default)</span></span>
```
Get-AzsVMExtension [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="8bd83-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="8bd83-106">Get</span></span>
```
Get-AzsVMExtension -Publisher <String> -Type <String> -Version <String> [-Location <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8bd83-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8bd83-107">GetViaIdentity</span></span>
```
Get-AzsVMExtension -InputObject <IComputeAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="8bd83-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8bd83-108">DESCRIPTION</span></span>
<span data-ttu-id="8bd83-109">Gibt den angeforderten Virtual Machine Extension-Bildabgleich mit Publisher, Typ, Version zurück.</span><span class="sxs-lookup"><span data-stu-id="8bd83-109">Returns requested Virtual Machine Extension Image matching publisher, type, version.</span></span>

## <span data-ttu-id="8bd83-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8bd83-110">EXAMPLES</span></span>

### <span data-ttu-id="8bd83-111">Beispiel 1: Abrufen aller VM-Erweiterungen</span><span class="sxs-lookup"><span data-stu-id="8bd83-111">Example 1:  Get All VM Extensions</span></span>
```powershell
PS C:\> Get-AzsVMExtension

ExtensionType            : IaaSDiagnostics
TypeHandlerVersion       : 1.11.3.12
ComputeRole              : IaaS
Id                       : /subscriptions/74c72bdc-d917-431c-a377-8ca80f4238a0/providers/Microsoft.Compute.Admin/locati
                           ons/northwest/artifactTypes/VMExtension/publishers/Microsoft.Azure.Diagnostics/types/IaaSDia
                           gnostics/versions/1.11.3.12
IsSystemExtension        : False
Location                 : northwest
Name                     :
ProvisioningState        : Succeeded
Publisher                : Microsoft.Azure.Diagnostics
SourceBlobUri            :
SupportMultipleExtension : False
Type                     : Microsoft.Compute.Admin/locations/artifactTypes/publishers/types/versions
VMScaleSetEnabled        : False
VmosType                 : Windows

...
```

<span data-ttu-id="8bd83-112">Rufen Sie eine Liste aller VMExtensions ab, indem Sie alle Parameter leer lassen.</span><span class="sxs-lookup"><span data-stu-id="8bd83-112">Get a list of all VMExtensions by leaving all parameters blank.</span></span>

## <span data-ttu-id="8bd83-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8bd83-113">PARAMETERS</span></span>

### <span data-ttu-id="8bd83-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bd83-114">-DefaultProfile</span></span>
<span data-ttu-id="8bd83-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8bd83-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8bd83-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8bd83-116">-InputObject</span></span>
<span data-ttu-id="8bd83-117">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8bd83-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8bd83-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="8bd83-118">-Location</span></span>
<span data-ttu-id="8bd83-119">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8bd83-119">Location of the resource.</span></span>

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

### <span data-ttu-id="8bd83-120">-Publisher</span><span class="sxs-lookup"><span data-stu-id="8bd83-120">-Publisher</span></span>
<span data-ttu-id="8bd83-121">Der Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="8bd83-121">Name of the publisher.</span></span>

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

### <span data-ttu-id="8bd83-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8bd83-122">-SubscriptionId</span></span>
<span data-ttu-id="8bd83-123">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8bd83-123">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8bd83-124">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8bd83-124">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8bd83-125">-Typ</span><span class="sxs-lookup"><span data-stu-id="8bd83-125">-Type</span></span>
<span data-ttu-id="8bd83-126">Der Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8bd83-126">Type of extension.</span></span>

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

### <span data-ttu-id="8bd83-127">-Version</span><span class="sxs-lookup"><span data-stu-id="8bd83-127">-Version</span></span>
<span data-ttu-id="8bd83-128">Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8bd83-128">The version of the resource.</span></span>

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

### <span data-ttu-id="8bd83-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bd83-129">CommonParameters</span></span>
<span data-ttu-id="8bd83-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8bd83-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bd83-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8bd83-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bd83-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8bd83-132">INPUTS</span></span>

### <span data-ttu-id="8bd83-133">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. IComputeAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8bd83-133">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.IComputeAdminIdentity</span></span>

## <span data-ttu-id="8bd83-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8bd83-134">OUTPUTS</span></span>

### <span data-ttu-id="8bd83-135">Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20151201Preview. IVMExtension</span><span class="sxs-lookup"><span data-stu-id="8bd83-135">Microsoft.Azure.PowerShell.Cmdlets.ComputeAdmin.Models.Api20151201Preview.IVMExtension</span></span>



## <span data-ttu-id="8bd83-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8bd83-136">NOTES</span></span>

<span data-ttu-id="8bd83-137">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8bd83-137">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8bd83-138">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8bd83-138">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8bd83-139">Inputobject <IComputeAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8bd83-139">INPUTOBJECT <IComputeAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8bd83-140">`[DiskId <String>]`: Die Datenträger-GUID als Identität.</span><span class="sxs-lookup"><span data-stu-id="8bd83-140">`[DiskId <String>]`: The disk guid as identity.</span></span>
  - <span data-ttu-id="8bd83-141">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8bd83-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8bd83-142">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8bd83-142">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8bd83-143">`[MigrationId <String>]`: Der GUID-Name des Migrationsauftrags.</span><span class="sxs-lookup"><span data-stu-id="8bd83-143">`[MigrationId <String>]`: The migration job guid name.</span></span>
  - <span data-ttu-id="8bd83-144">`[Offer <String>]`: Name des Angebots.</span><span class="sxs-lookup"><span data-stu-id="8bd83-144">`[Offer <String>]`: Name of the offer.</span></span>
  - <span data-ttu-id="8bd83-145">`[Publisher <String>]`: Name des Herausgebers.</span><span class="sxs-lookup"><span data-stu-id="8bd83-145">`[Publisher <String>]`: Name of the publisher.</span></span>
  - <span data-ttu-id="8bd83-146">`[QuotaName <String>]`: Name des Kontingents.</span><span class="sxs-lookup"><span data-stu-id="8bd83-146">`[QuotaName <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8bd83-147">`[Sku <String>]`: Name der SKU.</span><span class="sxs-lookup"><span data-stu-id="8bd83-147">`[Sku <String>]`: Name of the SKU.</span></span>
  - <span data-ttu-id="8bd83-148">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8bd83-148">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8bd83-149">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8bd83-149">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8bd83-150">`[Type <String>]`: Typ der Erweiterung.</span><span class="sxs-lookup"><span data-stu-id="8bd83-150">`[Type <String>]`: Type of extension.</span></span>
  - <span data-ttu-id="8bd83-151">`[Version <String>]`: Die Version der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8bd83-151">`[Version <String>]`: The version of the resource.</span></span>

## <span data-ttu-id="8bd83-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8bd83-152">RELATED LINKS</span></span>

