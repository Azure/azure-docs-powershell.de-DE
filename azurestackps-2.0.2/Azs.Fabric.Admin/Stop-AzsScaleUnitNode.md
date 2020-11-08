---
external help file: ''
Module Name: Azs.Fabric.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.fabric.admin/stop-azsscaleunitnode
schema: 2.0.0
ms.openlocfilehash: 3f5adef6382038fdaf8c17620508b4a450ff74bc
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/08/2020
ms.locfileid: "94007015"
---
# <span data-ttu-id="109ae-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="109ae-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="109ae-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="109ae-102">SYNOPSIS</span></span>
<span data-ttu-id="109ae-103">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="109ae-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="109ae-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="109ae-104">SYNTAX</span></span>

### <span data-ttu-id="109ae-105">PowerOff (Standard)</span><span class="sxs-lookup"><span data-stu-id="109ae-105">PowerOff (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="109ae-106">PowerOffViaIdentity</span><span class="sxs-lookup"><span data-stu-id="109ae-106">PowerOffViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="109ae-107">Gemäßen Beendigung</span><span class="sxs-lookup"><span data-stu-id="109ae-107">Shutdown</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-Force] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="109ae-108">ShutdownViaIdentity</span><span class="sxs-lookup"><span data-stu-id="109ae-108">ShutdownViaIdentity</span></span>
```
Stop-AzsScaleUnitNode -InputObject <IFabricAdminIdentity> [-Force] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="109ae-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="109ae-109">DESCRIPTION</span></span>
<span data-ttu-id="109ae-110">Schalten Sie einen Skalierungseinheit-Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="109ae-110">Power off a scale unit node.</span></span>

## <span data-ttu-id="109ae-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="109ae-111">EXAMPLES</span></span>

### <span data-ttu-id="109ae-112">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="109ae-112">Example 1:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="109ae-113">Schalten Sie einen Knoten der Skalierungseinheit herunter.</span><span class="sxs-lookup"><span data-stu-id="109ae-113">Power down a scale unit node.</span></span>

### <span data-ttu-id="109ae-114">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="109ae-114">Example 2:</span></span>
```powershell
PS C:\> Stop-AzsScaleUnitNode -Name "HC1n25r2236" -AsJob
```

<span data-ttu-id="109ae-115">Schalten Sie einen Knoten der Skalierungseinheit herunter.</span><span class="sxs-lookup"><span data-stu-id="109ae-115">Power down a scale unit node.</span></span> <span data-ttu-id="109ae-116">Als Job.</span><span class="sxs-lookup"><span data-stu-id="109ae-116">As a job.</span></span>

## <span data-ttu-id="109ae-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="109ae-117">PARAMETERS</span></span>

### <span data-ttu-id="109ae-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="109ae-118">-AsJob</span></span>
<span data-ttu-id="109ae-119">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="109ae-119">Run the command as a job</span></span>

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

### <span data-ttu-id="109ae-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="109ae-120">-DefaultProfile</span></span>
<span data-ttu-id="109ae-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="109ae-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="109ae-122">-Force</span><span class="sxs-lookup"><span data-stu-id="109ae-122">-Force</span></span>
<span data-ttu-id="109ae-123">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="109ae-123">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="109ae-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="109ae-124">-InputObject</span></span>
<span data-ttu-id="109ae-125">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="109ae-125">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="109ae-126">-Standort</span><span class="sxs-lookup"><span data-stu-id="109ae-126">-Location</span></span>
<span data-ttu-id="109ae-127">Der Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="109ae-127">Location of the resource.</span></span>

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

### <span data-ttu-id="109ae-128">-Name</span><span class="sxs-lookup"><span data-stu-id="109ae-128">-Name</span></span>
<span data-ttu-id="109ae-129">Der Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="109ae-129">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="109ae-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="109ae-130">-NoWait</span></span>
<span data-ttu-id="109ae-131">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="109ae-131">Run the command asynchronously</span></span>

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

### <span data-ttu-id="109ae-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="109ae-132">-PassThru</span></span>
<span data-ttu-id="109ae-133">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="109ae-133">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="109ae-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="109ae-134">-ResourceGroupName</span></span>
<span data-ttu-id="109ae-135">Name des Knotens der Skalierungseinheit</span><span class="sxs-lookup"><span data-stu-id="109ae-135">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="109ae-136">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="109ae-136">-SubscriptionId</span></span>
<span data-ttu-id="109ae-137">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="109ae-137">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="109ae-138">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="109ae-138">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="109ae-139">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="109ae-139">-Confirm</span></span>
<span data-ttu-id="109ae-140">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="109ae-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="109ae-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="109ae-141">-WhatIf</span></span>
<span data-ttu-id="109ae-142">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="109ae-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="109ae-143">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="109ae-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="109ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="109ae-144">CommonParameters</span></span>
<span data-ttu-id="109ae-145">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="109ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="109ae-146">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="109ae-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="109ae-147">Eingaben</span><span class="sxs-lookup"><span data-stu-id="109ae-147">INPUTS</span></span>

### <span data-ttu-id="109ae-148">Microsoft. Azure. PowerShell. Cmdlets. FabricAdmin. Models. IFabricAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="109ae-148">Microsoft.Azure.PowerShell.Cmdlets.FabricAdmin.Models.IFabricAdminIdentity</span></span>

## <span data-ttu-id="109ae-149">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="109ae-149">OUTPUTS</span></span>

### <span data-ttu-id="109ae-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="109ae-150">System.Boolean</span></span>

## <span data-ttu-id="109ae-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="109ae-151">NOTES</span></span>

<span data-ttu-id="109ae-152">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="109ae-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="109ae-153">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="109ae-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="109ae-154">Inputobject <IFabricAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="109ae-154">INPUTOBJECT <IFabricAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="109ae-155">`[Drive <String>]`: Name des Speicherlaufwerks.</span><span class="sxs-lookup"><span data-stu-id="109ae-155">`[Drive <String>]`: Name of the storage drive.</span></span>
  - <span data-ttu-id="109ae-156">`[EdgeGateway <String>]`: Name des Edge-Gateways.</span><span class="sxs-lookup"><span data-stu-id="109ae-156">`[EdgeGateway <String>]`: Name of the edge gateway.</span></span>
  - <span data-ttu-id="109ae-157">`[EdgeGatewayPool <String>]`: Name des Edge-Gateway-Pools.</span><span class="sxs-lookup"><span data-stu-id="109ae-157">`[EdgeGatewayPool <String>]`: Name of the edge gateway pool.</span></span>
  - <span data-ttu-id="109ae-158">`[FabricLocation <String>]`: Fabric-Standort.</span><span class="sxs-lookup"><span data-stu-id="109ae-158">`[FabricLocation <String>]`: Fabric location.</span></span>
  - <span data-ttu-id="109ae-159">`[FileShare <String>]`: Fabric-Dateifreigabe Name.</span><span class="sxs-lookup"><span data-stu-id="109ae-159">`[FileShare <String>]`: Fabric file share name.</span></span>
  - <span data-ttu-id="109ae-160">`[IPPool <String>]`: IP-Pool-Name.</span><span class="sxs-lookup"><span data-stu-id="109ae-160">`[IPPool <String>]`: IP pool name.</span></span>
  - <span data-ttu-id="109ae-161">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="109ae-161">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="109ae-162">`[InfraRole <String>]`: Name der Infrastruktur Rolle</span><span class="sxs-lookup"><span data-stu-id="109ae-162">`[InfraRole <String>]`: Infrastructure role name.</span></span>
  - <span data-ttu-id="109ae-163">`[InfraRoleInstance <String>]`: Name einer Infrastrukturrollen Instanz.</span><span class="sxs-lookup"><span data-stu-id="109ae-163">`[InfraRoleInstance <String>]`: Name of an infrastructure role instance.</span></span>
  - <span data-ttu-id="109ae-164">`[Location <String>]`: Speicherort der Ressource.</span><span class="sxs-lookup"><span data-stu-id="109ae-164">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="109ae-165">`[LogicalNetwork <String>]`: Name des logischen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="109ae-165">`[LogicalNetwork <String>]`: Name of the logical network.</span></span>
  - <span data-ttu-id="109ae-166">`[LogicalSubnet <String>]`: Name des logischen Subnetzes.</span><span class="sxs-lookup"><span data-stu-id="109ae-166">`[LogicalSubnet <String>]`: Name of the logical subnet.</span></span>
  - <span data-ttu-id="109ae-167">`[MacAddressPool <String>]`: Name des Mac-Adresspools.</span><span class="sxs-lookup"><span data-stu-id="109ae-167">`[MacAddressPool <String>]`: Name of the MAC address pool.</span></span>
  - <span data-ttu-id="109ae-168">`[Operation <String>]`: Vorgangs-ID.</span><span class="sxs-lookup"><span data-stu-id="109ae-168">`[Operation <String>]`: Operation identifier.</span></span>
  - <span data-ttu-id="109ae-169">`[ResourceGroupName <String>]`: Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="109ae-169">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="109ae-170">`[ScaleUnit <String>]`: Name der Skaleneinheiten.</span><span class="sxs-lookup"><span data-stu-id="109ae-170">`[ScaleUnit <String>]`: Name of the scale units.</span></span>
  - <span data-ttu-id="109ae-171">`[ScaleUnitNode <String>]`: Name des Knotens der Skalierungseinheit.</span><span class="sxs-lookup"><span data-stu-id="109ae-171">`[ScaleUnitNode <String>]`: Name of the scale unit node.</span></span>
  - <span data-ttu-id="109ae-172">`[SlbMuxInstance <String>]`: Name einer SLB-MUX-Instanz.</span><span class="sxs-lookup"><span data-stu-id="109ae-172">`[SlbMuxInstance <String>]`: Name of a SLB MUX instance.</span></span>
  - <span data-ttu-id="109ae-173">`[StoragePool <String>]`: Name des Speicherpools.</span><span class="sxs-lookup"><span data-stu-id="109ae-173">`[StoragePool <String>]`: Storage pool name.</span></span>
  - <span data-ttu-id="109ae-174">`[StorageSubSystem <String>]`: Name des Speichersystems.</span><span class="sxs-lookup"><span data-stu-id="109ae-174">`[StorageSubSystem <String>]`: Name of the storage system.</span></span>
  - <span data-ttu-id="109ae-175">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="109ae-175">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="109ae-176">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="109ae-176">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="109ae-177">`[Volume <String>]`: Name des Speicher Datenträgers.</span><span class="sxs-lookup"><span data-stu-id="109ae-177">`[Volume <String>]`: Name of the storage volume.</span></span>

## <span data-ttu-id="109ae-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="109ae-178">RELATED LINKS</span></span>
