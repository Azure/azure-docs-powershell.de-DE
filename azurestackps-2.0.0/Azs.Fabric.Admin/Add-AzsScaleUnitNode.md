---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/add-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 4546be57a2a2bd7f3f450290be2e0bf144e09817
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844844"
---
# <span data-ttu-id="5d03c-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5d03c-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="5d03c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d03c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d03c-103">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5d03c-103">Scales out a scale unit.</span></span>

## <span data-ttu-id="5d03c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d03c-104">SYNTAX</span></span>

### <span data-ttu-id="5d03c-105">ScaleExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="5d03c-105">ScaleExpanded (Default)</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AwaitStorageConvergence] [-NodeList <IScaleOutScaleUnitParameters[]>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d03c-106">Skalierung</span><span class="sxs-lookup"><span data-stu-id="5d03c-106">Scale</span></span>
```
Add-AzsScaleUnitNode -ScaleUnit <String> -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d03c-107">ScaleViaIdentity</span><span class="sxs-lookup"><span data-stu-id="5d03c-107">ScaleViaIdentity</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity>
 -ScaleUnitNodeParameter <IScaleOutScaleUnitParametersList> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="5d03c-108">ScaleViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="5d03c-108">ScaleViaIdentityExpanded</span></span>
```
Add-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-AwaitStorageConvergence]
 [-NodeList <IScaleOutScaleUnitParameters[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="5d03c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d03c-109">DESCRIPTION</span></span>
<span data-ttu-id="5d03c-110">Skaliert eine Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5d03c-110">Scales out a scale unit.</span></span>

## <span data-ttu-id="5d03c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d03c-111">EXAMPLES</span></span>

### <span data-ttu-id="5d03c-112">Beispiel 1: Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="5d03c-112">Example 1: Add-AzsScaleUnitNode</span></span>
```powershell
PS C:\> Add-AzsScaleUnitNode -NodeList $Nodes -ScaleUnit $ScaleUnitName

Adds a list of nodes to the scale unit.
```

<span data-ttu-id="5d03c-113">Fügen Sie einen neuen Skalierungseinheiten Knoten zu Ihrem Skalierungseinheiten Cluster hinzu.</span><span class="sxs-lookup"><span data-stu-id="5d03c-113">Add a new scale unit node to your scale unit cluster.</span></span>

## <span data-ttu-id="5d03c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d03c-114">PARAMETERS</span></span>

### <span data-ttu-id="5d03c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5d03c-115">-AsJob</span></span>
<span data-ttu-id="5d03c-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="5d03c-116">Run the command as a job</span></span>

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

### <span data-ttu-id="5d03c-117">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="5d03c-117">-AwaitStorageConvergence</span></span>
<span data-ttu-id="5d03c-118">Flag gibt an, ob der Vorgang auf eine Konvergenz des Speichers warten soll, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="5d03c-118">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="5d03c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d03c-119">-DefaultProfile</span></span>
<span data-ttu-id="5d03c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5d03c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d03c-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5d03c-121">-InputObject</span></span>
<span data-ttu-id="5d03c-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5d03c-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d03c-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="5d03c-123">-Location</span></span>
<span data-ttu-id="5d03c-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5d03c-124">Location of the resource.</span></span>

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

### <span data-ttu-id="5d03c-125">-Nodeliste</span><span class="sxs-lookup"><span data-stu-id="5d03c-125">-NodeList</span></span>
<span data-ttu-id="5d03c-126">Liste der Knoten in der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="5d03c-126">List of nodes in the scale unit.</span></span>
<span data-ttu-id="5d03c-127">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Knotenliste-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5d03c-127">To construct, see NOTES section for NODELIST properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d03c-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="5d03c-128">-NoWait</span></span>
<span data-ttu-id="5d03c-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="5d03c-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="5d03c-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d03c-130">-PassThru</span></span>
<span data-ttu-id="5d03c-131">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="5d03c-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="5d03c-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d03c-132">-ResourceGroupName</span></span>
<span data-ttu-id="5d03c-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d03c-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="5d03c-134">-ScaleUnit</span><span class="sxs-lookup"><span data-stu-id="5d03c-134">-ScaleUnit</span></span>
<span data-ttu-id="5d03c-135">Name der Skalierungseinheiten</span><span class="sxs-lookup"><span data-stu-id="5d03c-135">Name of the scale units.</span></span>

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

### <span data-ttu-id="5d03c-136">-ScaleUnitNodeParameter</span><span class="sxs-lookup"><span data-stu-id="5d03c-136">-ScaleUnitNodeParameter</span></span>
<span data-ttu-id="5d03c-137">Eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5d03c-137">A list of input data that allows for adding a set of scale unit nodes.</span></span>
<span data-ttu-id="5d03c-138">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für SCALEUNITNODEPARAMETER-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5d03c-138">To construct, see NOTES section for SCALEUNITNODEPARAMETER properties and create a hash table.</span></span>

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

### <span data-ttu-id="5d03c-139">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="5d03c-139">-SubscriptionId</span></span>
<span data-ttu-id="5d03c-140">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5d03c-140">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="5d03c-141">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5d03c-141">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="5d03c-142">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5d03c-142">-Confirm</span></span>
<span data-ttu-id="5d03c-143">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5d03c-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5d03c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d03c-144">-WhatIf</span></span>
<span data-ttu-id="5d03c-145">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5d03c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d03c-146">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5d03c-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5d03c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d03c-147">CommonParameters</span></span>
<span data-ttu-id="5d03c-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d03c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d03c-149">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5d03c-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d03c-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d03c-150">INPUTS</span></span>

### <span data-ttu-id="5d03c-151">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. Api20160501. IScaleOutScaleUnitParametersList</span><span class="sxs-lookup"><span data-stu-id="5d03c-151">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.Api20160501.IScaleOutScaleUnitParametersList</span></span>

### <span data-ttu-id="5d03c-152">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="5d03c-152">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="5d03c-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d03c-153">OUTPUTS</span></span>

### <span data-ttu-id="5d03c-154">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5d03c-154">System.Boolean</span></span>



## <span data-ttu-id="5d03c-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d03c-155">NOTES</span></span>

<span data-ttu-id="5d03c-156">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="5d03c-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="5d03c-157">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="5d03c-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="5d03c-158">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="5d03c-158">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="5d03c-159">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="5d03c-159">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="5d03c-160">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="5d03c-160">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="5d03c-161">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="5d03c-161">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="5d03c-162">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="5d03c-162">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="5d03c-163">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="5d03c-163">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="5d03c-164">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="5d03c-164">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="5d03c-165">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="5d03c-165">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="5d03c-166">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="5d03c-166">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="5d03c-167">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="5d03c-167">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="5d03c-168">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="5d03c-168">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="5d03c-169">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="5d03c-169">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="5d03c-170">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="5d03c-170">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="5d03c-171">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="5d03c-171">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="5d03c-172">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="5d03c-172">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="5d03c-173">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5d03c-173">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="5d03c-174">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="5d03c-174">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="5d03c-175">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5d03c-175">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="5d03c-176">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="5d03c-176">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="5d03c-177">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="5d03c-177">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="5d03c-178">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5d03c-178">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="5d03c-179">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="5d03c-179">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="5d03c-180">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="5d03c-180">`[Volume <String>]`: Name of the storage volume.</span></span>

<span data-ttu-id="5d03c-181">NodeList <IScaleOutScaleUnitParameters [] >: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5d03c-181">NODELIST <IScaleOutScaleUnitParameters[]>: List of nodes in the scale unit.</span></span>
  - <span data-ttu-id="5d03c-182">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="5d03c-182">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
  - <span data-ttu-id="5d03c-183">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="5d03c-183">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

<span data-ttu-id="5d03c-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList> : eine Liste mit Eingabedaten, die das Hinzufügen einer Gruppe von Skalierungseinheiten Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="5d03c-184">SCALEUNITNODEPARAMETER <IScaleOutScaleUnitParametersList>: A list of input data that allows for adding a set of scale unit nodes.</span></span>
  - <span data-ttu-id="5d03c-185">`[AwaitStorageConvergence <Boolean?>]`: Flag gibt an, ob der Vorgang warten soll, bis der Speicher konvergiert, bevor er zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="5d03c-185">`[AwaitStorageConvergence <Boolean?>]`: Flag indicates if the operation should wait for storage to converge before returning.</span></span>
  - <span data-ttu-id="5d03c-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: Liste der Knoten in der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="5d03c-186">`[NodeList <IScaleOutScaleUnitParameters[]>]`: List of nodes in the scale unit.</span></span>
    - <span data-ttu-id="5d03c-187">`[BmciPv4Address <String>]`: BMC-Adresse des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="5d03c-187">`[BmciPv4Address <String>]`: BMC address of the physical machine.</span></span>
    - <span data-ttu-id="5d03c-188">`[ComputerName <String>]`: Computer Name des physikalischen Computers.</span><span class="sxs-lookup"><span data-stu-id="5d03c-188">`[ComputerName <String>]`: Computer name of the physical machine.</span></span>

## <span data-ttu-id="5d03c-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d03c-189">RELATED LINKS</span></span>

