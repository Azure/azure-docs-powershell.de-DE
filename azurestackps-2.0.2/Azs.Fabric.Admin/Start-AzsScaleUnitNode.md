---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/start-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: c8b1ed8ea0be65e92022cf1ac759024a07fc76c4
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94006904"
---
# <span data-ttu-id="2104b-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2104b-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2104b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2104b-102">SYNOPSIS</span></span>
<span data-ttu-id="2104b-103">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="2104b-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="2104b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2104b-104">SYNTAX</span></span>

### <span data-ttu-id="2104b-105">PowerOn (Standard)</span><span class="sxs-lookup"><span data-stu-id="2104b-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="2104b-106">PowerOnViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2104b-106">PowerOnViaIdentity</span></span>
```
Start-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2104b-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2104b-107">DESCRIPTION</span></span>
<span data-ttu-id="2104b-108">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="2104b-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="2104b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2104b-109">EXAMPLES</span></span>

### <span data-ttu-id="2104b-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="2104b-110">Example 1:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="2104b-111">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="2104b-111">Power on a scale unit node.</span></span>

### <span data-ttu-id="2104b-112">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="2104b-112">Example 2:</span></span>
```powershell
PS C:\> Start-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="2104b-113">Schalten Sie den Knoten einer Skalierungseinheit ein.</span><span class="sxs-lookup"><span data-stu-id="2104b-113">Power on a scale unit node.</span></span> <span data-ttu-id="2104b-114">Als Job.</span><span class="sxs-lookup"><span data-stu-id="2104b-114">As a job.</span></span>

## <span data-ttu-id="2104b-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2104b-115">PARAMETERS</span></span>

### <span data-ttu-id="2104b-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2104b-116">-AsJob</span></span>
<span data-ttu-id="2104b-117">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="2104b-117">Run the command as a job</span></span>

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

### <span data-ttu-id="2104b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2104b-118">-DefaultProfile</span></span>
<span data-ttu-id="2104b-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2104b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2104b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="2104b-120">-Force</span></span>
<span data-ttu-id="2104b-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="2104b-121">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2104b-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2104b-122">-InputObject</span></span>
<span data-ttu-id="2104b-123">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="2104b-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity
Parameter Sets: PowerOnViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="2104b-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="2104b-124">-Location</span></span>
<span data-ttu-id="2104b-125">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2104b-125">Location of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2104b-126">-Name</span><span class="sxs-lookup"><span data-stu-id="2104b-126">-Name</span></span>
<span data-ttu-id="2104b-127">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="2104b-127">Name of the scale unit node.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2104b-128">-Nowait</span><span class="sxs-lookup"><span data-stu-id="2104b-128">-NoWait</span></span>
<span data-ttu-id="2104b-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="2104b-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2104b-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2104b-130">-PassThru</span></span>
<span data-ttu-id="2104b-131">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="2104b-131">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="2104b-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2104b-132">-ResourceGroupName</span></span>
<span data-ttu-id="2104b-133">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2104b-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2104b-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="2104b-134">-SubscriptionId</span></span>
<span data-ttu-id="2104b-135">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2104b-135">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2104b-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2104b-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2104b-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2104b-137">-Confirm</span></span>
<span data-ttu-id="2104b-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2104b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2104b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2104b-139">-WhatIf</span></span>
<span data-ttu-id="2104b-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2104b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2104b-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2104b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2104b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2104b-142">CommonParameters</span></span>
<span data-ttu-id="2104b-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2104b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2104b-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2104b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2104b-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2104b-145">INPUTS</span></span>

### <span data-ttu-id="2104b-146">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="2104b-146">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="2104b-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2104b-147">OUTPUTS</span></span>

### <span data-ttu-id="2104b-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2104b-148">System.Boolean</span></span>

## <span data-ttu-id="2104b-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="2104b-149">NOTES</span></span>

<span data-ttu-id="2104b-150">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="2104b-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2104b-151">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="2104b-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2104b-152">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="2104b-152">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2104b-153">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="2104b-153">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="2104b-154">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="2104b-154">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="2104b-155">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="2104b-155">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="2104b-156">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="2104b-156">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="2104b-157">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="2104b-157">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="2104b-158">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="2104b-158">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="2104b-159">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="2104b-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2104b-160">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="2104b-160">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="2104b-161">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="2104b-161">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="2104b-162">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="2104b-162">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="2104b-163">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="2104b-163">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="2104b-164">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="2104b-164">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="2104b-165">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="2104b-165">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="2104b-166">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="2104b-166">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="2104b-167">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2104b-167">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="2104b-168">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="2104b-168">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="2104b-169">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="2104b-169">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="2104b-170">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="2104b-170">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="2104b-171">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="2104b-171">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="2104b-172">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="2104b-172">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="2104b-173">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2104b-173">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2104b-174">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="2104b-174">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="2104b-175">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="2104b-175">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="2104b-176">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2104b-176">RELATED LINKS</span></span>
