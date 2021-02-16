---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167753"
---
# <span data-ttu-id="9393d-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="9393d-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="9393d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9393d-102">SYNOPSIS</span></span>
<span data-ttu-id="9393d-103">Erstellen oder aktualisieren Sie einen dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9393d-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="9393d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9393d-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9393d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9393d-105">DESCRIPTION</span></span>
<span data-ttu-id="9393d-106">Erstellen oder aktualisieren Sie einen dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9393d-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="9393d-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9393d-107">EXAMPLES</span></span>

### <span data-ttu-id="9393d-108">Beispiel 1: Erstellen eines dedizierten HSM in einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="9393d-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="9393d-109">Mit diesem Befehl wird ein dediziertes HSM in einem vorhandenen virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="9393d-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="9393d-110">**HINWEIS:** Zurzeit `New-AzDedicatedHsm` gibt es eine Einschränkung, die zurückgegeben wird, bevor das HSM in Azure vollständig bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="9393d-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="9393d-111">Fragen Sie daher nach dem Erstellen eines neuen HSM dessen Zustand ab, und stellen Sie sicher, dass er `Get-AzDedicatedHsm` `Provisioning State` verwendet `Succeeded` wird, bevor Sie ihn verwenden.</span><span class="sxs-lookup"><span data-stu-id="9393d-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="9393d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9393d-112">PARAMETERS</span></span>

### <span data-ttu-id="9393d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9393d-113">-AsJob</span></span>
<span data-ttu-id="9393d-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="9393d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="9393d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9393d-115">-DefaultProfile</span></span>
<span data-ttu-id="9393d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9393d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9393d-117">-Location</span><span class="sxs-lookup"><span data-stu-id="9393d-117">-Location</span></span>
<span data-ttu-id="9393d-118">Der unterstützte Azure-Speicherort, an dem der dedizierte HSM erstellt werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9393d-118">The supported Azure location where the dedicated HSM should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9393d-119">-Name</span></span>
<span data-ttu-id="9393d-120">Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="9393d-120">Name of the dedicated Hsm</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="9393d-121">-NetworkInterface</span></span>
<span data-ttu-id="9393d-122">Gibt die Liste der Ressourcen-IDs für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9393d-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="9393d-123">Informationen zum Erstellen finden Sie im Abschnitt "NOTES" zu #A0 und zum Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="9393d-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.INetworkInterface[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9393d-124">-NoWait</span></span>
<span data-ttu-id="9393d-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="9393d-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9393d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9393d-126">-ResourceGroupName</span></span>
<span data-ttu-id="9393d-127">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="9393d-127">The name of the Resource Group to which the resource belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="9393d-128">-Sku</span></span>
<span data-ttu-id="9393d-129">SKU des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="9393d-129">SKU of the dedicated HSM</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="9393d-130">-StampId</span></span>
<span data-ttu-id="9393d-131">Dieses Feld wird verwendet, wenn RP keine Verfügbarkeitszonen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9393d-131">This field will be used when RP does not support Availability zones.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="9393d-132">-SubnetId</span></span>
<span data-ttu-id="9393d-133">Die ARM in Form von /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="9393d-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9393d-134">-SubscriptionId</span></span>
<span data-ttu-id="9393d-135">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="9393d-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="9393d-136">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="9393d-136">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="9393d-137">-Tag</span></span>
<span data-ttu-id="9393d-138">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="9393d-138">Resource tags</span></span>

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

### <span data-ttu-id="9393d-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="9393d-139">-Zone</span></span>
<span data-ttu-id="9393d-140">Die Dedizierten Hsm-Zonen.</span><span class="sxs-lookup"><span data-stu-id="9393d-140">The Dedicated Hsm zones.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9393d-141">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9393d-141">-Confirm</span></span>
<span data-ttu-id="9393d-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9393d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9393d-143">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9393d-143">-WhatIf</span></span>
<span data-ttu-id="9393d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9393d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9393d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9393d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9393d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9393d-146">CommonParameters</span></span>
<span data-ttu-id="9393d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9393d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9393d-148">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9393d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9393d-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9393d-149">INPUTS</span></span>

## <span data-ttu-id="9393d-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9393d-150">OUTPUTS</span></span>

### <span data-ttu-id="9393d-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="9393d-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="9393d-152">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9393d-152">NOTES</span></span>

<span data-ttu-id="9393d-153">ALIASE</span><span class="sxs-lookup"><span data-stu-id="9393d-153">ALIASES</span></span>

<span data-ttu-id="9393d-154">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="9393d-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9393d-155">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="9393d-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9393d-156">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9393d-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9393d-157">NETWORKINTERFACE <INetworkInterface[]>: Gibt die Liste der Ressourcen-IDs für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="9393d-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="9393d-158">`[PrivateIPAddress <String>]`: Private IP-Adresse der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9393d-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="9393d-159">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9393d-159">RELATED LINKS</span></span>

