---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/disable-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: d6bb118a6b7699672209618e1409fe6a9bed466d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006916"
---
# <span data-ttu-id="85cab-101">Disable-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="85cab-101">Disable-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="85cab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="85cab-102">SYNOPSIS</span></span>


## <span data-ttu-id="85cab-103">Syntax</span><span class="sxs-lookup"><span data-stu-id="85cab-103">SYNTAX</span></span>

### <span data-ttu-id="85cab-104">Shutdown (Standard)</span><span class="sxs-lookup"><span data-stu-id="85cab-104">Shutdown (Default)</span></span>
```
Disable-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="85cab-105">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="85cab-105">ShutdownViaIdentity</span></span>
```
Disable-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="85cab-106">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85cab-106">DESCRIPTION</span></span>
<span data-ttu-id="85cab-107">Herunterfahren einer Infrastrukturrollen Instanz für die Wartung.</span><span class="sxs-lookup"><span data-stu-id="85cab-107">Shutdown an infrastructure role instance for maintenance.</span></span>

## <span data-ttu-id="85cab-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="85cab-108">EXAMPLES</span></span>

### <span data-ttu-id="85cab-109">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="85cab-109">Example 1:</span></span>
```powershell
PS C:\> Disable-AzsInfrastructureRoleInstance -Name "n22r0903-Xrp03"

Shutdown an infrastructure role instance for maintenance.
```

<span data-ttu-id="85cab-110">Herunterfahren einer Infrastrukturrollen Instanz für die Wartung.</span><span class="sxs-lookup"><span data-stu-id="85cab-110">Shutdown an infrastructure role instance for maintenance.</span></span>


## <span data-ttu-id="85cab-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="85cab-111">PARAMETERS</span></span>

### <span data-ttu-id="85cab-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="85cab-112">-AsJob</span></span>
<span data-ttu-id="85cab-113">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="85cab-113">Run the command as a job</span></span>

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

### <span data-ttu-id="85cab-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85cab-114">-DefaultProfile</span></span>
<span data-ttu-id="85cab-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="85cab-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85cab-116">-Force</span><span class="sxs-lookup"><span data-stu-id="85cab-116">-Force</span></span>
<span data-ttu-id="85cab-117">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="85cab-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="85cab-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="85cab-118">-InputObject</span></span>
<span data-ttu-id="85cab-119">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="85cab-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: ShutdownViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="85cab-120">-Standort</span><span class="sxs-lookup"><span data-stu-id="85cab-120">-Location</span></span>
<span data-ttu-id="85cab-121">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="85cab-121">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85cab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="85cab-122">-Name</span></span>
<span data-ttu-id="85cab-123">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="85cab-123">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85cab-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="85cab-124">-NoWait</span></span>
<span data-ttu-id="85cab-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="85cab-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="85cab-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85cab-126">-PassThru</span></span>
<span data-ttu-id="85cab-127">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="85cab-127">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="85cab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85cab-128">-ResourceGroupName</span></span>
<span data-ttu-id="85cab-129">Ressourcengruppe, in der der Ressourcenanbieter registriert wurde.</span><span class="sxs-lookup"><span data-stu-id="85cab-129">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85cab-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="85cab-130">-SubscriptionId</span></span>
<span data-ttu-id="85cab-131">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="85cab-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="85cab-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="85cab-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="85cab-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="85cab-133">-Confirm</span></span>
<span data-ttu-id="85cab-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85cab-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85cab-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85cab-135">-WhatIf</span></span>
<span data-ttu-id="85cab-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85cab-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85cab-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85cab-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85cab-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85cab-138">CommonParameters</span></span>
<span data-ttu-id="85cab-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85cab-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85cab-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="85cab-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85cab-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="85cab-141">INPUTS</span></span>

### <span data-ttu-id="85cab-142">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="85cab-142">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="85cab-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="85cab-143">OUTPUTS</span></span>

### <span data-ttu-id="85cab-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="85cab-144">System.Boolean</span></span>



## <span data-ttu-id="85cab-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="85cab-145">NOTES</span></span>

<span data-ttu-id="85cab-146">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="85cab-146">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="85cab-147">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="85cab-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="85cab-148">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="85cab-148">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="85cab-149">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="85cab-149">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="85cab-150">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="85cab-150">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="85cab-151">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="85cab-151">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="85cab-152">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="85cab-152">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="85cab-153">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="85cab-153">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="85cab-154">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="85cab-154">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="85cab-155">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="85cab-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="85cab-156">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="85cab-156">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="85cab-157">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="85cab-157">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="85cab-158">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="85cab-158">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="85cab-159">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="85cab-159">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="85cab-160">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="85cab-160">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="85cab-161">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="85cab-161">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="85cab-162">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="85cab-162">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="85cab-163">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="85cab-163">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="85cab-164">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="85cab-164">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="85cab-165">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="85cab-165">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="85cab-166">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="85cab-166">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="85cab-167">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="85cab-167">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="85cab-168">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="85cab-168">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="85cab-169">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="85cab-169">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="85cab-170">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="85cab-170">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="85cab-171">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="85cab-171">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="85cab-172">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="85cab-172">RELATED LINKS</span></span>

