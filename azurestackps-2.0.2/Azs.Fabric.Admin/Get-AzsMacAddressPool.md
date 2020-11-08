---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsmacaddresspool
schema: 2.0.0
ms.openlocfilehash: f7a2ae035ff0985c84dc78a18131c46239bafd1f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006867"
---
# <span data-ttu-id="5ec99-101">Get-AzsMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ec99-101">Get-AzsMacAddressPool</span></span>

## <span data-ttu-id="5ec99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ec99-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec99-103">Gibt den angeforderten Mac-Adresspool zurück.</span><span class="sxs-lookup"><span data-stu-id="5ec99-103">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="5ec99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ec99-104">SYNTAX</span></span>

### <span data-ttu-id="5ec99-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ec99-105">List (Default)</span></span>
```
Get-AzsMacAddressPool [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5ec99-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="5ec99-106">Get</span></span>
```
Get-AzsMacAddressPool -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="5ec99-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5ec99-107">GetViaIdentity</span></span>
```
Get-AzsMacAddressPool -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="5ec99-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ec99-108">DESCRIPTION</span></span>
<span data-ttu-id="5ec99-109">Gibt den angeforderten Mac-Adresspool zurück.</span><span class="sxs-lookup"><span data-stu-id="5ec99-109">Returns the requested MAC address pool.</span></span>

## <span data-ttu-id="5ec99-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ec99-110">EXAMPLES</span></span>

### <span data-ttu-id="5ec99-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="5ec99-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool

A list of all MAC address pools at a location.
```

<span data-ttu-id="5ec99-112">Gibt eine Liste aller Mac-Adresspools an einem Speicherort zurück.</span><span class="sxs-lookup"><span data-stu-id="5ec99-112">Returns a list of all MAC address pools at a location.</span></span>

### <span data-ttu-id="5ec99-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="5ec99-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsMacAddressPool -Name "8197fd09-8a69-417e-a55c-10c2c61f5ee7"

A specific MAC address pool at a location based on name.
```

<span data-ttu-id="5ec99-114">Abrufen eines bestimmten Mac-Adresspools an einem Speicherort, der auf dem Namen basiert.</span><span class="sxs-lookup"><span data-stu-id="5ec99-114">Get a specific MAC address pool at a location based on name.</span></span>

## <span data-ttu-id="5ec99-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ec99-115">PARAMETERS</span></span>

### <span data-ttu-id="5ec99-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec99-116">-DefaultProfile</span></span>
<span data-ttu-id="5ec99-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ec99-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec99-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="5ec99-118">-Filter</span></span>
<span data-ttu-id="5ec99-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="5ec99-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="5ec99-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ec99-120">-InputObject</span></span>
<span data-ttu-id="5ec99-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5ec99-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5ec99-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="5ec99-122">-Location</span></span>
<span data-ttu-id="5ec99-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5ec99-123">Location of the resource.</span></span>

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

### <span data-ttu-id="5ec99-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5ec99-124">-Name</span></span>
<span data-ttu-id="5ec99-125">Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="5ec99-125">Name of the MAC address pool.</span></span>

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

### <span data-ttu-id="5ec99-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5ec99-126">-PassThru</span></span>
<span data-ttu-id="5ec99-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="5ec99-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5ec99-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec99-128">-ResourceGroupName</span></span>
<span data-ttu-id="5ec99-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ec99-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="5ec99-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5ec99-130">-SubscriptionId</span></span>
<span data-ttu-id="5ec99-131">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5ec99-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5ec99-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5ec99-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5ec99-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec99-133">CommonParameters</span></span>
<span data-ttu-id="5ec99-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec99-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec99-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ec99-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec99-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ec99-136">INPUTS</span></span>

### <span data-ttu-id="5ec99-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5ec99-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5ec99-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ec99-138">OUTPUTS</span></span>

### <span data-ttu-id="5ec99-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IMacAddressPool</span><span class="sxs-lookup"><span data-stu-id="5ec99-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IMacAddressPool</span></span>



## <span data-ttu-id="5ec99-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ec99-140">NOTES</span></span>

<span data-ttu-id="5ec99-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5ec99-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5ec99-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5ec99-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5ec99-143">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5ec99-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5ec99-144">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="5ec99-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5ec99-145">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="5ec99-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5ec99-146">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="5ec99-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5ec99-147">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="5ec99-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5ec99-148">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="5ec99-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5ec99-149">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="5ec99-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5ec99-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5ec99-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5ec99-151">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="5ec99-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5ec99-152">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="5ec99-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5ec99-153">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5ec99-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5ec99-154">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5ec99-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5ec99-155">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="5ec99-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5ec99-156">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="5ec99-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5ec99-157">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="5ec99-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5ec99-158">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ec99-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5ec99-159">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="5ec99-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5ec99-160">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5ec99-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5ec99-161">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5ec99-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5ec99-162">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="5ec99-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="5ec99-163">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="5ec99-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5ec99-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5ec99-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5ec99-165">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5ec99-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5ec99-166">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="5ec99-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="5ec99-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ec99-167">RELATED LINKS</span></span>

