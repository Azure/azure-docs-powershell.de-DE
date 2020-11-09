---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/en-us/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: a8f6e3d6d7818a03f0e284b9c08a1ffdcd646710
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297285"
---
# <span data-ttu-id="ebf08-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ebf08-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="ebf08-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ebf08-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf08-103">Ruft das angegebene Azure dedizierte HSM ab.</span><span class="sxs-lookup"><span data-stu-id="ebf08-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="ebf08-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ebf08-104">SYNTAX</span></span>

### <span data-ttu-id="ebf08-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="ebf08-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="ebf08-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="ebf08-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ebf08-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="ebf08-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="ebf08-108">Liste</span><span class="sxs-lookup"><span data-stu-id="ebf08-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="ebf08-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ebf08-109">DESCRIPTION</span></span>
<span data-ttu-id="ebf08-110">Ruft das angegebene Azure dedizierte HSM ab.</span><span class="sxs-lookup"><span data-stu-id="ebf08-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="ebf08-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ebf08-111">EXAMPLES</span></span>

### <span data-ttu-id="ebf08-112">Beispiel 1: Abrufen aller dedizierten HSM unter einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="ebf08-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ebf08-113">Dieser Befehl ruft alle dedizierten HSM-Abonnements unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ebf08-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="ebf08-114">Beispiel 2: Abrufen aller dedizierten HSM unter einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ebf08-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ebf08-115">Dieser Befehl ruft alle dedizierten HSM unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ebf08-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="ebf08-116">Beispiel 3: Abrufen eines dedizierten HSM nach Namen</span><span class="sxs-lookup"><span data-stu-id="ebf08-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ebf08-117">Dieser Befehl ruft einen dedizierten HSM-Namen ab.</span><span class="sxs-lookup"><span data-stu-id="ebf08-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="ebf08-118">Beispiel 4: Abrufen eines dedizierten HSM nach Objekt</span><span class="sxs-lookup"><span data-stu-id="ebf08-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="ebf08-119">Mit diesem Befehl wird ein dediziertes HSM nach Objekt abgerufen.</span><span class="sxs-lookup"><span data-stu-id="ebf08-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="ebf08-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf08-120">PARAMETERS</span></span>

### <span data-ttu-id="ebf08-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf08-121">-DefaultProfile</span></span>
<span data-ttu-id="ebf08-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ebf08-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf08-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ebf08-123">-InputObject</span></span>
<span data-ttu-id="ebf08-124">Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="ebf08-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebf08-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ebf08-125">-Name</span></span>
<span data-ttu-id="ebf08-126">Der Name des dedizierten HSM.</span><span class="sxs-lookup"><span data-stu-id="ebf08-126">The name of the dedicated HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf08-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf08-127">-ResourceGroupName</span></span>
<span data-ttu-id="ebf08-128">Der Name der Ressourcengruppe, zu der das dedizierte HSM gehört.</span><span class="sxs-lookup"><span data-stu-id="ebf08-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf08-129">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="ebf08-129">-SubscriptionId</span></span>
<span data-ttu-id="ebf08-130">Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ebf08-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="ebf08-131">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebf08-131">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf08-132">-Top</span><span class="sxs-lookup"><span data-stu-id="ebf08-132">-Top</span></span>
<span data-ttu-id="ebf08-133">Die maximale Anzahl von Ergebnissen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ebf08-133">Maximum number of results to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, List1
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebf08-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf08-134">CommonParameters</span></span>
<span data-ttu-id="ebf08-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf08-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf08-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebf08-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf08-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ebf08-137">INPUTS</span></span>

### <span data-ttu-id="ebf08-138">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="ebf08-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="ebf08-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ebf08-139">OUTPUTS</span></span>

### <span data-ttu-id="ebf08-140">Microsoft. Azure. PowerShell. Cmdlets. DedicatedHsm. Models. Api20181031. IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="ebf08-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="ebf08-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ebf08-141">NOTES</span></span>

<span data-ttu-id="ebf08-142">Aliase</span><span class="sxs-lookup"><span data-stu-id="ebf08-142">ALIASES</span></span>

<span data-ttu-id="ebf08-143">komplexe Parameter Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="ebf08-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ebf08-144">Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="ebf08-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ebf08-145">Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.</span><span class="sxs-lookup"><span data-stu-id="ebf08-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ebf08-146">Inputobject <IDedicatedHsmIdentity> : Identity-Parameter</span><span class="sxs-lookup"><span data-stu-id="ebf08-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="ebf08-147">`[Id <String>]`: Ressourcen Identitäts Pfad</span><span class="sxs-lookup"><span data-stu-id="ebf08-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="ebf08-148">`[Name <String>]`: Name des dedizierten HSM</span><span class="sxs-lookup"><span data-stu-id="ebf08-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="ebf08-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="ebf08-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="ebf08-150">`[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="ebf08-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="ebf08-151">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="ebf08-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="ebf08-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ebf08-152">RELATED LINKS</span></span>

