---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/new-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/New-AzDedicatedHsm.md
ms.openlocfilehash: ff1fc53d7fec9a56564bbf536469ea9f745f9265
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297286"
---
# <span data-ttu-id="aa61d-101">New-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aa61d-101">New-AzDedicatedHsm</span></span>

## <span data-ttu-id="aa61d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="aa61d-102">SYNOPSIS</span></span>
<span data-ttu-id="aa61d-103">Erstellen oder Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa61d-103">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="aa61d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa61d-104">SYNTAX</span></span>

```
New-AzDedicatedHsm -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-NetworkInterface <INetworkInterface[]>] [-Sku <String>] [-StampId <String>] [-SubnetId <String>]
 [-Tag <Hashtable>] [-Zone <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="aa61d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa61d-105">DESCRIPTION</span></span>
<span data-ttu-id="aa61d-106">Erstellen oder Aktualisieren eines dedizierten HSM im angegebenen Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa61d-106">Create or Update a dedicated HSM in the specified subscription.</span></span>

## <span data-ttu-id="aa61d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="aa61d-107">EXAMPLES</span></span>

### <span data-ttu-id="aa61d-108">Beispiel 1: Erstellen eines dedizierten HSM in einem vorhandenen virtuellen Netzwerk</span><span class="sxs-lookup"><span data-stu-id="aa61d-108">Example 1: Create a Dedicated HSM into an existing virtual network</span></span>
```powershell
PS C:\> New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="aa61d-109">Mit diesem Befehl wird ein dediziertes HSM in einem vorhandenen virtuellen Netzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="aa61d-109">This command creates a Dedicated HSM into an existing virtual network.</span></span>

<span data-ttu-id="aa61d-110">**Hinweis:** Derzeit `New-AzDedicatedHsm` gibt es eine Einschränkung, die zurückgegeben wird, bevor das HSM vollständig auf Azure bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa61d-110">**NOTE:** Currently `New-AzDedicatedHsm` has a limitation that it returns before the HSM is fully provisioned on Azure.</span></span>
<span data-ttu-id="aa61d-111">Stellen Sie daher nach dem Erstellen eines neuen HSM bitte seinen Zustand nach `Get-AzDedicatedHsm` und stellen Sie sicher, dass `Provisioning State` `Succeeded` es sich vor der Verwendung befindet.</span><span class="sxs-lookup"><span data-stu-id="aa61d-111">Therefore after creating a new HSM, please query its state by `Get-AzDedicatedHsm` and make sure its `Provisioning State` is `Succeeded` before using it.</span></span>

## <span data-ttu-id="aa61d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa61d-112">PARAMETERS</span></span>

### <span data-ttu-id="aa61d-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa61d-113">-AsJob</span></span>
<span data-ttu-id="aa61d-114">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="aa61d-114">Run the command as a job</span></span>

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

### <span data-ttu-id="aa61d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa61d-115">-DefaultProfile</span></span>
<span data-ttu-id="aa61d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="aa61d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa61d-117">-Standort</span><span class="sxs-lookup"><span data-stu-id="aa61d-117">-Location</span></span>
<span data-ttu-id="aa61d-118">Der unterstützte Azure-Speicherort, an dem das dedizierte HSM erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="aa61d-118">The supported Azure location where the dedicated HSM should be created.</span></span>

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

### <span data-ttu-id="aa61d-119">-Name</span><span class="sxs-lookup"><span data-stu-id="aa61d-119">-Name</span></span>
<span data-ttu-id="aa61d-120">Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="aa61d-120">Name of the dedicated Hsm</span></span>

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

### <span data-ttu-id="aa61d-121">-Network Interface</span><span class="sxs-lookup"><span data-stu-id="aa61d-121">-NetworkInterface</span></span>
<span data-ttu-id="aa61d-122">Gibt die Liste der Ressourcen-IDs für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aa61d-122">Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
<span data-ttu-id="aa61d-123">Informationen zum Erstellen finden Sie unter Abschnitt "Notizen" für Network Interface-Eigenschaften und Erstellen einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="aa61d-123">To construct, see NOTES section for NETWORKINTERFACE properties and create a hash table.</span></span>

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

