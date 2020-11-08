---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsippool
schema: 2.0.0
ms.openlocfilehash: 532dcd2a91591b639b93b5b67851a4118457068b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005474"
---
# <span data-ttu-id="0a6dc-101">Get-AzsIPPool</span><span class="sxs-lookup"><span data-stu-id="0a6dc-101">Get-AzsIPPool</span></span>

## <span data-ttu-id="0a6dc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a6dc-102">SYNOPSIS</span></span>
<span data-ttu-id="0a6dc-103">Geben Sie den angeforderten IP-Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-103">Return the requested IP pool.</span></span>

## <span data-ttu-id="0a6dc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a6dc-104">SYNTAX</span></span>

### <span data-ttu-id="0a6dc-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="0a6dc-105">List (Default)</span></span>
```
Get-AzsIPPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0a6dc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="0a6dc-106">Get</span></span>
```
Get-AzsIPPool -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="0a6dc-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="0a6dc-107">GetViaIdentity</span></span>
```
Get-AzsIPPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="0a6dc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a6dc-108">DESCRIPTION</span></span>
<span data-ttu-id="0a6dc-109">Geben Sie den angeforderten IP-Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-109">Return the requested IP pool.</span></span>

## <span data-ttu-id="0a6dc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a6dc-110">EXAMPLES</span></span>

### <span data-ttu-id="0a6dc-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="0a6dc-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsIpPool

Return an all infrastructure ip pools.
```

<span data-ttu-id="0a6dc-112">Abrufen aller IP-Pools für Infrastrukturen</span><span class="sxs-lookup"><span data-stu-id="0a6dc-112">Get an all infrastructure ip pools.</span></span>

### <span data-ttu-id="0a6dc-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="0a6dc-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsIpPool -Name "08786a0f-ad8c-43aa-a154-06083abfc1ac"

Get an infrastructure ip pool based on name.
```

<span data-ttu-id="0a6dc-114">Abrufen eines Infrastruktur-IP-Pools basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-114">Get an infrastructure ip pool based on name.</span></span>

## <span data-ttu-id="0a6dc-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a6dc-115">PARAMETERS</span></span>

### <span data-ttu-id="0a6dc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a6dc-116">-DefaultProfile</span></span>


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

### <span data-ttu-id="0a6dc-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="0a6dc-117">-Filter</span></span>
<span data-ttu-id="0a6dc-118">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="0a6dc-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="0a6dc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0a6dc-119">-InputObject</span></span>
<span data-ttu-id="0a6dc-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="0a6dc-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="0a6dc-121">-Location</span></span>
<span data-ttu-id="0a6dc-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-122">Location of the resource.</span></span>

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

### <span data-ttu-id="0a6dc-123">-Name</span><span class="sxs-lookup"><span data-stu-id="0a6dc-123">-Name</span></span>
<span data-ttu-id="0a6dc-124">Name des IP-Pools.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-124">IP pool name.</span></span>

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

### <span data-ttu-id="0a6dc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a6dc-125">-PassThru</span></span>
<span data-ttu-id="0a6dc-126">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="0a6dc-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a6dc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a6dc-127">-ResourceGroupName</span></span>
<span data-ttu-id="0a6dc-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-128">Name of the resource group.</span></span>

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

### <span data-ttu-id="0a6dc-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="0a6dc-129">-SubscriptionId</span></span>
<span data-ttu-id="0a6dc-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-130">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="0a6dc-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="0a6dc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a6dc-132">CommonParameters</span></span>
<span data-ttu-id="0a6dc-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a6dc-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0a6dc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a6dc-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a6dc-135">INPUTS</span></span>

### <span data-ttu-id="0a6dc-136">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="0a6dc-136">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="0a6dc-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a6dc-137">OUTPUTS</span></span>

### <span data-ttu-id="0a6dc-138">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IIPPool</span><span class="sxs-lookup"><span data-stu-id="0a6dc-138">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IIPPool</span></span>



## <span data-ttu-id="0a6dc-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a6dc-139">NOTES</span></span>

<span data-ttu-id="0a6dc-140">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="0a6dc-141">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="0a6dc-142">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="0a6dc-142">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="0a6dc-143">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-143">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="0a6dc-144">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-144">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="0a6dc-145">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-145">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="0a6dc-146">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-146">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="0a6dc-147">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-147">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="0a6dc-148">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-148">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="0a6dc-149">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="0a6dc-149">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="0a6dc-150">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="0a6dc-150">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="0a6dc-151">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-151">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="0a6dc-152">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-152">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="0a6dc-153">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-153">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="0a6dc-154">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-154">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="0a6dc-155">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-155">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="0a6dc-156">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-156">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="0a6dc-157">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-157">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="0a6dc-158">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-158">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="0a6dc-159">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-159">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="0a6dc-160">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-160">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="0a6dc-161">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-161">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="0a6dc-162">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-162">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="0a6dc-163">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-163">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="0a6dc-164">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-164">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="0a6dc-165">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="0a6dc-165">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="0a6dc-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a6dc-166">RELATED LINKS</span></span>

