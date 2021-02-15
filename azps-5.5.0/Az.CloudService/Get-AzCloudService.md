---
external help file: ''
Module Name: Az.CloudService
online version: https://docs.microsoft.com/en-us/powershell/module/az.cloudservice/get-azcloudservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CloudService/help/Get-AzCloudService.md
ms.openlocfilehash: faab9e645f05b8b661b03911bcba517e770f4d78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171378"
---
# <span data-ttu-id="60ace-101">Get-AzCloudService</span><span class="sxs-lookup"><span data-stu-id="60ace-101">Get-AzCloudService</span></span>

## <span data-ttu-id="60ace-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60ace-102">SYNOPSIS</span></span>
<span data-ttu-id="60ace-103">Anzeigen von Informationen zu einem Clouddienst</span><span class="sxs-lookup"><span data-stu-id="60ace-103">Display information about a cloud service.</span></span>

## <span data-ttu-id="60ace-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60ace-104">SYNTAX</span></span>

### <span data-ttu-id="60ace-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="60ace-105">List (Default)</span></span>
```
Get-AzCloudService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60ace-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="60ace-106">Get</span></span>
```
Get-AzCloudService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60ace-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="60ace-107">GetViaIdentity</span></span>
```
Get-AzCloudService -InputObject <ICloudServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="60ace-108">Liste1</span><span class="sxs-lookup"><span data-stu-id="60ace-108">List1</span></span>
```
Get-AzCloudService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="60ace-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60ace-109">DESCRIPTION</span></span>
<span data-ttu-id="60ace-110">Anzeigen von Informationen zu einem Clouddienst</span><span class="sxs-lookup"><span data-stu-id="60ace-110">Display information about a cloud service.</span></span>

## <span data-ttu-id="60ace-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60ace-111">EXAMPLES</span></span>

### <span data-ttu-id="60ace-112">Beispiel 1: Den ganzen Clouddienst unter einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="60ace-112">Example 1: Get all cloud service under a resource group</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded
ContosOrg         ContosoCSTest     eastus2euap Failed
```

<span data-ttu-id="60ace-113">Dieser Befehl ruft alle Clouddienste in der Ressourcengruppe "ContosOrg" ab.</span><span class="sxs-lookup"><span data-stu-id="60ace-113">This command gets all cloud services in resource group named ContosOrg</span></span>

### <span data-ttu-id="60ace-114">Beispiel 2: Clouddienst erhalten</span><span class="sxs-lookup"><span data-stu-id="60ace-114">Example 2: Get cloud service</span></span>
```powershell
PS C:\> Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"

ResourceGroupName Name              Location    ProvisioningState
----------------- ----              --------    -----------------
ContosOrg         ContosoCS         eastus2euap Succeeded

PS C:\> $cloudService = Get-AzCloudService -ResourceGroupName "ContosOrg" -CloudServiceName "ContosoCS"
PS C:\> $cloudService | Format-List
ResourceGroupName : ContosOrg
Configuration     : xxxxxxxx
ConfigurationUrl  :
ExtensionProfile  : xxxxxxxx
Id                : xxxxxxxx
Location          : East US
Name              : ContosoCS
NetworkProfile    : xxxxxxxx
OSProfile         : xxxxxxxx
PackageUrl        : xxxxxxxx
ProvisioningState : Succeeded
RoleProfile       : xxxxxxxx
StartCloudService :
Tag               : {
                      "Owner": "Contos"
                    }
Type              : Microsoft.Compute/cloudServices
UniqueId          : xxxxxxxx
UpgradeMode       : Auto

