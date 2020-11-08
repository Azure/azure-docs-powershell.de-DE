---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/get-azsstoragesubsystem
schema: 2.0.0
ms.openlocfilehash: 75349838437ad34743b67510f3a284ff2736b30c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006874"
---
# <span data-ttu-id="aa2da-101">Get-AzsStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="aa2da-101">Get-AzsStorageSubSystem</span></span>

## <span data-ttu-id="aa2da-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa2da-102">SYNOPSIS</span></span>
<span data-ttu-id="aa2da-103">Geben Sie das angeforderte Speichersubsystem zurück.</span><span class="sxs-lookup"><span data-stu-id="aa2da-103">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="aa2da-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa2da-104">SYNTAX</span></span>

### <span data-ttu-id="aa2da-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="aa2da-105">List (Default)</span></span>
```
Get-AzsStorageSubSystem -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-Skip <String>] [-Top <String>] [-DefaultProfile <PSObject>]
 [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="aa2da-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="aa2da-106">Get</span></span>
```
Get-AzsStorageSubSystem -Name <String> -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru] [<CommonParameters>]
```

### <span data-ttu-id="aa2da-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aa2da-107">GetViaIdentity</span></span>
```
Get-AzsStorageSubSystem -InputObject <IFabricAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="aa2da-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa2da-108">DESCRIPTION</span></span>
<span data-ttu-id="aa2da-109">Geben Sie das angeforderte Speichersubsystem zurück.</span><span class="sxs-lookup"><span data-stu-id="aa2da-109">Return the requested storage subsystem.</span></span>

## <span data-ttu-id="aa2da-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa2da-110">EXAMPLES</span></span>

### <span data-ttu-id="aa2da-111">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="aa2da-111">Example 1:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name
```

<span data-ttu-id="aa2da-112">Abrufen aller Speichersubsysteme aus einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="aa2da-112">Get all storage subsystems from a scale unit.</span></span>

### <span data-ttu-id="aa2da-113">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="aa2da-113">Example 2:</span></span>
```powershell
PS C:\> $scaleUnit = Get-AzsScaleUnit | select -First 1
PS C:\> Get-AzsStorageSubSystem -ScaleUnit $scaleUnit.Name -Name s-cluster.DomainFQDN
```

<span data-ttu-id="aa2da-114">Besorgen Sie sich ein Speichersubsystem, das eine Skalierungseinheit und einen Namen erhält.</span><span class="sxs-lookup"><span data-stu-id="aa2da-114">Get a storage subsystem given a scale unit and name.</span></span>

## <span data-ttu-id="aa2da-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2da-115">PARAMETERS</span></span>

### <span data-ttu-id="aa2da-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa2da-116">-DefaultProfile</span></span>
<span data-ttu-id="aa2da-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa2da-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa2da-118">-Filter</span><span class="sxs-lookup"><span data-stu-id="aa2da-118">-Filter</span></span>
<span data-ttu-id="aa2da-119">OData-Filterparameter</span><span class="sxs-lookup"><span data-stu-id="aa2da-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="aa2da-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="aa2da-120">-InputObject</span></span>
<span data-ttu-id="aa2da-121">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aa2da-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa2da-122">-Standort</span><span class="sxs-lookup"><span data-stu-id="aa2da-122">-Location</span></span>
<span data-ttu-id="aa2da-123">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="aa2da-123">Location of the resource.</span></span>

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

### <span data-ttu-id="aa2da-124">-Name</span><span class="sxs-lookup"><span data-stu-id="aa2da-124">-Name</span></span>
<span data-ttu-id="aa2da-125">Name des Speichersystems</span><span class="sxs-lookup"><span data-stu-id="aa2da-125">Name of the storage system.</span></span>

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

### <span data-ttu-id="aa2da-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa2da-126">-PassThru</span></span>
<span data-ttu-id="aa2da-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="aa2da-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aa2da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa2da-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa2da-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa2da-129">Name of the resource group.</span></span>

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

### <span data-ttu-id="aa2da-130">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="aa2da-130">-ScaleUnit</span></span>
<span data-ttu-id="aa2da-131">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="aa2da-131">Name of the scale units.</span></span>

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

### <span data-ttu-id="aa2da-132">-Skip</span><span class="sxs-lookup"><span data-stu-id="aa2da-132">-Skip</span></span>
<span data-ttu-id="aa2da-133">OData-Skip-Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2da-133">OData skip parameter.</span></span>

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

### <span data-ttu-id="aa2da-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="aa2da-134">-SubscriptionId</span></span>
<span data-ttu-id="aa2da-135">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aa2da-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa2da-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="aa2da-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa2da-137">-Top</span><span class="sxs-lookup"><span data-stu-id="aa2da-137">-Top</span></span>
<span data-ttu-id="aa2da-138">OData-oberer Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa2da-138">OData top parameter.</span></span>

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

### <span data-ttu-id="aa2da-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa2da-139">CommonParameters</span></span>
<span data-ttu-id="aa2da-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa2da-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa2da-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa2da-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa2da-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa2da-142">INPUTS</span></span>

### <span data-ttu-id="aa2da-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="aa2da-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="aa2da-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa2da-144">OUTPUTS</span></span>

### <span data-ttu-id="aa2da-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20181001. IStorageSubSystem</span><span class="sxs-lookup"><span data-stu-id="aa2da-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20181001.IStorageSubSystem</span></span>



## <span data-ttu-id="aa2da-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa2da-146">NOTES</span></span>

<span data-ttu-id="aa2da-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa2da-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa2da-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="aa2da-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aa2da-149">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="aa2da-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aa2da-150">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="aa2da-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="aa2da-151">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="aa2da-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="aa2da-152">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="aa2da-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="aa2da-153">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="aa2da-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="aa2da-154">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="aa2da-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="aa2da-155">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="aa2da-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="aa2da-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="aa2da-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aa2da-157">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="aa2da-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="aa2da-158">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="aa2da-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="aa2da-159">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="aa2da-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="aa2da-160">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="aa2da-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="aa2da-161">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="aa2da-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="aa2da-162">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="aa2da-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="aa2da-163">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="aa2da-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="aa2da-164">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="aa2da-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="aa2da-165">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="aa2da-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="aa2da-166">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="aa2da-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="aa2da-167">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="aa2da-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="aa2da-168">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="aa2da-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="aa2da-169">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aa2da-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="aa2da-170">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="aa2da-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aa2da-171">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="aa2da-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="aa2da-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa2da-172">RELATED LINKS</span></span>

