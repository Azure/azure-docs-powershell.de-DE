---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructurelocation
schema: 2.0.0
ms.openlocfilehash: 0d0f2856503943d19653dd09a8cb1c125fec9517
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842607"
---
# <span data-ttu-id="5163f-101">Get-AzsInfrastructureLocation</span><span class="sxs-lookup"><span data-stu-id="5163f-101">Get-AzsInfrastructureLocation</span></span>

## <span data-ttu-id="5163f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5163f-102">SYNOPSIS</span></span>
<span data-ttu-id="5163f-103">Gibt den angeforderten Fabric-Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5163f-103">Returns the requested fabric location.</span></span>

## <span data-ttu-id="5163f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5163f-104">SYNTAX</span></span>

### <span data-ttu-id="5163f-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5163f-105">List (Default)</span></span>
```
Get-AzsInfrastructureLocation [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="5163f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5163f-106">Get</span></span>
```
Get-AzsInfrastructureLocation -FabricLocation <String> [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5163f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5163f-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureLocation -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5163f-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5163f-108">DESCRIPTION</span></span>
<span data-ttu-id="5163f-109">Gibt den angeforderten Fabric-Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5163f-109">Returns the requested fabric location.</span></span>

## <span data-ttu-id="5163f-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5163f-110">EXAMPLES</span></span>

### <span data-ttu-id="5163f-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="5163f-111">Example 1:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation

Return a list of all fabric locations.
```

<span data-ttu-id="5163f-112">Abrufen einer Liste aller Fabric-Standorte</span><span class="sxs-lookup"><span data-stu-id="5163f-112">Get a list of all fabric locations.</span></span>

### <span data-ttu-id="5163f-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="5163f-113">Example 2:</span></span> 
```powershell
PS C:\> Get-AzsInfrastructureLocation -Location "local"

Return a location based on the name.
```

<span data-ttu-id="5163f-114">Besorgen Sie sich einen Speicherort basierend auf dem Namen.</span><span class="sxs-lookup"><span data-stu-id="5163f-114">Get a location based on the name.</span></span>

## <span data-ttu-id="5163f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5163f-115">PARAMETERS</span></span>

### <span data-ttu-id="5163f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5163f-116">-DefaultProfile</span></span>
<span data-ttu-id="5163f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5163f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5163f-118">-FabricLocation</span><span class="sxs-lookup"><span data-stu-id="5163f-118">-FabricLocation</span></span>
<span data-ttu-id="5163f-119">Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="5163f-119">Fabric location.</span></span>

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

### <span data-ttu-id="5163f-120">-Filter</span><span class="sxs-lookup"><span data-stu-id="5163f-120">-Filter</span></span>
<span data-ttu-id="5163f-121">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="5163f-121">OData filter parameter.</span></span>

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

### <span data-ttu-id="5163f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5163f-122">-InputObject</span></span>
<span data-ttu-id="5163f-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5163f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5163f-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5163f-124">-PassThru</span></span>
<span data-ttu-id="5163f-125">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="5163f-125">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="5163f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5163f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5163f-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5163f-127">Name of the resource group.</span></span>

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

### <span data-ttu-id="5163f-128">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5163f-128">-SubscriptionId</span></span>
<span data-ttu-id="5163f-129">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5163f-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5163f-130">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5163f-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5163f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5163f-131">CommonParameters</span></span>
<span data-ttu-id="5163f-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5163f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5163f-133">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5163f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5163f-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5163f-134">INPUTS</span></span>

### <span data-ttu-id="5163f-135">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5163f-135">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5163f-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5163f-136">OUTPUTS</span></span>

### <span data-ttu-id="5163f-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFabricLocation</span><span class="sxs-lookup"><span data-stu-id="5163f-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFabricLocation</span></span>



## <span data-ttu-id="5163f-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5163f-138">NOTES</span></span>

<span data-ttu-id="5163f-139">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5163f-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5163f-140">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5163f-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5163f-141">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5163f-141">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5163f-142">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="5163f-142">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5163f-143">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="5163f-143">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5163f-144">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="5163f-144">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5163f-145">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="5163f-145">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5163f-146">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="5163f-146">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5163f-147">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="5163f-147">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5163f-148">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5163f-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5163f-149">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="5163f-149">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5163f-150">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="5163f-150">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5163f-151">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5163f-151">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5163f-152">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5163f-152">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5163f-153">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="5163f-153">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5163f-154">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="5163f-154">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5163f-155">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="5163f-155">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5163f-156">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5163f-156">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5163f-157">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="5163f-157">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5163f-158">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5163f-158">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5163f-159">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5163f-159">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5163f-160">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="5163f-160">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5163f-161">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5163f-161">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5163f-162">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5163f-162">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5163f-163">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="5163f-163">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5163f-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5163f-164">RELATED LINKS</span></span>