```

<span data-ttu-id="60ace-115">Dieser Befehl ruft den Clouddienst "ContosoCS" ab, der zur Ressourcengruppe "ContosOrg" gehört.</span><span class="sxs-lookup"><span data-stu-id="60ace-115">This command gets cloud service named ContosoCS that belongs to the resource group named ContosOrg.</span></span>

## <span data-ttu-id="60ace-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60ace-116">PARAMETERS</span></span>

### <span data-ttu-id="60ace-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60ace-117">-DefaultProfile</span></span>
<span data-ttu-id="60ace-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60ace-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60ace-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="60ace-119">-InputObject</span></span>
<span data-ttu-id="60ace-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="60ace-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="60ace-121">-Name</span><span class="sxs-lookup"><span data-stu-id="60ace-121">-Name</span></span>
<span data-ttu-id="60ace-122">Der Name des Clouddiensts.</span><span class="sxs-lookup"><span data-stu-id="60ace-122">Name of the cloud service.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: CloudServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ace-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60ace-123">-ResourceGroupName</span></span>
<span data-ttu-id="60ace-124">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="60ace-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60ace-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60ace-125">-SubscriptionId</span></span>
<span data-ttu-id="60ace-126">Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="60ace-126">Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60ace-127">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="60ace-127">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60ace-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60ace-128">CommonParameters</span></span>
<span data-ttu-id="60ace-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60ace-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60ace-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60ace-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60ace-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60ace-131">INPUTS</span></span>

### <span data-ttu-id="60ace-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="60ace-132">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.ICloudServiceIdentity</span></span>

## <span data-ttu-id="60ace-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60ace-133">OUTPUTS</span></span>

### <span data-ttu-id="60ace-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span><span class="sxs-lookup"><span data-stu-id="60ace-134">Microsoft.Azure.PowerShell.Cmdlets.CloudService.Models.Api20201001Preview.ICloudService</span></span>

## <span data-ttu-id="60ace-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60ace-135">NOTES</span></span>

<span data-ttu-id="60ace-136">ALIASE</span><span class="sxs-lookup"><span data-stu-id="60ace-136">ALIASES</span></span>

<span data-ttu-id="60ace-137">KOMPLEXE PARAMETEREIGENSCHAFTEN</span><span class="sxs-lookup"><span data-stu-id="60ace-137">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="60ace-138">Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="60ace-138">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="60ace-139">Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="60ace-139">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="60ace-140">INPUTOBJECT <ICloudServiceIdentity> : Identity Parameter</span><span class="sxs-lookup"><span data-stu-id="60ace-140">INPUTOBJECT <ICloudServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="60ace-141">`[CloudServiceName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="60ace-141">`[CloudServiceName <String>]`:</span></span> 
  - <span data-ttu-id="60ace-142">`[Id <String>]`: Ressourcenidentitätspfad</span><span class="sxs-lookup"><span data-stu-id="60ace-142">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="60ace-143">`[ResourceGroupName <String>]`:</span><span class="sxs-lookup"><span data-stu-id="60ace-143">`[ResourceGroupName <String>]`:</span></span> 
  - <span data-ttu-id="60ace-144">`[RoleInstanceName <String>]`: Name der Rolleninstanz.</span><span class="sxs-lookup"><span data-stu-id="60ace-144">`[RoleInstanceName <String>]`: Name of the role instance.</span></span>
  - <span data-ttu-id="60ace-145">`[RoleName <String>]`: Name der Rolle.</span><span class="sxs-lookup"><span data-stu-id="60ace-145">`[RoleName <String>]`: Name of the role.</span></span>
  - <span data-ttu-id="60ace-146">`[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="60ace-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="60ace-147">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="60ace-147">The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="60ace-148">`[UpdateDomain <Int32?>]`: Gibt einen ganzzahligen Wert an, der die Updatedomäne identifiziert.</span><span class="sxs-lookup"><span data-stu-id="60ace-148">`[UpdateDomain <Int32?>]`: Specifies an integer value that identifies the update domain.</span></span> <span data-ttu-id="60ace-149">Updatedomänen werden mit einem nullbasierten Index identifiziert: Die erste Updatedomäne hat die ID 0, die zweite die ID 1 und so weiter.</span><span class="sxs-lookup"><span data-stu-id="60ace-149">Update domains are identified with a zero-based index: the first update domain has an ID of 0, the second has an ID of 1, and so on.</span></span>

## <span data-ttu-id="60ace-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60ace-150">RELATED LINKS</span></span>

