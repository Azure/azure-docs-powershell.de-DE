---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/repair-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: b9a285e650f0ed47dd0144a460b324ecdae49f7d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007353"
---
# <span data-ttu-id="9d36f-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="9d36f-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="9d36f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9d36f-102">SYNOPSIS</span></span>
<span data-ttu-id="9d36f-103">Repariert einen Knoten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="9d36f-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9d36f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9d36f-104">SYNTAX</span></span>

### <span data-ttu-id="9d36f-105">RepairExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d36f-105">RepairExpanded (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-BiosVersion <String>] [-BmciPv4Address <String>] [-ClusterName <String>]
 [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>] [-SerialNumber <String>]
 [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9d36f-106">Reparatur</span><span class="sxs-lookup"><span data-stu-id="9d36f-106">Repair</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BareMetalNode <IBareMetalNodeDescription> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9d36f-107">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9d36f-107">RepairViaIdentity</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> -BareMetalNode <IBareMetalNodeDescription>
 [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="9d36f-108">RepairViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9d36f-108">RepairViaIdentityExpanded</span></span>
```
Repair-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-BiosVersion <String>] [-BmciPv4Address <String>]
 [-ClusterName <String>] [-ComputerName <String>] [-Force] [-MacAddress <String>] [-Model <String>]
 [-SerialNumber <String>] [-Vendor <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9d36f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9d36f-109">DESCRIPTION</span></span>
<span data-ttu-id="9d36f-110">Repariert einen Knoten des Clusters.</span><span class="sxs-lookup"><span data-stu-id="9d36f-110">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="9d36f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9d36f-111">EXAMPLES</span></span>

### <span data-ttu-id="9d36f-112">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="9d36f-112">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***

```

<span data-ttu-id="9d36f-113">Reparieren eines Knotens einer Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="9d36f-113">Repair a scale unit node.</span></span>


## <span data-ttu-id="9d36f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9d36f-114">PARAMETERS</span></span>

### <span data-ttu-id="9d36f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9d36f-115">-AsJob</span></span>
<span data-ttu-id="9d36f-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9d36f-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9d36f-117">-BareMetalNode</span><span class="sxs-lookup"><span data-stu-id="9d36f-117">-BareMetalNode</span></span>
<span data-ttu-id="9d36f-118">Beschreibung eines baren Metall Knotens, der für die Skalierungsoperation in einem Cluster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d36f-118">Description of a bare metal node used for ScaleOut operation on a cluster.</span></span>
<span data-ttu-id="9d36f-119">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für BAREMETALNODE-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9d36f-119">To construct, see NOTES section for BAREMETALNODE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription
Parameter Sets: Repair, RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-120">-BiosVersion</span><span class="sxs-lookup"><span data-stu-id="9d36f-120">-BiosVersion</span></span>
<span data-ttu-id="9d36f-121">BIOS-Version des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-121">Bios version of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-122">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="9d36f-122">-BmciPv4Address</span></span>
<span data-ttu-id="9d36f-123">BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-123">BMC address of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-124">-Clustername</span><span class="sxs-lookup"><span data-stu-id="9d36f-124">-ClusterName</span></span>
<span data-ttu-id="9d36f-125">Der Name des Clusters.</span><span class="sxs-lookup"><span data-stu-id="9d36f-125">Name of the cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-126">-Computername</span><span class="sxs-lookup"><span data-stu-id="9d36f-126">-ComputerName</span></span>
<span data-ttu-id="9d36f-127">Der Name des Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-127">Name of the computer.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d36f-128">-DefaultProfile</span></span>
<span data-ttu-id="9d36f-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9d36f-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d36f-130">-Force</span><span class="sxs-lookup"><span data-stu-id="9d36f-130">-Force</span></span>
<span data-ttu-id="9d36f-131">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9d36f-131">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9d36f-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9d36f-132">-InputObject</span></span>
<span data-ttu-id="9d36f-133">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Inputobject-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9d36f-133">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RepairViaIdentity, RepairViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="9d36f-134">-Location</span></span>
<span data-ttu-id="9d36f-135">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d36f-135">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-136">-MACAddress</span><span class="sxs-lookup"><span data-stu-id="9d36f-136">-MacAddress</span></span>
<span data-ttu-id="9d36f-137">Der Name der Mac-Adresse des Bare Metal-Knotens.</span><span class="sxs-lookup"><span data-stu-id="9d36f-137">Name of the MAC address of the bare metal node.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-138">-Modell</span><span class="sxs-lookup"><span data-stu-id="9d36f-138">-Model</span></span>
<span data-ttu-id="9d36f-139">Modell des physikalischen Computers</span><span class="sxs-lookup"><span data-stu-id="9d36f-139">Model of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-140">-Name</span><span class="sxs-lookup"><span data-stu-id="9d36f-140">-Name</span></span>
<span data-ttu-id="9d36f-141">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="9d36f-141">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-142">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9d36f-142">-NoWait</span></span>
<span data-ttu-id="9d36f-143">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9d36f-143">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9d36f-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9d36f-144">-PassThru</span></span>
<span data-ttu-id="9d36f-145">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="9d36f-145">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9d36f-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d36f-146">-ResourceGroupName</span></span>
<span data-ttu-id="9d36f-147">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d36f-147">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-148">-Seriennummer</span><span class="sxs-lookup"><span data-stu-id="9d36f-148">-SerialNumber</span></span>
<span data-ttu-id="9d36f-149">Die Seriennummer des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-149">Serial number of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-150">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9d36f-150">-SubscriptionId</span></span>
<span data-ttu-id="9d36f-151">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9d36f-151">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9d36f-152">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d36f-152">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair, RepairExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-153">-Vendor</span><span class="sxs-lookup"><span data-stu-id="9d36f-153">-Vendor</span></span>
<span data-ttu-id="9d36f-154">Hersteller des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-154">Vendor of the physical machine.</span></span>

```yaml
Type: System.String
Parameter Sets: RepairExpanded, RepairViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-155">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9d36f-155">-Confirm</span></span>
<span data-ttu-id="9d36f-156">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d36f-156">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d36f-157">-WhatIf</span></span>
<span data-ttu-id="9d36f-158">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d36f-158">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9d36f-159">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d36f-159">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9d36f-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d36f-160">CommonParameters</span></span>
<span data-ttu-id="9d36f-161">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d36f-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d36f-162">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9d36f-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d36f-163">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9d36f-163">INPUTS</span></span>

### <span data-ttu-id="9d36f-164">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IBareMetalNodeDescription</span><span class="sxs-lookup"><span data-stu-id="9d36f-164">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IBareMetalNodeDescription</span></span>

### <span data-ttu-id="9d36f-165">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9d36f-165">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9d36f-166">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9d36f-166">OUTPUTS</span></span>

### <span data-ttu-id="9d36f-167">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9d36f-167">System.Boolean</span></span>



## <span data-ttu-id="9d36f-168">Notizen</span><span class="sxs-lookup"><span data-stu-id="9d36f-168">NOTES</span></span>

<span data-ttu-id="9d36f-169">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9d36f-169">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9d36f-170">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9d36f-170">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9d36f-171">BAREMETALNODE <IBareMetalNodeDescription> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d36f-171">BAREMETALNODE <IBareMetalNodeDescription>: Identity Parameter</span></span>
  - <span data-ttu-id="9d36f-172">`[BiosVersion <String>]`: BIOS-Version des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-172">`[BiosVersion <String>]`: Bios version of the physical machine.</span></span>
  - <span data-ttu-id="9d36f-173">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-173">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="9d36f-174">`[ClusterName <String>]`: Name des Clusters.</span><span class="sxs-lookup"><span data-stu-id="9d36f-174">`[ClusterName <String>]`: Name of the cluster.</span></span>
  - <span data-ttu-id="9d36f-175">`[ComputerName <String>]`: Name des Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-175">`[ComputerName <String>]`: Name of the computer.</span></span>
  - <span data-ttu-id="9d36f-176">`[MacAddress <String>]`: Name der Mac-Adresse des Bare Metal-Knotens.</span><span class="sxs-lookup"><span data-stu-id="9d36f-176">`[MacAddress <String>]`: Name of the MAC address of the bare metal node.</span></span>
  - <span data-ttu-id="9d36f-177">`[Model <String>]`: Modell des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-177">`[Model <String>]`: Model of the physical machine.</span></span>
  - <span data-ttu-id="9d36f-178">`[SerialNumber <String>]`: Seriennummer des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-178">`[SerialNumber <String>]`: Serial number of the physical machine.</span></span>
  - <span data-ttu-id="9d36f-179">`[Vendor <String>]`: Anbieter des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-179">`[Vendor <String>]`: Vendor of the physical machine.</span></span>

<span data-ttu-id="9d36f-180">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9d36f-180">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9d36f-181">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="9d36f-181">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9d36f-182">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="9d36f-182">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9d36f-183">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="9d36f-183">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9d36f-184">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="9d36f-184">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9d36f-185">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="9d36f-185">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9d36f-186">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="9d36f-186">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9d36f-187">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9d36f-187">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9d36f-188">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="9d36f-188">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9d36f-189">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="9d36f-189">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9d36f-190">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9d36f-190">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9d36f-191">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="9d36f-191">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9d36f-192">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="9d36f-192">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9d36f-193">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="9d36f-193">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9d36f-194">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="9d36f-194">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9d36f-195">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9d36f-195">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9d36f-196">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="9d36f-196">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9d36f-197">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="9d36f-197">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9d36f-198">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9d36f-198">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9d36f-199">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="9d36f-199">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9d36f-200">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="9d36f-200">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9d36f-201">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9d36f-201">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9d36f-202">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9d36f-202">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9d36f-203">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="9d36f-203">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9d36f-204">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9d36f-204">RELATED LINKS</span></span>

