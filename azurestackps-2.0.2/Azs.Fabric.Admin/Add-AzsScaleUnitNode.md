---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: fe7726c25ee9dd83ca940b4ac6e47b3cc26a6457
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006919"
---
# <span data-ttu-id="8c8cc-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8c8cc-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="8c8cc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8c8cc-102">SYNOPSIS</span></span>
<span data-ttu-id="8c8cc-103">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="8c8cc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8c8cc-104">SYNTAX</span></span>

### <span data-ttu-id="8c8cc-105">ScaleExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="8c8cc-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-BmciPv4Address <String>] [-ComputerName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c8cc-106">Skalierung</span><span class="sxs-lookup"><span data-stu-id="8c8cc-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c8cc-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c8cc-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="8c8cc-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="8c8cc-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-BmciPv4Address <String>] [-ComputerName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c8cc-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8c8cc-109">DESCRIPTION</span></span>
<span data-ttu-id="8c8cc-110">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="8c8cc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8c8cc-111">EXAMPLES</span></span>

### <span data-ttu-id="8c8cc-112">Beispiel 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="8c8cc-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -BmciPv4Address $BmciPv4Address -ComputerName $ComputerName -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="8c8cc-113">Fügen Sie einen neuen Skalierungseinheiten Knoten zu Ihrem Skalierungseinheiten Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="8c8cc-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8cc-114">PARAMETERS</span></span>

### <span data-ttu-id="8c8cc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c8cc-115">-AsJob</span></span>
<span data-ttu-id="8c8cc-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="8c8cc-116">Run the command as a job</span></span>

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

### <span data-ttu-id="8c8cc-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="8c8cc-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="8c8cc-118">Flag gibt an, ob der Vorgang auf eine Konvergenz des Speichers warten soll, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c8cc-119">-DefaultProfile</span></span>
<span data-ttu-id="8c8cc-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c8cc-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8c8cc-121">-InputObject</span></span>
<span data-ttu-id="8c8cc-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ScaleViaIdentity, ScaleViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="8c8cc-123">-Location</span></span>
<span data-ttu-id="8c8cc-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-125">-BmciPv4Address</span><span class="sxs-lookup"><span data-stu-id="8c8cc-125">-BmciPv4Address</span></span> 
<span data-ttu-id="8c8cc-126">BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-126">BMC address of the physical machine.</span></span>

### <span data-ttu-id="8c8cc-127">-Computername</span><span class="sxs-lookup"><span data-stu-id="8c8cc-127">-ComputerName</span></span> 
<span data-ttu-id="8c8cc-128">Der Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-128">Computer name of the physical machine.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParameters[]
Parameter Sets: ScaleExpanded, ScaleViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8c8cc-129">-NoWait</span></span>
<span data-ttu-id="8c8cc-130">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="8c8cc-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c8cc-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c8cc-131">-PassThru</span></span>
<span data-ttu-id="8c8cc-132">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="8c8cc-132">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c8cc-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c8cc-133">-ResourceGroupName</span></span>
<span data-ttu-id="8c8cc-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-134">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-135">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="8c8cc-135">-ScaleUnit</span></span>
<span data-ttu-id="8c8cc-136">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="8c8cc-136">Name of the scale units.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-137">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="8c8cc-137">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="8c8cc-138">Eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-138">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="8c8cc-139">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SCALEUNITNODEPARAMETER-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-139">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList
Parameter Sets: Scale, ScaleViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-140">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="8c8cc-140">-SubscriptionId</span></span>
<span data-ttu-id="8c8cc-141">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-141">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c8cc-142">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-142">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Scale, ScaleExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c8cc-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8c8cc-143">-Confirm</span></span>
<span data-ttu-id="8c8cc-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c8cc-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c8cc-145">-WhatIf</span></span>
<span data-ttu-id="8c8cc-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c8cc-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c8cc-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c8cc-148">CommonParameters</span></span>
<span data-ttu-id="8c8cc-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c8cc-150">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c8cc-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c8cc-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8c8cc-151">INPUTS</span></span>

### <span data-ttu-id="8c8cc-152">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="8c8cc-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="8c8cc-153">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="8c8cc-153">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="8c8cc-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8c8cc-154">OUTPUTS</span></span>

### <span data-ttu-id="8c8cc-155">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8c8cc-155">System.Boolean</span></span>

## <span data-ttu-id="8c8cc-156">Notizen</span><span class="sxs-lookup"><span data-stu-id="8c8cc-156">NOTES</span></span>

<span data-ttu-id="8c8cc-157">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-157">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c8cc-158">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-158">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8c8cc-159">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="8c8cc-159">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c8cc-160">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-160">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="8c8cc-161">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-161">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="8c8cc-162">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-162">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="8c8cc-163">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-163">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="8c8cc-164">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-164">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="8c8cc-165">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-165">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="8c8cc-166">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="8c8cc-166">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c8cc-167">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="8c8cc-167">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="8c8cc-168">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-168">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="8c8cc-169">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-169">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8c8cc-170">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-170">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="8c8cc-171">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-171">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="8c8cc-172">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-172">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="8c8cc-173">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-173">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="8c8cc-174">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-174">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="8c8cc-175">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-175">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="8c8cc-176">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-176">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="8c8cc-177">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-177">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="8c8cc-178">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-178">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="8c8cc-179">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-179">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="8c8cc-180">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-180">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8c8cc-181">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-181">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="8c8cc-182">NodeList <IScaleOutScaleUnitParameters [] >: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-182">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="8c8cc-183">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-183">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="8c8cc-184">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-184">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="8c8cc-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-185">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="8c8cc-186">`[AwaitStorageConvergence <Boolean?>]`: Flag gibt an, ob der Vorgang warten soll, bis der Speicher konvergiert, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-186">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="8c8cc-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-187">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="8c8cc-188">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-188">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="8c8cc-189">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="8c8cc-189">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="8c8cc-190">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8c8cc-190">RELATED LINKS</span></span>
