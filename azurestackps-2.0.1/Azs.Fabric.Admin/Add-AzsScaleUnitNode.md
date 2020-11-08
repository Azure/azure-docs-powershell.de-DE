---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005585"
---
# <span data-ttu-id="2cd44-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2cd44-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2cd44-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2cd44-102">SYNOPSIS</span></span>
<span data-ttu-id="2cd44-103">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2cd44-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="2cd44-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2cd44-104">SYNTAX</span></span>

### <span data-ttu-id="2cd44-105">ScaleExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="2cd44-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cd44-106">Skalierung</span><span class="sxs-lookup"><span data-stu-id="2cd44-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cd44-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2cd44-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2cd44-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="2cd44-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2cd44-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2cd44-109">DESCRIPTION</span></span>
<span data-ttu-id="2cd44-110">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2cd44-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="2cd44-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2cd44-111">EXAMPLES</span></span>

### <span data-ttu-id="2cd44-112">Beispiel 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2cd44-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="2cd44-113">Fügen Sie einen neuen Skalierungseinheiten Knoten zu Ihrem Skalierungseinheiten Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="2cd44-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="2cd44-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="2cd44-114">PARAMETERS</span></span>

### <span data-ttu-id="2cd44-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2cd44-115">-AsJob</span></span>
<span data-ttu-id="2cd44-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2cd44-116">Run the command as a job</span></span>

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

### <span data-ttu-id="2cd44-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="2cd44-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="2cd44-118">Flag gibt an, ob der Vorgang auf eine Konvergenz des Speichers warten soll, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="2cd44-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="2cd44-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cd44-119">-DefaultProfile</span></span>
<span data-ttu-id="2cd44-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2cd44-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2cd44-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2cd44-121">-InputObject</span></span>
<span data-ttu-id="2cd44-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2cd44-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2cd44-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="2cd44-123">-Location</span></span>
<span data-ttu-id="2cd44-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2cd44-124">Location of the resource.</span></span>

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

### <span data-ttu-id="2cd44-125">-Nodeliste</span><span class="sxs-lookup"><span data-stu-id="2cd44-125">-NodeList</span></span>
<span data-ttu-id="2cd44-126">Liste der Knoten in der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="2cd44-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="2cd44-127">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Knotenliste-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2cd44-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="2cd44-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2cd44-128">-NoWait</span></span>
<span data-ttu-id="2cd44-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2cd44-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2cd44-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2cd44-130">-PassThru</span></span>
<span data-ttu-id="2cd44-131">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2cd44-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2cd44-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cd44-132">-ResourceGroupName</span></span>
<span data-ttu-id="2cd44-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cd44-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="2cd44-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="2cd44-134">-ScaleUnit</span></span>
<span data-ttu-id="2cd44-135">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="2cd44-135">Name of the scale units.</span></span>

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

### <span data-ttu-id="2cd44-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="2cd44-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="2cd44-137">Eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2cd44-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="2cd44-138">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SCALEUNITNODEPARAMETER-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2cd44-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="2cd44-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2cd44-139">-SubscriptionId</span></span>
<span data-ttu-id="2cd44-140">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2cd44-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2cd44-141">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2cd44-141">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2cd44-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2cd44-142">-Confirm</span></span>
<span data-ttu-id="2cd44-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2cd44-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2cd44-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2cd44-144">-WhatIf</span></span>
<span data-ttu-id="2cd44-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2cd44-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2cd44-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2cd44-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2cd44-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cd44-147">CommonParameters</span></span>
<span data-ttu-id="2cd44-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cd44-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cd44-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2cd44-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cd44-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2cd44-150">INPUTS</span></span>

### <span data-ttu-id="2cd44-151">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="2cd44-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="2cd44-152">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2cd44-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2cd44-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2cd44-153">OUTPUTS</span></span>

### <span data-ttu-id="2cd44-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2cd44-154">System.Boolean</span></span>



## <span data-ttu-id="2cd44-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="2cd44-155">NOTES</span></span>

<span data-ttu-id="2cd44-156">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2cd44-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2cd44-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2cd44-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2cd44-158">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2cd44-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2cd44-159">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="2cd44-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2cd44-160">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="2cd44-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2cd44-161">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="2cd44-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2cd44-162">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="2cd44-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2cd44-163">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="2cd44-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2cd44-164">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="2cd44-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2cd44-165">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2cd44-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2cd44-166">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="2cd44-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2cd44-167">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="2cd44-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2cd44-168">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2cd44-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2cd44-169">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2cd44-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2cd44-170">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="2cd44-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2cd44-171">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="2cd44-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2cd44-172">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="2cd44-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2cd44-173">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2cd44-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2cd44-174">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="2cd44-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2cd44-175">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2cd44-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2cd44-176">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="2cd44-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2cd44-177">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="2cd44-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2cd44-178">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2cd44-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2cd44-179">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2cd44-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2cd44-180">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="2cd44-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="2cd44-181">NodeList <IScaleOutScaleUnitParameters [] >: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2cd44-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="2cd44-182">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="2cd44-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="2cd44-183">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="2cd44-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="2cd44-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="2cd44-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="2cd44-185">`[AwaitStorageConvergence <Boolean?>]`: Flag gibt an, ob der Vorgang warten soll, bis der Speicher konvergiert, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="2cd44-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="2cd44-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2cd44-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="2cd44-187">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="2cd44-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="2cd44-188">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="2cd44-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="2cd44-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2cd44-189">RELATED LINKS</span></span>

