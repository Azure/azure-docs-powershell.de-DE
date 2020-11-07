---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsdrive
schema: 2.0.0
ms.openlocfilehash: ec2216a9234086702e8a9331888c04034d13a99f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844800"
---
# <span data-ttu-id="dc632-101">Get-AzsDrive</span><span class="sxs-lookup"><span data-stu-id="dc632-101">Get-AzsDrive</span></span>

## <span data-ttu-id="dc632-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dc632-102">SYNOPSIS</span></span>
<span data-ttu-id="dc632-103">Geben Sie das angeforderte Speicherlaufwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="dc632-103">Return the requested a storage drive.</span></span>

## <span data-ttu-id="dc632-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dc632-104">SYNTAX</span></span>

### <span data-ttu-id="dc632-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dc632-105">List (Default)</span></span>
```
Get-AzsDrive -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="dc632-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dc632-106">Get</span></span>
```
Get-AzsDrive -Name <String> -ScaleUnit <String> -StorageSubSystem <String> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="dc632-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dc632-107">GetViaIdentity</span></span>
```
Get-AzsDrive -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

## <span data-ttu-id="dc632-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dc632-108">DESCRIPTION</span></span>
<span data-ttu-id="dc632-109">Geben Sie das angeforderte Speicherlaufwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="dc632-109">Return the requested a storage drive.</span></span>

## <span data-ttu-id="dc632-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dc632-110">EXAMPLES</span></span>

### <span data-ttu-id="dc632-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="dc632-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name
```

<span data-ttu-id="dc632-112">Abrufen einer Liste aller Speicherlaufwerke für einen bestimmten Cluster</span><span class="sxs-lookup"><span data-stu-id="dc632-112">Get a list of all storage drives for a given cluster.</span></span>

### <span data-ttu-id="dc632-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="dc632-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> $storageSubSystem = Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
PS C:\> Get-AzsDrive -ScaleUnit $scaleUnit.Name -StorageSubSystem $storageSubSystem.Name -Name '{a185d466-4d21-4c1f-9489-7c9c66b6b172}:PD:{fd389cf7-2115-2144-5afe-27910562d6b3}'
```

<span data-ttu-id="dc632-114">Besorgen Sie sich ein Speicherlaufwerk nach Namen für einen bestimmten Cluster.</span><span class="sxs-lookup"><span data-stu-id="dc632-114">Get a storage drive by name for a given cluster.</span></span>

## <span data-ttu-id="dc632-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dc632-115">PARAMETERS</span></span>

### <span data-ttu-id="dc632-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc632-116">-DefaultProfile</span></span>
<span data-ttu-id="dc632-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dc632-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc632-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="dc632-118">-Filter</span></span>
<span data-ttu-id="dc632-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="dc632-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="dc632-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dc632-120">-InputObject</span></span>
<span data-ttu-id="dc632-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="dc632-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dc632-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="dc632-122">-Location</span></span>
<span data-ttu-id="dc632-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="dc632-123">Location of the resource.</span></span>

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

### <span data-ttu-id="dc632-124">-Name</span><span class="sxs-lookup"><span data-stu-id="dc632-124">-Name</span></span>
<span data-ttu-id="dc632-125">Name des Speicherlaufwerks</span><span class="sxs-lookup"><span data-stu-id="dc632-125">Name of the storage drive.</span></span>

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

### <span data-ttu-id="dc632-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dc632-126">-PassThru</span></span>
<span data-ttu-id="dc632-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="dc632-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="dc632-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc632-128">-ResourceGroupName</span></span>
<span data-ttu-id="dc632-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc632-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="dc632-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="dc632-130">-ScaleUnit</span></span>
<span data-ttu-id="dc632-131">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="dc632-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="dc632-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="dc632-132">-Skip</span></span>
<span data-ttu-id="dc632-133">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc632-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="dc632-134">-StorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="dc632-134">-StorageSubSystem</span></span>
<span data-ttu-id="dc632-135">Name des Speichersystems</span><span class="sxs-lookup"><span data-stu-id="dc632-135">Name of the storage system.</span></span>

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

### <span data-ttu-id="dc632-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="dc632-136">-SubscriptionId</span></span>
<span data-ttu-id="dc632-137">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dc632-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dc632-138">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc632-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="dc632-139">-Top</span><span class="sxs-lookup"><span data-stu-id="dc632-139">-Top</span></span>
<span data-ttu-id="dc632-140">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="dc632-140">OData top parameter.</span></span>

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

### <span data-ttu-id="dc632-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc632-141">CommonParameters</span></span>
<span data-ttu-id="dc632-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc632-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc632-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc632-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc632-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dc632-144">INPUTS</span></span>

### <span data-ttu-id="dc632-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="dc632-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="dc632-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dc632-146">OUTPUTS</span></span>

### <span data-ttu-id="dc632-147">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20190501. IDrive</span><span class="sxs-lookup"><span data-stu-id="dc632-147">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20190501.IDrive</span></span>



## <span data-ttu-id="dc632-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="dc632-148">NOTES</span></span>

<span data-ttu-id="dc632-149">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dc632-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dc632-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="dc632-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="dc632-151">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="dc632-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dc632-152">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="dc632-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="dc632-153">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="dc632-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="dc632-154">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="dc632-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="dc632-155">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="dc632-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="dc632-156">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="dc632-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="dc632-157">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="dc632-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="dc632-158">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="dc632-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dc632-159">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="dc632-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="dc632-160">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="dc632-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="dc632-161">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="dc632-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="dc632-162">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="dc632-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="dc632-163">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="dc632-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="dc632-164">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="dc632-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="dc632-165">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="dc632-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="dc632-166">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dc632-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="dc632-167">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="dc632-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="dc632-168">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="dc632-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="dc632-169">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="dc632-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="dc632-170">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="dc632-170">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="dc632-171">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dc632-171">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dc632-172">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="dc632-172">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dc632-173">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="dc632-173">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="dc632-174">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dc632-174">RELATED LINKS</span></span>

