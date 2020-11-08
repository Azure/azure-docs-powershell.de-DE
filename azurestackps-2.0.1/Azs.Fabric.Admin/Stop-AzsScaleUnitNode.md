---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: d413d7da00fe18de804306d0cfaa1ccade0e2650
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005415"
---
# <span data-ttu-id="4f66d-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="4f66d-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="4f66d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4f66d-102">SYNOPSIS</span></span>
<span data-ttu-id="4f66d-103">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="4f66d-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="4f66d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f66d-104">SYNTAX</span></span>

### <span data-ttu-id="4f66d-105">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="4f66d-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f66d-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f66d-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f66d-107">Gemäßen Beendigung</span><span class="sxs-lookup"><span data-stu-id="4f66d-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4f66d-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4f66d-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4f66d-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4f66d-109">DESCRIPTION</span></span>
<span data-ttu-id="4f66d-110">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="4f66d-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="4f66d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f66d-111">EXAMPLES</span></span>

### <span data-ttu-id="4f66d-112">Beispiel 1: {{Titel hier hinzufügen}}</span><span class="sxs-lookup"><span data-stu-id="4f66d-112">Example 1: {{ Add title here }}</span></span>
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="4f66d-113">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="4f66d-113">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="4f66d-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f66d-114">PARAMETERS</span></span>

### <span data-ttu-id="4f66d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4f66d-115">-AsJob</span></span>
<span data-ttu-id="4f66d-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4f66d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="4f66d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f66d-117">-DefaultProfile</span></span>
<span data-ttu-id="4f66d-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4f66d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f66d-119">-Force</span><span class="sxs-lookup"><span data-stu-id="4f66d-119">-Force</span></span>
<span data-ttu-id="4f66d-120">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4f66d-120">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4f66d-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4f66d-121">-InputObject</span></span>
<span data-ttu-id="4f66d-122">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="4f66d-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity, ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4f66d-123">-Standort</span><span class="sxs-lookup"><span data-stu-id="4f66d-123">-Location</span></span>
<span data-ttu-id="4f66d-124">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f66d-124">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f66d-125">-Name</span><span class="sxs-lookup"><span data-stu-id="4f66d-125">-Name</span></span>
<span data-ttu-id="4f66d-126">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="4f66d-126">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f66d-127">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4f66d-127">-NoWait</span></span>
<span data-ttu-id="4f66d-128">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4f66d-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4f66d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f66d-129">-PassThru</span></span>
<span data-ttu-id="4f66d-130">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="4f66d-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4f66d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f66d-131">-ResourceGroupName</span></span>
<span data-ttu-id="4f66d-132">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="4f66d-132">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f66d-133">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="4f66d-133">-SubscriptionId</span></span>
<span data-ttu-id="4f66d-134">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4f66d-134">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4f66d-135">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4f66d-135">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff, Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4f66d-136">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4f66d-136">-Confirm</span></span>
<span data-ttu-id="4f66d-137">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f66d-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4f66d-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4f66d-138">-WhatIf</span></span>
<span data-ttu-id="4f66d-139">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4f66d-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4f66d-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4f66d-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4f66d-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f66d-141">CommonParameters</span></span>
<span data-ttu-id="4f66d-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f66d-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f66d-143">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4f66d-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f66d-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4f66d-144">INPUTS</span></span>

### <span data-ttu-id="4f66d-145">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4f66d-145">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="4f66d-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4f66d-146">OUTPUTS</span></span>

### <span data-ttu-id="4f66d-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4f66d-147">System.Boolean</span></span>



## <span data-ttu-id="4f66d-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4f66d-148">NOTES</span></span>

<span data-ttu-id="4f66d-149">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="4f66d-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4f66d-150">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="4f66d-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4f66d-151">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="4f66d-151">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4f66d-152">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="4f66d-152">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="4f66d-153">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="4f66d-153">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="4f66d-154">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="4f66d-154">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="4f66d-155">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="4f66d-155">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="4f66d-156">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="4f66d-156">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="4f66d-157">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="4f66d-157">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="4f66d-158">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="4f66d-158">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4f66d-159">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="4f66d-159">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="4f66d-160">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="4f66d-160">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="4f66d-161">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="4f66d-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="4f66d-162">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="4f66d-162">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="4f66d-163">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="4f66d-163">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="4f66d-164">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="4f66d-164">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="4f66d-165">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="4f66d-165">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="4f66d-166">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4f66d-166">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="4f66d-167">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="4f66d-167">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="4f66d-168">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="4f66d-168">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="4f66d-169">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="4f66d-169">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="4f66d-170">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="4f66d-170">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="4f66d-171">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="4f66d-171">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="4f66d-172">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4f66d-172">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="4f66d-173">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="4f66d-173">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4f66d-174">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="4f66d-174">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="4f66d-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4f66d-175">RELATED LINKS</span></span>

