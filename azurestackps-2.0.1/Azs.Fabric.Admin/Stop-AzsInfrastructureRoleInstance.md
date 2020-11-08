---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/stop-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 07751ba4228faa578e4181ec481eef6e5b033126
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005402"
---
# <span data-ttu-id="2efc5-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="2efc5-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="2efc5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2efc5-102">SYNOPSIS</span></span>
<span data-ttu-id="2efc5-103">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="2efc5-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="2efc5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2efc5-104">SYNTAX</span></span>

### <span data-ttu-id="2efc5-105">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="2efc5-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2efc5-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2efc5-106">PowerOffViaIdentity</span></span>
```
Stop-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2efc5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2efc5-107">DESCRIPTION</span></span>
<span data-ttu-id="2efc5-108">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="2efc5-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="2efc5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2efc5-109">EXAMPLES</span></span>

### <span data-ttu-id="2efc5-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2efc5-110">Example 1:</span></span> 
```powershell
PS C:\> Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"

```

<span data-ttu-id="2efc5-111">Schalten Sie eine Infrastrukturrollen Instanz aus.</span><span class="sxs-lookup"><span data-stu-id="2efc5-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="2efc5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2efc5-112">PARAMETERS</span></span>

### <span data-ttu-id="2efc5-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2efc5-113">-AsJob</span></span>
<span data-ttu-id="2efc5-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2efc5-114">Run the command as a job</span></span>

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

### <span data-ttu-id="2efc5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2efc5-115">-DefaultProfile</span></span>
<span data-ttu-id="2efc5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2efc5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2efc5-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2efc5-117">-Force</span></span>
<span data-ttu-id="2efc5-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2efc5-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2efc5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2efc5-119">-InputObject</span></span>
<span data-ttu-id="2efc5-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2efc5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOffViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2efc5-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="2efc5-121">-Location</span></span>
<span data-ttu-id="2efc5-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2efc5-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2efc5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2efc5-123">-Name</span></span>
<span data-ttu-id="2efc5-124">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="2efc5-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2efc5-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2efc5-125">-NoWait</span></span>
<span data-ttu-id="2efc5-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2efc5-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2efc5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2efc5-127">-PassThru</span></span>
<span data-ttu-id="2efc5-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2efc5-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2efc5-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2efc5-129">-ResourceGroupName</span></span>
<span data-ttu-id="2efc5-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2efc5-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2efc5-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2efc5-131">-SubscriptionId</span></span>
<span data-ttu-id="2efc5-132">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2efc5-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2efc5-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2efc5-133">The subscription ID forms part of the URI for every service call.</span></span>


```yaml
Type: System.String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2efc5-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2efc5-134">-Confirm</span></span>
<span data-ttu-id="2efc5-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2efc5-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2efc5-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2efc5-136">-WhatIf</span></span>
<span data-ttu-id="2efc5-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2efc5-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2efc5-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2efc5-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2efc5-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2efc5-139">CommonParameters</span></span>
<span data-ttu-id="2efc5-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2efc5-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2efc5-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2efc5-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2efc5-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2efc5-142">INPUTS</span></span>

### <span data-ttu-id="2efc5-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2efc5-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2efc5-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2efc5-144">OUTPUTS</span></span>

### <span data-ttu-id="2efc5-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2efc5-145">System.Boolean</span></span>



## <span data-ttu-id="2efc5-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="2efc5-146">NOTES</span></span>

<span data-ttu-id="2efc5-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2efc5-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2efc5-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2efc5-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2efc5-149">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2efc5-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2efc5-150">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="2efc5-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2efc5-151">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="2efc5-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2efc5-152">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="2efc5-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2efc5-153">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="2efc5-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2efc5-154">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="2efc5-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2efc5-155">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="2efc5-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2efc5-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2efc5-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2efc5-157">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="2efc5-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2efc5-158">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="2efc5-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2efc5-159">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2efc5-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2efc5-160">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2efc5-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2efc5-161">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="2efc5-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2efc5-162">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="2efc5-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2efc5-163">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="2efc5-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2efc5-164">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2efc5-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2efc5-165">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="2efc5-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2efc5-166">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2efc5-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2efc5-167">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="2efc5-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2efc5-168">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="2efc5-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2efc5-169">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="2efc5-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2efc5-170">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2efc5-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2efc5-171">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2efc5-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2efc5-172">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="2efc5-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2efc5-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2efc5-173">RELATED LINKS</span></span>

