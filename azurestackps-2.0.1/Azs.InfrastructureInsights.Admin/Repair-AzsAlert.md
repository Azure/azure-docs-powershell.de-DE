---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2020
ms.locfileid: "94005427"
---
# <span data-ttu-id="c2bba-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="c2bba-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="c2bba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2bba-102">SYNOPSIS</span></span>
<span data-ttu-id="c2bba-103">Repariert eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c2bba-103">Repairs an alert.</span></span>

## <span data-ttu-id="c2bba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2bba-104">SYNTAX</span></span>

### <span data-ttu-id="c2bba-105">Reparieren (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2bba-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c2bba-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c2bba-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c2bba-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2bba-107">DESCRIPTION</span></span>
<span data-ttu-id="c2bba-108">Repariert eine Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c2bba-108">Repairs an alert.</span></span>

## <span data-ttu-id="c2bba-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2bba-109">EXAMPLES</span></span>

### <span data-ttu-id="c2bba-110">Beispiel 1:</span><span class="sxs-lookup"><span data-stu-id="c2bba-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="c2bba-111">Repariert eine Benachrichtigung nach Namen.</span><span class="sxs-lookup"><span data-stu-id="c2bba-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="c2bba-112">Beispiel 2:</span><span class="sxs-lookup"><span data-stu-id="c2bba-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="c2bba-113">Repariert eine Warnung durch Rohrleitungen.</span><span class="sxs-lookup"><span data-stu-id="c2bba-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="c2bba-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2bba-114">PARAMETERS</span></span>

### <span data-ttu-id="c2bba-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c2bba-115">-AsJob</span></span>
<span data-ttu-id="c2bba-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="c2bba-116">Run the command as a job</span></span>

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

### <span data-ttu-id="c2bba-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2bba-117">-DefaultProfile</span></span>
<span data-ttu-id="c2bba-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2bba-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2bba-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2bba-119">-InputObject</span></span>
<span data-ttu-id="c2bba-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="c2bba-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="c2bba-121">-Standort</span><span class="sxs-lookup"><span data-stu-id="c2bba-121">-Location</span></span>
<span data-ttu-id="c2bba-122">Name der Region</span><span class="sxs-lookup"><span data-stu-id="c2bba-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2bba-123">-Name</span><span class="sxs-lookup"><span data-stu-id="c2bba-123">-Name</span></span>
<span data-ttu-id="c2bba-124">Der Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c2bba-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2bba-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c2bba-125">-NoWait</span></span>
<span data-ttu-id="c2bba-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="c2bba-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c2bba-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2bba-127">-PassThru</span></span>
<span data-ttu-id="c2bba-128">Gibt "true" zurück, wenn der Befehl erfolgreich ist</span><span class="sxs-lookup"><span data-stu-id="c2bba-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c2bba-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2bba-129">-ResourceGroupName</span></span>
<span data-ttu-id="c2bba-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2bba-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2bba-131">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="c2bba-131">-SubscriptionId</span></span>
<span data-ttu-id="c2bba-132">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c2bba-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c2bba-133">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c2bba-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c2bba-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2bba-134">-Confirm</span></span>
<span data-ttu-id="c2bba-135">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2bba-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2bba-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2bba-136">-WhatIf</span></span>
<span data-ttu-id="c2bba-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2bba-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2bba-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2bba-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2bba-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2bba-139">CommonParameters</span></span>
<span data-ttu-id="c2bba-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2bba-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2bba-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2bba-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2bba-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2bba-142">INPUTS</span></span>

### <span data-ttu-id="c2bba-143">Microsoft. Azure. PowerShell. Cmdlets. InfrastructureInsightsAdmin. Models. IInfrastructureInsightsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c2bba-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="c2bba-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2bba-144">OUTPUTS</span></span>

### <span data-ttu-id="c2bba-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c2bba-145">System.Boolean</span></span>



## <span data-ttu-id="c2bba-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2bba-146">NOTES</span></span>

<span data-ttu-id="c2bba-147">Komplexe Parametereigenschaften Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c2bba-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c2bba-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="c2bba-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c2bba-149">Inputobject <IInfrastructureInsightsAdminIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="c2bba-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c2bba-150">`[AlertName <String>]`: Name der Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c2bba-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="c2bba-151">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="c2bba-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c2bba-152">`[Location <String>]`: Name der Region</span><span class="sxs-lookup"><span data-stu-id="c2bba-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="c2bba-153">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2bba-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="c2bba-154">`[ResourceRegistrationId <String>]`: Ressourcen Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="c2bba-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="c2bba-155">`[ServiceHealth <String>]`: Name des Dienststatus.</span><span class="sxs-lookup"><span data-stu-id="c2bba-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="c2bba-156">`[ServiceRegistrationId <String>]`: Dienst Registrierungs-ID.</span><span class="sxs-lookup"><span data-stu-id="c2bba-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="c2bba-157">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c2bba-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="c2bba-158">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="c2bba-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="c2bba-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2bba-159">RELATED LINKS</span></span>

