---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureshare
schema: 2.0.0
ms.openlocfilehash: e5fce1490b27bb569ce493a66a1c2646b73466a4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844796"
---
# <span data-ttu-id="7d76e-101">Get-AzsInfrastructureShare</span><span class="sxs-lookup"><span data-stu-id="7d76e-101">Get-AzsInfrastructureShare</span></span>

## <span data-ttu-id="7d76e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7d76e-102">SYNOPSIS</span></span>
<span data-ttu-id="7d76e-103">Gibt die angeforderte Fabric-Dateifreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="7d76e-103">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="7d76e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7d76e-104">SYNTAX</span></span>

### <span data-ttu-id="7d76e-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7d76e-105">List (Default)</span></span>
```
Get-AzsInfrastructureShare [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="7d76e-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7d76e-106">Get</span></span>
```
Get-AzsInfrastructureShare -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="7d76e-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="7d76e-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureShare -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="7d76e-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7d76e-108">DESCRIPTION</span></span>
<span data-ttu-id="7d76e-109">Gibt die angeforderte Fabric-Dateifreigabe zurück.</span><span class="sxs-lookup"><span data-stu-id="7d76e-109">Returns the requested fabric file share.</span></span>

## <span data-ttu-id="7d76e-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7d76e-110">EXAMPLES</span></span>

### <span data-ttu-id="7d76e-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="7d76e-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare
```

<span data-ttu-id="7d76e-112">Gibt eine Liste aller Dateifreigaben zurück.</span><span class="sxs-lookup"><span data-stu-id="7d76e-112">Returns a list of all file shares.</span></span>

### <span data-ttu-id="7d76e-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="7d76e-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureShare -Name SU1_ObjStore_1
```

<span data-ttu-id="7d76e-114">Gibt eine Dateifreigabe basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="7d76e-114">Returns a file share based on name.</span></span>

## <span data-ttu-id="7d76e-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7d76e-115">PARAMETERS</span></span>

### <span data-ttu-id="7d76e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d76e-116">-DefaultProfile</span></span>
<span data-ttu-id="7d76e-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7d76e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d76e-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="7d76e-118">-Filter</span></span>
<span data-ttu-id="7d76e-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="7d76e-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="7d76e-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7d76e-120">-InputObject</span></span>
<span data-ttu-id="7d76e-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="7d76e-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="7d76e-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="7d76e-122">-Location</span></span>
<span data-ttu-id="7d76e-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7d76e-123">Location of the resource.</span></span>

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

### <span data-ttu-id="7d76e-124">-Name</span><span class="sxs-lookup"><span data-stu-id="7d76e-124">-Name</span></span>
<span data-ttu-id="7d76e-125">Name der Fabric-Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="7d76e-125">Fabric file share name.</span></span>

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

### <span data-ttu-id="7d76e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d76e-126">-PassThru</span></span>
<span data-ttu-id="7d76e-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="7d76e-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="7d76e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d76e-128">-ResourceGroupName</span></span>
<span data-ttu-id="7d76e-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d76e-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="7d76e-130">-Skip</span><span class="sxs-lookup"><span data-stu-id="7d76e-130">-Skip</span></span>
<span data-ttu-id="7d76e-131">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="7d76e-131">OData skip parameter.</span></span>

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

### <span data-ttu-id="7d76e-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7d76e-132">-SubscriptionId</span></span>
<span data-ttu-id="7d76e-133">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7d76e-133">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="7d76e-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7d76e-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="7d76e-135">-Top</span><span class="sxs-lookup"><span data-stu-id="7d76e-135">-Top</span></span>
<span data-ttu-id="7d76e-136">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="7d76e-136">OData top parameter.</span></span>

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

### <span data-ttu-id="7d76e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d76e-137">CommonParameters</span></span>
<span data-ttu-id="7d76e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d76e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d76e-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d76e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d76e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7d76e-140">INPUTS</span></span>

### <span data-ttu-id="7d76e-141">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="7d76e-141">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="7d76e-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7d76e-142">OUTPUTS</span></span>

### <span data-ttu-id="7d76e-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IFileShare</span><span class="sxs-lookup"><span data-stu-id="7d76e-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IFileShare</span></span>



## <span data-ttu-id="7d76e-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="7d76e-144">NOTES</span></span>

<span data-ttu-id="7d76e-145">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="7d76e-145">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7d76e-146">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="7d76e-146">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="7d76e-147">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="7d76e-147">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7d76e-148">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="7d76e-148">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="7d76e-149">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="7d76e-149">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="7d76e-150">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="7d76e-150">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="7d76e-151">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="7d76e-151">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="7d76e-152">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="7d76e-152">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="7d76e-153">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="7d76e-153">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="7d76e-154">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="7d76e-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7d76e-155">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="7d76e-155">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="7d76e-156">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d76e-156">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="7d76e-157">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="7d76e-157">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="7d76e-158">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="7d76e-158">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="7d76e-159">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="7d76e-159">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="7d76e-160">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="7d76e-160">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="7d76e-161">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="7d76e-161">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="7d76e-162">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7d76e-162">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="7d76e-163">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="7d76e-163">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="7d76e-164">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="7d76e-164">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="7d76e-165">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="7d76e-165">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="7d76e-166">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="7d76e-166">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="7d76e-167">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7d76e-167">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="7d76e-168">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="7d76e-168">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="7d76e-169">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="7d76e-169">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="7d76e-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7d76e-170">RELATED LINKS</span></span>

