---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsedgegatewaypool
schema: 2.0.0
ms.openlocfilehash: 79b4ae3a4bd3807b08ea45be9a9a328455f03b67
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006832"
---
# <span data-ttu-id="48611-101">Get-AzsEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="48611-101">Get-AzsEdgeGatewayPool</span></span>

## <span data-ttu-id="48611-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="48611-102">SYNOPSIS</span></span>


## <span data-ttu-id="48611-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="48611-103">SYNTAX</span></span>

### <span data-ttu-id="48611-104">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="48611-104">List (Default)</span></span>
```
Get-AzsEdgeGatewayPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="48611-105">Erhalten</span><span class="sxs-lookup"><span data-stu-id="48611-105">Get</span></span>
```
Get-AzsEdgeGatewayPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="48611-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="48611-106">GetViaIdentity</span></span>
```
Get-AzsEdgeGatewayPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="48611-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="48611-107">DESCRIPTION</span></span>


## <span data-ttu-id="48611-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="48611-108">EXAMPLES</span></span>

### <span data-ttu-id="48611-109">Beispiel 1: Abrufen einer Liste aller Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="48611-109">Example 1: Get a list of all Edge Gateway pools.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a list of all Edge Gateway pools.
```

<span data-ttu-id="48611-110">Abrufen einer Liste aller Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="48611-110">Get a list of all Edge Gateway pools.</span></span>

### <span data-ttu-id="48611-111">Beispiel 2: Abrufen eines bestimmten Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="48611-111">Example 2: Get a specific edge gateway pool.</span></span>
```powershell
PS C:\> Get-AzsEdgeGatewayPool

Return a specific edge gateway pool.
```

<span data-ttu-id="48611-112">Abrufen eines bestimmten Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="48611-112">Get a specific edge gateway pool.</span></span>

## <span data-ttu-id="48611-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="48611-113">PARAMETERS</span></span>

### <span data-ttu-id="48611-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48611-114">-DefaultProfile</span></span>


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

### <span data-ttu-id="48611-115">-Filter</span><span class="sxs-lookup"><span data-stu-id="48611-115">-Filter</span></span>


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

### <span data-ttu-id="48611-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="48611-116">-InputObject</span></span>
<span data-ttu-id="48611-117">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="48611-117">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="48611-118">-Standort</span><span class="sxs-lookup"><span data-stu-id="48611-118">-Location</span></span>


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

### <span data-ttu-id="48611-119">-Name</span><span class="sxs-lookup"><span data-stu-id="48611-119">-Name</span></span>


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

### <span data-ttu-id="48611-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="48611-120">-PassThru</span></span>


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

### <span data-ttu-id="48611-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="48611-121">-ResourceGroupName</span></span>


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

### <span data-ttu-id="48611-122">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="48611-122">-SubscriptionId</span></span>


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

### <span data-ttu-id="48611-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48611-123">CommonParameters</span></span>
<span data-ttu-id="48611-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="48611-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48611-125">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="48611-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48611-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="48611-126">INPUTS</span></span>

### <span data-ttu-id="48611-127">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="48611-127">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="48611-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="48611-128">OUTPUTS</span></span>

### <span data-ttu-id="48611-129">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IEdgeGatewayPool</span><span class="sxs-lookup"><span data-stu-id="48611-129">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IEdgeGatewayPool</span></span>



## <span data-ttu-id="48611-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="48611-130">NOTES</span></span>

<span data-ttu-id="48611-131">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="48611-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="48611-132">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="48611-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="48611-133">Inputobject <IFabricAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="48611-133">INPUTOBJECT <IFabricAdminIdentity>:</span></span> 
  - <span data-ttu-id="48611-134">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="48611-134">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="48611-135">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="48611-135">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="48611-136">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="48611-136">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="48611-137">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="48611-137">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="48611-138">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="48611-138">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="48611-139">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="48611-139">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="48611-140">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="48611-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="48611-141">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="48611-141">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="48611-142">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="48611-142">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="48611-143">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="48611-143">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="48611-144">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="48611-144">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="48611-145">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="48611-145">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="48611-146">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="48611-146">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="48611-147">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="48611-147">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="48611-148">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="48611-148">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="48611-149">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="48611-149">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="48611-150">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="48611-150">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="48611-151">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="48611-151">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="48611-152">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="48611-152">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="48611-153">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="48611-153">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="48611-154">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="48611-154">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="48611-155">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="48611-155">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="48611-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="48611-156">RELATED LINKS</span></span>

