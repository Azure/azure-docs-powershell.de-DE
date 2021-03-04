---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: 9d2d1ee1dd17b9d1783ba267b2f656be6adce05b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925803"
---
# <span data-ttu-id="e0ccb-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ccb-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="e0ccb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0ccb-102">SYNOPSIS</span></span>
<span data-ttu-id="e0ccb-103">Erstellen oder Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="e0ccb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e0ccb-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="e0ccb-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e0ccb-105">DESCRIPTION</span></span>
<span data-ttu-id="e0ccb-106">Erstellen oder Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="e0ccb-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e0ccb-107">EXAMPLES</span></span>

### <span data-ttu-id="e0ccb-108">Beispiel 1: Erstellen eines dedizierten HSM in einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="e0ccb-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="e0ccb-109">Mit diesem Befehl wird ein dediziertes HSM in einem vorhandenen virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="e0ccb-110">**HINWEIS:** Derzeit `New-AzDedicatedHsm` gibt es eine Einschränkung, die zurückgegeben wird, bevor das HSM vollständig in Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="e0ccb-111">Fragen Sie daher nach dem Erstellen eines neuen HSM den Zustand nach ab, und stellen Sie sicher, dass er `Get-AzDedicatedHsm` `Provisioning State` vor der Verwendung `Succeeded` ist.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="e0ccb-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e0ccb-112">PARAMETERS</span></span>

### <span data-ttu-id="e0ccb-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e0ccb-113">-AsJob</span></span>
<span data-ttu-id="e0ccb-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="e0ccb-114">Run the command as a job</span></span>

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

### <span data-ttu-id="e0ccb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0ccb-115">-DefaultProfile</span></span>
<span data-ttu-id="e0ccb-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0ccb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="e0ccb-117">-Location</span></span>
<span data-ttu-id="e0ccb-118">Der unterstützte Azure-Speicherort, an dem das dedizierte HSM erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="e0ccb-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e0ccb-119">-Name</span></span>
<span data-ttu-id="e0ccb-120">Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="e0ccb-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="e0ccb-121">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="e0ccb-121">-NetworkInterface</span></span>
<span data-ttu-id="e0ccb-122">Gibt die Liste der Ressourcen-ID für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="e0ccb-123">Informationen zum Erstellen finden Sie im Abschnitt NOTIZEN zu DEN NETZWERKINTERFACE-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="e0ccb-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="e0ccb-124">-NoWait</span></span>
<span data-ttu-id="e0ccb-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="e0ccb-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e0ccb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0ccb-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0ccb-127">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="e0ccb-128">-Sku</span><span class="sxs-lookup"><span data-stu-id="e0ccb-128">-Sku</span></span>
<span data-ttu-id="e0ccb-129">SKU des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="e0ccb-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="e0ccb-130">-StampId</span><span class="sxs-lookup"><span data-stu-id="e0ccb-130">-StampId</span></span>
<span data-ttu-id="e0ccb-131">Dieses Feld wird verwendet, wenn RP Verfügbarkeitszonen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="e0ccb-132">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="e0ccb-132">-SubnetId</span></span>
<span data-ttu-id="e0ccb-133">Die ARM-Ressourcen-ID in Form von /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="e0ccb-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="e0ccb-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e0ccb-134">-SubscriptionId</span></span>
<span data-ttu-id="e0ccb-135">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e0ccb-136">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="e0ccb-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="e0ccb-137">-Tag</span></span>
<span data-ttu-id="e0ccb-138">Ressourcentags</span><span class="sxs-lookup"><span data-stu-id="e0ccb-138">Resource tags</span></span>

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

### <span data-ttu-id="e0ccb-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="e0ccb-139">-Zone</span></span>
<span data-ttu-id="e0ccb-140">Die Dedizierten Hsm-Zonen.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="e0ccb-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e0ccb-141">-Confirm</span></span>
<span data-ttu-id="e0ccb-142">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0ccb-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0ccb-143">-WhatIf</span></span>
<span data-ttu-id="e0ccb-144">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0ccb-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0ccb-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0ccb-146">CommonParameters</span></span>
<span data-ttu-id="e0ccb-147">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0ccb-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e0ccb-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0ccb-149">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e0ccb-149">INPUTS</span></span>

## <span data-ttu-id="e0ccb-150">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e0ccb-150">OUTPUTS</span></span>

### <span data-ttu-id="e0ccb-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="e0ccb-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="e0ccb-152">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e0ccb-152">NOTES</span></span>

<span data-ttu-id="e0ccb-153">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e0ccb-153">ALIASES</span></span>

<span data-ttu-id="e0ccb-154">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="e0ccb-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="e0ccb-155">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e0ccb-156">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="e0ccb-157">NETWORKINTERFACE <INetworkInterface[]>: Gibt die Liste der Ressourcen-IDs für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e0ccb-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="e0ccb-158">`[PrivateIPAddress <String>]`: Private IP-Adresse der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="e0ccb-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="e0ccb-159">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e0ccb-159">RELATED LINKS</span></span>

