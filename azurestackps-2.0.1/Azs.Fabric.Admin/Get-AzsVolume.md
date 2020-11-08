---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsvolume
schema: 2.0.0
ms.openlocfilehash: a423470454e77c58a8b611a47c737e5d86bfd1cf
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005510"
---
# <span data-ttu-id="cc1e1-101">Get-AzsVolume</span><span class="sxs-lookup"><span data-stu-id="cc1e1-101">Get-AzsVolume</span></span>

## <span data-ttu-id="cc1e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cc1e1-102">SYNOPSIS</span></span>
<span data-ttu-id="cc1e1-103">Geben Sie das angeforderte Speichervolumen zurück.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-103">Return the requested a storage volume.</span></span>

## <span data-ttu-id="cc1e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc1e1-104">SYNTAX</span></span>

### <span data-ttu-id="cc1e1-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc1e1-105">List (Default)</span></span>
```
Get-AzsVolume -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>]
 [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="cc1e1-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="cc1e1-106">Get</span></span>
```
Get-AzsVolume -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="cc1e1-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cc1e1-107">GetViaIdentity</span></span>
```
Get-AzsVolume -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="cc1e1-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cc1e1-108">DESCRIPTION</span></span>
<span data-ttu-id="cc1e1-109">Geben Sie das angeforderte Speichervolumen zurück.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-109">Return the requested a storage volume.</span></span>

## <span data-ttu-id="cc1e1-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cc1e1-110">EXAMPLES</span></span>

### <span data-ttu-id="cc1e1-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="cc1e1-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="cc1e1-112">Sie erhalten eine Liste aller Speicher-Volumes an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-112">Get a list of all storage volumes at a given location.</span></span>

### <span data-ttu-id="cc1e1-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="cc1e1-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsVolume -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name ee594cf5-cf54-46b4-a641-139553307195
```

<span data-ttu-id="cc1e1-114">Besorgen Sie sich ein Speichervolumen nach Name an einem bestimmten Ort.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-114">Get a storage volume by name at a given location.</span></span>

## <span data-ttu-id="cc1e1-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc1e1-115">PARAMETERS</span></span>

### <span data-ttu-id="cc1e1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc1e1-116">-DefaultProfile</span></span>
<span data-ttu-id="cc1e1-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cc1e1-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="cc1e1-118">-Filter</span></span>
<span data-ttu-id="cc1e1-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="cc1e1-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cc1e1-120">-InputObject</span></span>
<span data-ttu-id="cc1e1-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="cc1e1-122">-Location</span></span>
<span data-ttu-id="cc1e1-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-123">Location of the resource.</span></span>

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

### <span data-ttu-id="cc1e1-124">-Name</span><span class="sxs-lookup"><span data-stu-id="cc1e1-124">-Name</span></span>
<span data-ttu-id="cc1e1-125">Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-125">Name of the storage volume.</span></span>

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

### <span data-ttu-id="cc1e1-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc1e1-126">-PassThru</span></span>
<span data-ttu-id="cc1e1-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="cc1e1-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="cc1e1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cc1e1-128">-ResourceGroupName</span></span>
<span data-ttu-id="cc1e1-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-129">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="cc1e1-130">-ScaleUnit</span></span>
<span data-ttu-id="cc1e1-131">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="cc1e1-131">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="cc1e1-132">-Skip</span></span>
<span data-ttu-id="cc1e1-133">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="cc1e1-133">OData skip parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="cc1e1-134">-StorageSubSystem</span></span>
<span data-ttu-id="cc1e1-135">Name des Speichersystems</span><span class="sxs-lookup"><span data-stu-id="cc1e1-135">Name of the storage system.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="cc1e1-136">-SubscriptionId</span></span>
<span data-ttu-id="cc1e1-137">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="cc1e1-138">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cc1e1-139">-Top</span><span class="sxs-lookup"><span data-stu-id="cc1e1-139">-Top</span></span>
<span data-ttu-id="cc1e1-140">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-140">OData top parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cc1e1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc1e1-141">CommonParameters</span></span>
<span data-ttu-id="cc1e1-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc1e1-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cc1e1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc1e1-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cc1e1-144">INPUTS</span></span>

### <span data-ttu-id="cc1e1-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cc1e1-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="cc1e1-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cc1e1-146">OUTPUTS</span></span>

### <span data-ttu-id="cc1e1-147">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20190501. IVolume</span><span class="sxs-lookup"><span data-stu-id="cc1e1-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IVolume</span></span>



## <span data-ttu-id="cc1e1-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="cc1e1-148">NOTES</span></span>

<span data-ttu-id="cc1e1-149">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cc1e1-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cc1e1-151">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="cc1e1-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cc1e1-152">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="cc1e1-153">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="cc1e1-154">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="cc1e1-155">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="cc1e1-156">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="cc1e1-157">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="cc1e1-158">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="cc1e1-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cc1e1-159">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="cc1e1-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="cc1e1-160">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="cc1e1-161">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="cc1e1-162">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="cc1e1-163">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="cc1e1-164">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="cc1e1-165">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="cc1e1-166">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="cc1e1-167">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="cc1e1-168">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="cc1e1-169">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="cc1e1-170">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="cc1e1-171">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="cc1e1-172">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cc1e1-173">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="cc1e1-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="cc1e1-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cc1e1-174">RELATED LINKS</span></span>

