---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegateway
schema: 2.0.0
ms.openlocfilehash: a9c883fab422252aad167d92da3adf55edd9a78b
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006831"
---
# <span data-ttu-id="f6450-101">Get-AzsEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="f6450-101">Get-AzsEdgeGateway</span></span>

## <span data-ttu-id="f6450-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6450-102">SYNOPSIS</span></span>
<span data-ttu-id="f6450-103">Gibt das angeforderte Edge-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="f6450-103">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="f6450-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6450-104">SYNTAX</span></span>

### <span data-ttu-id="f6450-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6450-105">List (Default)</span></span>
```
Get-AzsEdgeGateway [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f6450-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="f6450-106">Get</span></span>
```
Get-AzsEdgeGateway -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="f6450-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f6450-107">GetViaIdentity</span></span>
```
Get-AzsEdgeGateway -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="f6450-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6450-108">DESCRIPTION</span></span>
<span data-ttu-id="f6450-109">Gibt das angeforderte Edge-Gateway zurück.</span><span class="sxs-lookup"><span data-stu-id="f6450-109">Returns the requested edge gateway.</span></span>

## <span data-ttu-id="f6450-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6450-110">EXAMPLES</span></span>

### <span data-ttu-id="f6450-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="f6450-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsEdgeGateway

Get a list of all edge gateways.
```

<span data-ttu-id="f6450-112">Gibt die Liste aller Edge-Gateways an einer bestimmten Position zurück.</span><span class="sxs-lookup"><span data-stu-id="f6450-112">Returns the list of all edge gateways at a certain location.</span></span>


## <span data-ttu-id="f6450-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6450-113">PARAMETERS</span></span>

### <span data-ttu-id="f6450-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6450-114">-DefaultProfile</span></span>
<span data-ttu-id="f6450-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6450-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6450-116">-Filter</span><span class="sxs-lookup"><span data-stu-id="f6450-116">-Filter</span></span>
<span data-ttu-id="f6450-117">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="f6450-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="f6450-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f6450-118">-InputObject</span></span>
<span data-ttu-id="f6450-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="f6450-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f6450-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="f6450-120">-Location</span></span>
<span data-ttu-id="f6450-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f6450-121">Location of the resource.</span></span>

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

### <span data-ttu-id="f6450-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f6450-122">-Name</span></span>
<span data-ttu-id="f6450-123">Der Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="f6450-123">Name of the edge gateway.</span></span>

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

### <span data-ttu-id="f6450-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f6450-124">-PassThru</span></span>
<span data-ttu-id="f6450-125">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="f6450-125">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f6450-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6450-126">-ResourceGroupName</span></span>
<span data-ttu-id="f6450-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6450-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="f6450-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="f6450-128">-SubscriptionId</span></span>
<span data-ttu-id="f6450-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f6450-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="f6450-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f6450-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f6450-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6450-131">CommonParameters</span></span>
<span data-ttu-id="f6450-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6450-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6450-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6450-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6450-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6450-134">INPUTS</span></span>

### <span data-ttu-id="f6450-135">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f6450-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="f6450-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6450-136">OUTPUTS</span></span>

### <span data-ttu-id="f6450-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IEdgeGateway</span><span class="sxs-lookup"><span data-stu-id="f6450-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGateway</span></span>



## <span data-ttu-id="f6450-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6450-138">NOTES</span></span>

<span data-ttu-id="f6450-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="f6450-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f6450-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="f6450-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f6450-141">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="f6450-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f6450-142">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="f6450-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="f6450-143">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="f6450-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="f6450-144">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="f6450-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="f6450-145">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="f6450-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="f6450-146">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="f6450-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="f6450-147">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="f6450-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="f6450-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="f6450-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f6450-149">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="f6450-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="f6450-150">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="f6450-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="f6450-151">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="f6450-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="f6450-152">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="f6450-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="f6450-153">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="f6450-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="f6450-154">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="f6450-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="f6450-155">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="f6450-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="f6450-156">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6450-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="f6450-157">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="f6450-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="f6450-158">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="f6450-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="f6450-159">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="f6450-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="f6450-160">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="f6450-160">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="f6450-161">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="f6450-161">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="f6450-162">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f6450-162">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="f6450-163">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="f6450-163">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f6450-164">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="f6450-164">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="f6450-165">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6450-165">RELATED LINKS</span></span>

