---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/powershell/module/azs.fabric.admin/restart-azsinfrastructureroleinstance
schema: 2.0.0
ms.openlocfilehash: 5762cbd1c972f5500a15be8fea8595165add3afc
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005373"
---
# <span data-ttu-id="9de05-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="9de05-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="9de05-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9de05-102">SYNOPSIS</span></span>
<span data-ttu-id="9de05-103">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="9de05-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="9de05-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9de05-104">SYNTAX</span></span>

### <span data-ttu-id="9de05-105">Neustart (Standard)</span><span class="sxs-lookup"><span data-stu-id="9de05-105">Reboot (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9de05-106">RebootViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9de05-106">RebootViaIdentity</span></span>
```
Restart-AzsInfrastructureRoleInstance -InputObject <IFabricAdminIdentity> [-Force]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9de05-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9de05-107">DESCRIPTION</span></span>
<span data-ttu-id="9de05-108">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="9de05-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="9de05-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9de05-109">EXAMPLES</span></span>

### <span data-ttu-id="9de05-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="9de05-110">Example 1:</span></span>
```powershell
PS C:\> Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"

```

<span data-ttu-id="9de05-111">Starten Sie eine Infrastrukturrollen Instanz neu.</span><span class="sxs-lookup"><span data-stu-id="9de05-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="9de05-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9de05-112">PARAMETERS</span></span>

### <span data-ttu-id="9de05-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9de05-113">-AsJob</span></span>
<span data-ttu-id="9de05-114">Führen Sie asynchron als Auftrag aus, und geben Sie das Auftragsobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="9de05-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="9de05-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9de05-115">-DefaultProfile</span></span>
<span data-ttu-id="9de05-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9de05-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9de05-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9de05-117">-Force</span></span>
<span data-ttu-id="9de05-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="9de05-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="9de05-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9de05-119">-InputObject</span></span>
<span data-ttu-id="9de05-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9de05-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: RebootViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9de05-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="9de05-121">-Location</span></span>
<span data-ttu-id="9de05-122">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9de05-122">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9de05-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9de05-123">-Name</span></span>
<span data-ttu-id="9de05-124">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="9de05-124">Name of an infrastructure role instance.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9de05-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9de05-125">-NoWait</span></span>
<span data-ttu-id="9de05-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9de05-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9de05-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9de05-127">-PassThru</span></span>
<span data-ttu-id="9de05-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="9de05-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9de05-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9de05-129">-ResourceGroupName</span></span>
<span data-ttu-id="9de05-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9de05-130">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```
### <span data-ttu-id="9de05-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="9de05-131">-SubscriptionId</span></span>
<span data-ttu-id="9de05-132">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9de05-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9de05-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9de05-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Reboot
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9de05-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9de05-134">-Confirm</span></span>
<span data-ttu-id="9de05-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9de05-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9de05-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9de05-136">-WhatIf</span></span>
<span data-ttu-id="9de05-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9de05-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9de05-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9de05-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9de05-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9de05-139">CommonParameters</span></span>
<span data-ttu-id="9de05-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9de05-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9de05-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9de05-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9de05-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9de05-142">INPUTS</span></span>

### <span data-ttu-id="9de05-143">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9de05-143">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="9de05-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9de05-144">OUTPUTS</span></span>

### <span data-ttu-id="9de05-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9de05-145">System.Boolean</span></span>



## <span data-ttu-id="9de05-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="9de05-146">NOTES</span></span>

<span data-ttu-id="9de05-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9de05-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9de05-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="9de05-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9de05-149">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="9de05-149">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9de05-150">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="9de05-150">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="9de05-151">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="9de05-151">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="9de05-152">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="9de05-152">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="9de05-153">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="9de05-153">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="9de05-154">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="9de05-154">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="9de05-155">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="9de05-155">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="9de05-156">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="9de05-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9de05-157">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="9de05-157">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="9de05-158">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="9de05-158">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="9de05-159">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="9de05-159">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="9de05-160">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="9de05-160">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="9de05-161">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="9de05-161">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="9de05-162">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="9de05-162">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="9de05-163">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="9de05-163">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="9de05-164">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9de05-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="9de05-165">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="9de05-165">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="9de05-166">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="9de05-166">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="9de05-167">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9de05-167">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="9de05-168">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="9de05-168">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="9de05-169">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="9de05-169">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="9de05-170">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9de05-170">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="9de05-171">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="9de05-171">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9de05-172">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="9de05-172">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="9de05-173">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9de05-173">RELATED LINKS</span></span>

