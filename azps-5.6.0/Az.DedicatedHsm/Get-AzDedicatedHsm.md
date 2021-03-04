---
external help file: ''
Module Name: Az.DedicatedHsm
online version: https://docs.microsoft.com/powershell/module/az.dedicatedhsm/get-azdedicatedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DedicatedHsm/help/Get-AzDedicatedHsm.md
ms.openlocfilehash: b4e00745655be6eb050141bb04dcef4797bde256
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101925819"
---
# <span data-ttu-id="b9c7f-101">Get-AzDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b9c7f-101">Get-AzDedicatedHsm</span></span>

## <span data-ttu-id="b9c7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9c7f-102">SYNOPSIS</span></span>
<span data-ttu-id="b9c7f-103">Ruft das angegebene dedizierte Azure-HSM ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-103">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b9c7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9c7f-104">SYNTAX</span></span>

### <span data-ttu-id="b9c7f-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9c7f-105">List1 (Default)</span></span>
```
Get-AzDedicatedHsm [-SubscriptionId <String[]>] [-Top <Int32>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9c7f-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b9c7f-106">Get</span></span>
```
Get-AzDedicatedHsm -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9c7f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b9c7f-107">GetViaIdentity</span></span>
```
Get-AzDedicatedHsm -InputObject <IDedicatedHsmIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b9c7f-108">Liste</span><span class="sxs-lookup"><span data-stu-id="b9c7f-108">List</span></span>
```
Get-AzDedicatedHsm -ResourceGroupName <String> [-SubscriptionId <String[]>] [-Top <Int32>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b9c7f-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9c7f-109">DESCRIPTION</span></span>
<span data-ttu-id="b9c7f-110">Ruft das angegebene dedizierte Azure-HSM ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-110">Gets the specified Azure dedicated HSM.</span></span>

## <span data-ttu-id="b9c7f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9c7f-111">EXAMPLES</span></span>

### <span data-ttu-id="b9c7f-112">Beispiel 1: Alle dedizierten HSM unter einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="b9c7f-112">Example 1: Get all Dedicated HSM under a subscription</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
yeminghsm  Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b9c7f-113">Dieser Befehl ruft alle dedizierten HSM unter einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-113">This command gets all Dedicated HSM under a subscription</span></span>

### <span data-ttu-id="b9c7f-114">Beispiel 2: Alle dedizierten HSM unter einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-114">Example 2: Get all Dedicated HSM under a resource group.</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b9c7f-115">Dieser Befehl ruft alle dedizierten HSM unter einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-115">This command gets all Dedicated HSM under a resource group.</span></span>

### <span data-ttu-id="b9c7f-116">Beispiel 3: Erhalten eines dedizierten HSM nach Name</span><span class="sxs-lookup"><span data-stu-id="b9c7f-116">Example 3: Get a Dedicated HSM by name</span></span>
```powershell
PS C:\> Get-AzDedicatedHsm -Name hsm-7t2xaf -ResourceGroupName dedicatedhsm-rg-n359cz

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-7t2xaf Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b9c7f-117">Dieser Befehl ruft einen dedizierten HSM nach Namen ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-117">This command gets a Dedicated HSM by name.</span></span>

### <span data-ttu-id="b9c7f-118">Beispiel 4: Erhalten eines dedizierten HSM nach -Objekt</span><span class="sxs-lookup"><span data-stu-id="b9c7f-118">Example 4: Get a Dedicated HSM by object</span></span>
```powershell
PS C:\> $hsm = New-AzDedicatedHsm -Name  hsm-n7wfxi -ResourceGroupName dedicatedhsm-rg-n359cz -Location eastus -Sku "SafeNet Luna Network HSM A790" -StampId stamp1 -SubnetId "/subscriptions/xxxx-xxxx-xxx-xxx/resourceGroups/dedicatedhsm-rg-n359cz/providers/Microsoft.Network/virtualNetworks/vnetq30la9/subnets/hsmsubnet" -NetworkInterface @{PrivateIPAddress = '10.2.1.120' }
PS C:\> Get-AzDedicatedHsm -InputObject $hsm

Name       Provisioning State SKU                           Location
----       ------------------ ---                           --------
hsm-n7wfxi Succeeded          SafeNet Luna Network HSM A790 eastus
```

<span data-ttu-id="b9c7f-119">Dieser Befehl ruft ein Dediziertes HSM nach -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-119">This command gets a Dedicated HSM by object.</span></span>

## <span data-ttu-id="b9c7f-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9c7f-120">PARAMETERS</span></span>

### <span data-ttu-id="b9c7f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9c7f-121">-DefaultProfile</span></span>
<span data-ttu-id="b9c7f-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9c7f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b9c7f-123">-InputObject</span></span>
<span data-ttu-id="b9c7f-124">Identitätsparameter Zum Erstellen lesen Sie den Abschnitt NOTIZEN für INPUTOBJECT-Eigenschaften, und erstellen Sie eine Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b9c7f-125">-Name</span><span class="sxs-lookup"><span data-stu-id="b9c7f-125">-Name</span></span>
<span data-ttu-id="b9c7f-126">Der Name des dedizierten HSM.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-126">The name of the dedicated HSM.</span></span>

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

### <span data-ttu-id="b9c7f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9c7f-127">-ResourceGroupName</span></span>
<span data-ttu-id="b9c7f-128">Der Name der Ressourcengruppe, zu der der dedizierte hsm gehört.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-128">The name of the Resource Group to which the dedicated hsm belongs.</span></span>

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

### <span data-ttu-id="b9c7f-129">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b9c7f-129">-SubscriptionId</span></span>
<span data-ttu-id="b9c7f-130">Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-130">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="b9c7f-131">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-131">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b9c7f-132">-Top</span><span class="sxs-lookup"><span data-stu-id="b9c7f-132">-Top</span></span>
<span data-ttu-id="b9c7f-133">Maximale Anzahl von Ergebnissen, die zurücksennen.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-133">Maximum number of results to return.</span></span>

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

### <span data-ttu-id="b9c7f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9c7f-134">CommonParameters</span></span>
<span data-ttu-id="b9c7f-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9c7f-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9c7f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9c7f-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9c7f-137">INPUTS</span></span>

### <span data-ttu-id="b9c7f-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span><span class="sxs-lookup"><span data-stu-id="b9c7f-138">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.IDedicatedHsmIdentity</span></span>

## <span data-ttu-id="b9c7f-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9c7f-139">OUTPUTS</span></span>

### <span data-ttu-id="b9c7f-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span><span class="sxs-lookup"><span data-stu-id="b9c7f-140">Microsoft.Azure.PowerShell.Cmdlets.DedicatedHsm.Models.Api20181031.IDedicatedHsm</span></span>

## <span data-ttu-id="b9c7f-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9c7f-141">NOTES</span></span>

<span data-ttu-id="b9c7f-142">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b9c7f-142">ALIASES</span></span>

<span data-ttu-id="b9c7f-143">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="b9c7f-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b9c7f-144">Um die unten beschriebenen Parameter zu erstellen, erstellen Sie eine Hashtabelle, die die entsprechenden Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b9c7f-145">Informationen zu Hashtabellen finden Sie unter Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b9c7f-146">INPUTOBJECT <IDedicatedHsmIdentity> : Identitätsparameter</span><span class="sxs-lookup"><span data-stu-id="b9c7f-146">INPUTOBJECT <IDedicatedHsmIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b9c7f-147">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="b9c7f-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b9c7f-148">`[Name <String>]`: Name des dedizierten Hsm</span><span class="sxs-lookup"><span data-stu-id="b9c7f-148">`[Name <String>]`: Name of the dedicated Hsm</span></span>
  - <span data-ttu-id="b9c7f-149">`[ResourceGroupName <String>]`: Der Name der Ressourcengruppe, zu der die Ressource gehört.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-149">`[ResourceGroupName <String>]`: The name of the Resource Group to which the resource belongs.</span></span>
  - <span data-ttu-id="b9c7f-150">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="b9c7f-151">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="b9c7f-151">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="b9c7f-152">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9c7f-152">RELATED LINKS</span></span>

