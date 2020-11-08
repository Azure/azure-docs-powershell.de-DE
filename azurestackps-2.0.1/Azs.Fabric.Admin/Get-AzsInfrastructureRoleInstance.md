---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: b5eb59c1f2ad631e8cbb9fdffbf65bee00425d43
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005433"
---
# <span data-ttu-id="9b1df-101">Get-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="9b1df-101">Get-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="9b1df-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9b1df-102">SYNOPSIS</span></span>
<span data-ttu-id="9b1df-103">Gibt die angeforderte Infrastrukturrollen Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="9b1df-103">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="9b1df-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9b1df-104">SYNTAX</span></span>

### <span data-ttu-id="9b1df-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="9b1df-105">List (Default)</span></span>
```
Get-AzsInfrastructureRoleInstance [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9b1df-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="9b1df-106">Get</span></span>
```
Get-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="9b1df-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b1df-107">GetViaIdentity</span></span>
```
Get-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="9b1df-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9b1df-108">DESCRIPTION</span></span>
<span data-ttu-id="9b1df-109">Gibt die angeforderte Infrastrukturrollen Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="9b1df-109">Return the requested infrastructure role instance.</span></span>

## <span data-ttu-id="9b1df-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9b1df-110">EXAMPLES</span></span>

### <span data-ttu-id="9b1df-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="9b1df-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance

A list of all infrastructure role instances.
```

<span data-ttu-id="9b1df-112">Gibt eine Liste aller Rolleninstanzen der Infrastruktur zurück.</span><span class="sxs-lookup"><span data-stu-id="9b1df-112">Return a list of all infrastructure role instances.</span></span>

### <span data-ttu-id="9b1df-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="9b1df-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

A single infrastructure role instance based on name.
```

<span data-ttu-id="9b1df-114">Gibt eine einzelne Infrastrukturrollen Instanz basierend auf dem Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="9b1df-114">Return a single infrastructure role instance based on name.</span></span>

## <span data-ttu-id="9b1df-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="9b1df-115">PARAMETERS</span></span>

### <span data-ttu-id="9b1df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b1df-116">-DefaultProfile</span></span>
<span data-ttu-id="9b1df-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9b1df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b1df-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="9b1df-118">-Filter</span></span>
<span data-ttu-id="9b1df-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="9b1df-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="9b1df-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b1df-120">-InputObject</span></span>
<span data-ttu-id="9b1df-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9b1df-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b1df-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="9b1df-122">-Location</span></span>
<span data-ttu-id="9b1df-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9b1df-123">Location of the resource.</span></span>

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

### <span data-ttu-id="9b1df-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9b1df-124">-Name</span></span>
<span data-ttu-id="9b1df-125">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b1df-125">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="9b1df-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b1df-126">-PassThru</span></span>
<span data-ttu-id="9b1df-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="9b1df-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9b1df-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b1df-128">-ResourceGroupName</span></span>
<span data-ttu-id="9b1df-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b1df-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="9b1df-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9b1df-130">-SubscriptionId</span></span>
<span data-ttu-id="9b1df-131">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9b1df-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9b1df-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9b1df-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b1df-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b1df-133">CommonParameters</span></span>
<span data-ttu-id="9b1df-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b1df-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b1df-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b1df-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b1df-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9b1df-136">INPUTS</span></span>

### <span data-ttu-id="9b1df-137">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9b1df-137">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9b1df-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9b1df-138">OUTPUTS</span></span>

### <span data-ttu-id="9b1df-139">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IInfraRoleInstance</span><span class="sxs-lookup"><span data-stu-id="9b1df-139">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IInfraRoleInstance</span></span>



## <span data-ttu-id="9b1df-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="9b1df-140">NOTES</span></span>

<span data-ttu-id="9b1df-141">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9b1df-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b1df-142">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9b1df-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9b1df-143">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9b1df-143">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b1df-144">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="9b1df-144">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9b1df-145">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="9b1df-145">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9b1df-146">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="9b1df-146">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9b1df-147">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="9b1df-147">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9b1df-148">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="9b1df-148">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9b1df-149">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="9b1df-149">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9b1df-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9b1df-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b1df-151">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="9b1df-151">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9b1df-152">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b1df-152">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9b1df-153">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9b1df-153">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9b1df-154">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="9b1df-154">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9b1df-155">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="9b1df-155">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9b1df-156">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="9b1df-156">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9b1df-157">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="9b1df-157">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9b1df-158">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9b1df-158">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9b1df-159">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="9b1df-159">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9b1df-160">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="9b1df-160">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9b1df-161">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9b1df-161">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9b1df-162">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="9b1df-162">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9b1df-163">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="9b1df-163">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9b1df-164">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9b1df-164">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9b1df-165">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9b1df-165">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9b1df-166">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="9b1df-166">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9b1df-167">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9b1df-167">RELATED LINKS</span></span>

