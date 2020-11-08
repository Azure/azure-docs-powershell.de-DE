---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azslogicalnetwork
schema: 2.0.0
ms.openlocfilehash: 8229e487cd7c616969e049bbbea0ba7a6a18a448
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005525"
---
# <span data-ttu-id="85c39-101">Get-AzsLogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="85c39-101">Get-AzsLogicalNetwork</span></span>

## <span data-ttu-id="85c39-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85c39-102">SYNOPSIS</span></span>
<span data-ttu-id="85c39-103">Gibt das angeforderte logische Netzwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="85c39-103">Returns the requested logical network.</span></span>

## <span data-ttu-id="85c39-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="85c39-104">SYNTAX</span></span>

### <span data-ttu-id="85c39-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="85c39-105">List (Default)</span></span>
```
Get-AzsLogicalNetwork [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="85c39-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="85c39-106">Get</span></span>
```
Get-AzsLogicalNetwork -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="85c39-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85c39-107">GetViaIdentity</span></span>
```
Get-AzsLogicalNetwork -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="85c39-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85c39-108">DESCRIPTION</span></span>
<span data-ttu-id="85c39-109">Gibt das angeforderte logische Netzwerk zurück.</span><span class="sxs-lookup"><span data-stu-id="85c39-109">Returns the requested logical network.</span></span>

## <span data-ttu-id="85c39-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85c39-110">EXAMPLES</span></span>

### <span data-ttu-id="85c39-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="85c39-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork

A list of all logical networks at a location.
```

<span data-ttu-id="85c39-112">Abrufen aller logischen Netzwerke an einem Speicherort</span><span class="sxs-lookup"><span data-stu-id="85c39-112">Get all logical networks at a location.</span></span>

### <span data-ttu-id="85c39-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="85c39-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsLogicalNetwork -Name "bb6c6f28-bad9-441b-8e62-57d2be255904"

A specific logical networks at a location based on a name.
```

<span data-ttu-id="85c39-114">Abrufen bestimmter logischer Netzwerke an einem Speicherort, der auf einem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="85c39-114">Get a specific logical networks at a location based on a name.</span></span>

## <span data-ttu-id="85c39-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="85c39-115">PARAMETERS</span></span>

### <span data-ttu-id="85c39-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85c39-116">-DefaultProfile</span></span>
<span data-ttu-id="85c39-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85c39-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85c39-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="85c39-118">-Filter</span></span>
<span data-ttu-id="85c39-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="85c39-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="85c39-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85c39-120">-InputObject</span></span>
<span data-ttu-id="85c39-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="85c39-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="85c39-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="85c39-122">-Location</span></span>
<span data-ttu-id="85c39-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="85c39-123">Location of the resource.</span></span>

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

### <span data-ttu-id="85c39-124">-Name</span><span class="sxs-lookup"><span data-stu-id="85c39-124">-Name</span></span>
<span data-ttu-id="85c39-125">Der Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="85c39-125">Name of the logical network.</span></span>

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

### <span data-ttu-id="85c39-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85c39-126">-PassThru</span></span>
<span data-ttu-id="85c39-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="85c39-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85c39-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85c39-128">-ResourceGroupName</span></span>
<span data-ttu-id="85c39-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85c39-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="85c39-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="85c39-130">-SubscriptionId</span></span>
<span data-ttu-id="85c39-131">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="85c39-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85c39-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="85c39-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="85c39-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85c39-133">CommonParameters</span></span>
<span data-ttu-id="85c39-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85c39-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85c39-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85c39-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85c39-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85c39-136">INPUTS</span></span>

### <span data-ttu-id="85c39-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="85c39-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="85c39-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85c39-138">OUTPUTS</span></span>

### <span data-ttu-id="85c39-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. ILogicalNetwork</span><span class="sxs-lookup"><span data-stu-id="85c39-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.ILogicalNetwork</span></span>



## <span data-ttu-id="85c39-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="85c39-140">NOTES</span></span>

<span data-ttu-id="85c39-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85c39-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85c39-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="85c39-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="85c39-143">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="85c39-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85c39-144">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="85c39-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="85c39-145">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="85c39-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="85c39-146">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="85c39-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="85c39-147">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="85c39-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="85c39-148">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="85c39-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="85c39-149">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="85c39-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="85c39-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="85c39-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85c39-151">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="85c39-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="85c39-152">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="85c39-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="85c39-153">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="85c39-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="85c39-154">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="85c39-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="85c39-155">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="85c39-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="85c39-156">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="85c39-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="85c39-157">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="85c39-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="85c39-158">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85c39-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="85c39-159">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="85c39-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="85c39-160">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="85c39-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="85c39-161">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="85c39-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="85c39-162">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="85c39-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="85c39-163">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="85c39-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="85c39-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="85c39-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="85c39-165">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="85c39-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="85c39-166">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="85c39-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="85c39-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85c39-167">RELATED LINKS</span></span>

