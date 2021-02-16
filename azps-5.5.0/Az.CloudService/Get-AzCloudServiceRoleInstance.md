---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudserviceroleinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudServiceRoleInstance.md
ms.openlocfilehash: 55416adbd2ffbcb816e5652ad33e1777594fdcb6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149033"
---
# <span data-ttu-id="dcd41-101">Get-AzCloudServiceRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dcd41-101">Get-AzCloudServiceRoleInstance</span></span>

## <span data-ttu-id="dcd41-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcd41-102">SYNOPSIS</span></span>
<span data-ttu-id="dcd41-103">Ruft eine Rolleninstanz von einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="dcd41-103">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="dcd41-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcd41-104">SYNTAX</span></span>

### <span data-ttu-id="dcd41-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="dcd41-105">List (Default)</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dcd41-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="dcd41-106">Get</span></span>
```
Get-AzCloudServiceRoleInstance -CloudServiceName <String> -ResourceGroupName <String>
 -RoleInstanceName <String> [-SubscriptionId <String[]>] [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="dcd41-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="dcd41-107">GetViaIdentity</span></span>
```
Get-AzCloudServiceRoleInstance -InputObject <ICloudServiceIdentity> [-Expand <InstanceViewTypes>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="dcd41-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dcd41-108">DESCRIPTION</span></span>
<span data-ttu-id="dcd41-109">Ruft eine Rolleninstanz von einem Clouddienst ab.</span><span class="sxs-lookup"><span data-stu-id="dcd41-109">Gets a role instance from a cloud service.</span></span>

## <span data-ttu-id="dcd41-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dcd41-110">EXAMPLES</span></span>

### <span data-ttu-id="dcd41-111">Beispiel 1: Alle Rolleninstanzen erhalten</span><span class="sxs-lookup"><span data-stu-id="dcd41-111">Example 1: Get all role instances</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard
ContosoFrontEnd_IN_1    eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard
ContosoBackEnd_IN_1     eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="dcd41-112">Dieser Befehl ruft die Eigenschaften aller Rolleninstanzen des Clouddiensts "ContosoCS" ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="dcd41-112">This command gets the properties of all role instances of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

### <span data-ttu-id="dcd41-113">Beispiel 2: Erhalten von Eigenschaften für eine Rolleninstanz</span><span class="sxs-lookup"><span data-stu-id="dcd41-113">Example 2: Get properties for single role instance</span></span>
```powershell
PS C:\> Get-AzCloudServiceRoleInstance -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS" -RoleInstanceName "ContosoFrontEnd_IN_0"

Name                    Location    SkuName        SkuTier
----                    --------    -------        -------
ContosoFrontEnd_IN_0    eastus2euap Standard_D1_v2 Standard

```

<span data-ttu-id="dcd41-114">Dieser Befehl ruft die Eigenschaften der Rolleninstanz mit dem Namen ContosoFrontEnd_IN_0 des Clouddiensts "ContosoCS" ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="dcd41-114">This command gets the properties of the role instance named ContosoFrontEnd_IN_0 of cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="dcd41-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dcd41-115">PARAMETERS</span></span>

### <span data-ttu-id="dcd41-116">-CloudServiceName</span><span class="sxs-lookup"><span data-stu-id="dcd41-116">-CloudServiceName</span></span>
<span data-ttu-id="dcd41-117">.</span><span class="sxs-lookup"><span data-stu-id="dcd41-117">.</span></span>

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

### <span data-ttu-id="dcd41-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcd41-118">-DefaultProfile</span></span>
<span data-ttu-id="dcd41-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dcd41-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcd41-120">-Expand</span><span class="sxs-lookup"><span data-stu-id="dcd41-120">-Expand</span></span>
<span data-ttu-id="dcd41-121">Der Erweiterungsausdruck, der auf den Vorgang angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dcd41-121">The expand expression to apply to the operation.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Support.InstanceViewTypes
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd41-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dcd41-122">-InputObject</span></span>
<span data-ttu-id="dcd41-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="dcd41-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dcd41-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dcd41-124">-ResourceGroupName</span></span>
<span data-ttu-id="dcd41-125">.</span><span class="sxs-lookup"><span data-stu-id="dcd41-125">.</span></span>

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

### <span data-ttu-id="dcd41-126">-RoleInstanceName</span><span class="sxs-lookup"><span data-stu-id="dcd41-126">-RoleInstanceName</span></span>
<span data-ttu-id="dcd41-127">Der Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="dcd41-127">Name of the role instance.</span></span>

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

### <span data-ttu-id="dcd41-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="dcd41-128">-SubscriptionId</span></span>
<span data-ttu-id="dcd41-129">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dcd41-129">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="dcd41-130">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dcd41-130">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcd41-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcd41-131">CommonParameters</span></span>
<span data-ttu-id="dcd41-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcd41-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcd41-133">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dcd41-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcd41-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dcd41-134">INPUTS</span></span>

### <span data-ttu-id="dcd41-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="dcd41-135">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="dcd41-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dcd41-136">OUTPUTS</span></span>

### <span data-ttu-id="dcd41-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dcd41-137">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.IRoleInstance</span></span>

## <span data-ttu-id="dcd41-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="dcd41-138">NOTES</span></span>

<span data-ttu-id="dcd41-139">ALIASE</span><span class="sxs-lookup"><span data-stu-id="dcd41-139">ALIASES</span></span>

<span data-ttu-id="dcd41-140">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="dcd41-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dcd41-141">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="dcd41-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dcd41-142">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dcd41-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dcd41-143">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="dcd41-143">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dcd41-144">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dcd41-144">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="dcd41-145">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="dcd41-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dcd41-146">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="dcd41-146">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="dcd41-147">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="dcd41-147">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="dcd41-148">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="dcd41-148">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="dcd41-149">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="dcd41-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="dcd41-150">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="dcd41-150">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="dcd41-151">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dcd41-151">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="dcd41-152">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="dcd41-152">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="dcd41-153">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="dcd41-153">RELATED LINKS</span></span>

