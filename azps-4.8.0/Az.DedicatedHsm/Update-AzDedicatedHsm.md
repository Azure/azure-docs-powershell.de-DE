---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/update-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Update-AzDedicatedHsm.md
ms.openlocfilehash: 5aa286eeedb08e6f582210d98a1d29bcd0074031
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94008541"
---
# <span data-ttu-id="75d65-101">Update-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="75d65-101">Update-AzDedicatedHsm</span></span>

## <span data-ttu-id="75d65-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75d65-102">SYNOPSIS</span></span>
<span data-ttu-id="75d65-103">Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75d65-103">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="75d65-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75d65-104">SYNTAX</span></span>

### <span data-ttu-id="75d65-105">UpdateExpanded (Standard)</span><span class="sxs-lookup"><span data-stu-id="75d65-105">UpdateExpanded (Default)</span></span>
```
Update-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="75d65-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="75d65-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-Tag <Hashtable>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="75d65-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75d65-107">DESCRIPTION</span></span>
<span data-ttu-id="75d65-108">Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75d65-108">Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="75d65-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75d65-109">EXAMPLES</span></span>

### <span data-ttu-id="75d65-110">Beispiel 1: Aktualisieren des Parameter Tags des dedizierten HSM nach Name</span><span class="sxs-lookup"><span data-stu-id="75d65-110">Example 1: Update the parameter tag of the Dedicated HSM by name</span></span>
```powershell
PS C:\> Update-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="75d65-111">Dieser Befehl aktualisiert das Parameter-Tag des dedizierten HSM nach Namen.</span><span class="sxs-lookup"><span data-stu-id="75d65-111">This command updates the parameter tag of the Dedicated HSM by name</span></span>

### <span data-ttu-id="75d65-112">Beispiel 2: Aktualisieren des Parameter Tags des dedizierten HSM nach Objekt</span><span class="sxs-lookup"><span data-stu-id="75d65-112">Example 2: Update the parameter tag of the Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = Get-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz 
PS C:\> Update-AzDedicatedHsm -InputObject -Tag @{'key1' = '1'; 'key2' = 2; 'key3' = 3}

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="75d65-113">Dieser Befehl aktualisiert das Parameter-Tag des dedizierten HSM nach Objekt.</span><span class="sxs-lookup"><span data-stu-id="75d65-113">This command updates the parameter tag of the Dedicated HSM by object</span></span>

## <span data-ttu-id="75d65-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="75d65-114">PARAMETERS</span></span>

### <span data-ttu-id="75d65-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="75d65-115">-AsJob</span></span>
<span data-ttu-id="75d65-116">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="75d65-116">Run the command as a job</span></span>

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

### <span data-ttu-id="75d65-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75d65-117">-DefaultProfile</span></span>
<span data-ttu-id="75d65-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75d65-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="75d65-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="75d65-119">-InputObject</span></span>
<span data-ttu-id="75d65-120">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="75d65-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="75d65-121">-Name</span><span class="sxs-lookup"><span data-stu-id="75d65-121">-Name</span></span>
<span data-ttu-id="75d65-122">Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="75d65-122">Name of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d65-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="75d65-123">-NoWait</span></span>
<span data-ttu-id="75d65-124">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="75d65-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="75d65-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75d65-125">-ResourceGroupName</span></span>
<span data-ttu-id="75d65-126">Der Name der Ressourcengruppe, zu der der Server gehört.</span><span class="sxs-lookup"><span data-stu-id="75d65-126">The name of the Resource Group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d65-127">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="75d65-127">-SubscriptionId</span></span>
<span data-ttu-id="75d65-128">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="75d65-128">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="75d65-129">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="75d65-129">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d65-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="75d65-130">-Tag</span></span>
<span data-ttu-id="75d65-131">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="75d65-131">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="75d65-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75d65-132">-Confirm</span></span>
<span data-ttu-id="75d65-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75d65-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75d65-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75d65-134">-WhatIf</span></span>
<span data-ttu-id="75d65-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75d65-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75d65-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75d65-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75d65-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75d65-137">CommonParameters</span></span>
<span data-ttu-id="75d65-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75d65-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75d65-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="75d65-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75d65-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75d65-140">INPUTS</span></span>

### <span data-ttu-id="75d65-141">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="75d65-141">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="75d65-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75d65-142">OUTPUTS</span></span>

### <span data-ttu-id="75d65-143">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="75d65-143">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="75d65-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="75d65-144">NOTES</span></span>

<span data-ttu-id="75d65-145">Aliase</span><span class="sxs-lookup"><span data-stu-id="75d65-145">ALIASES</span></span>

<span data-ttu-id="75d65-146">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="75d65-146">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="75d65-147">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="75d65-147">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="75d65-148">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="75d65-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="75d65-149">Inputobject <IDedicatedHsmIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="75d65-149">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="75d65-150">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="75d65-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="75d65-151">`[Name <String>]`: Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="75d65-151">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="75d65-152">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="75d65-152">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="75d65-153">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="75d65-153">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="75d65-154">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="75d65-154">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="75d65-155">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75d65-155">RELATED LINKS</span></span>