### <span data-ttu-id="aa61d-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="aa61d-124">-NoWait</span></span>
<span data-ttu-id="aa61d-125">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="aa61d-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="aa61d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa61d-126">-ResourceGroupName</span></span>
<span data-ttu-id="aa61d-127">Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="aa61d-127">The name of the Resource Group to which the resource belongs.</span></span>

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

### <span data-ttu-id="aa61d-128">-SKU</span><span class="sxs-lookup"><span data-stu-id="aa61d-128">-Sku</span></span>
<span data-ttu-id="aa61d-129">SKU des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="aa61d-129">SKU of the dedicated HSM</span></span>

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

### <span data-ttu-id="aa61d-130">-Stamp-Nr</span><span class="sxs-lookup"><span data-stu-id="aa61d-130">-StampId</span></span>
<span data-ttu-id="aa61d-131">Dieses Feld wird verwendet, wenn RP keine Verfügbarkeits Zonen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aa61d-131">This field will be used when RP does not support Availability zones.</span></span>

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

### <span data-ttu-id="aa61d-132">-Subnet-Nr</span><span class="sxs-lookup"><span data-stu-id="aa61d-132">-SubnetId</span></span>
<span data-ttu-id="aa61d-133">Die Arm-Ressourcen-ID in Form von/Subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span><span class="sxs-lookup"><span data-stu-id="aa61d-133">The ARM resource id in the form of /subscriptions/{SubscriptionId}/resourceGroups/{ResourceGroupName}/...</span></span>

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

### <span data-ttu-id="aa61d-134">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="aa61d-134">-SubscriptionId</span></span>
<span data-ttu-id="aa61d-135">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="aa61d-135">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="aa61d-136">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="aa61d-136">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="aa61d-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="aa61d-137">-Tag</span></span>
<span data-ttu-id="aa61d-138">Ressourcenkategorien</span><span class="sxs-lookup"><span data-stu-id="aa61d-138">Resource tags</span></span>

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

### <span data-ttu-id="aa61d-139">-Zone</span><span class="sxs-lookup"><span data-stu-id="aa61d-139">-Zone</span></span>
<span data-ttu-id="aa61d-140">Die dedizierten HSM-Zonen.</span><span class="sxs-lookup"><span data-stu-id="aa61d-140">The Dedicated Hsm zones.</span></span>

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

### <span data-ttu-id="aa61d-141">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="aa61d-141">-Confirm</span></span>
<span data-ttu-id="aa61d-142">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="aa61d-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa61d-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa61d-143">-WhatIf</span></span>
<span data-ttu-id="aa61d-144">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="aa61d-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa61d-145">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aa61d-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa61d-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa61d-146">CommonParameters</span></span>
<span data-ttu-id="aa61d-147">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa61d-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa61d-148">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aa61d-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa61d-149">Eingaben</span><span class="sxs-lookup"><span data-stu-id="aa61d-149">INPUTS</span></span>

## <span data-ttu-id="aa61d-150">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="aa61d-150">OUTPUTS</span></span>

### <span data-ttu-id="aa61d-151">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="aa61d-151">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="aa61d-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="aa61d-152">NOTES</span></span>

<span data-ttu-id="aa61d-153">Aliase</span><span class="sxs-lookup"><span data-stu-id="aa61d-153">ALIASES</span></span>

<span data-ttu-id="aa61d-154">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="aa61d-154">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="aa61d-155">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="aa61d-155">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aa61d-156">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="aa61d-156">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="aa61d-157">Network Interface <INetworkInterface [] >: gibt die Liste der Ressourcen-IDs für die Netzwerkschnittstellen an, die dem dedizierten HSM zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="aa61d-157">NETWORKINTERFACE <INetworkInterface[]>: Specifies the list of resource Ids for the network interfaces associated with the dedicated HSM.</span></span>
  - <span data-ttu-id="aa61d-158">`[PrivateIPAddress <String>]`: Private IP-Adresse der Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="aa61d-158">`[PrivateIPAddress <String>]`: Private Ip address of the interface</span></span>

## <span data-ttu-id="aa61d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="aa61d-159">RELATED LINKS</span></span>

