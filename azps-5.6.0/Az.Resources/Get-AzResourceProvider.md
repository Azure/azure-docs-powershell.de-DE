---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 6AB09621-488B-4A16-92D9-9C47EB87DA95
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceProvider.md
ms.openlocfilehash: 57e1aa691ffaca498e925488fb90fb8b828ff9f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922352"
---
# <span data-ttu-id="20c13-101">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="20c13-101">Get-AzResourceProvider</span></span>

## <span data-ttu-id="20c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20c13-102">SYNOPSIS</span></span>
<span data-ttu-id="20c13-103">Ruft einen Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="20c13-103">Gets a resource provider.</span></span>

## <span data-ttu-id="20c13-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20c13-104">SYNTAX</span></span>

### <span data-ttu-id="20c13-105">ListAvailable (Standard)</span><span class="sxs-lookup"><span data-stu-id="20c13-105">ListAvailable (Default)</span></span>
```
Get-AzResourceProvider [-Location <String>] [-ListAvailable] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20c13-106">IndividualProvider</span><span class="sxs-lookup"><span data-stu-id="20c13-106">IndividualProvider</span></span>
```
Get-AzResourceProvider -ProviderNamespace <String[]> [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20c13-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="20c13-107">DESCRIPTION</span></span>
<span data-ttu-id="20c13-108">Das **Get-AzResourceProvider-Cmdlet** ruft einen Azure-Ressourcenanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="20c13-108">The **Get-AzResourceProvider** cmdlet gets an Azure resource provider.</span></span>

## <span data-ttu-id="20c13-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="20c13-109">EXAMPLES</span></span>

### <span data-ttu-id="20c13-110">Beispiel 1: Alle Ressourcenanbieter erhalten, die mit dem aktuellen Abonnement registriert sind</span><span class="sxs-lookup"><span data-stu-id="20c13-110">Example 1: Get all resource providers registered with the current subscription</span></span>

```powershell
PS C:\>Get-AzResourceProvider

ProviderNamespace : Microsoft.AppConfiguration
RegistrationState : Registered
ResourceTypes     : {configurationStores, configurationStores/eventGridFilters, checkNameAvailability, locations…}
Locations         : {West Central US, Central US, West US, East US…}

ProviderNamespace : Microsoft.KeyVault
RegistrationState : Registered
ResourceTypes     : {vaults, vaults/secrets, vaults/accessPolicies, operations…}
Locations         : {North Central US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks, publicIPAddresses, networkInterfaces, privateEndpoints…}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets, virtualMachines, virtualMachines/extensions, virtualMachineScaleSets…}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Security
RegistrationState : Registered
ResourceTypes     : {operations, securityStatuses, tasks, regulatoryComplianceStandards…}
Locations         : {Central US, East US, West Europe, West Central US…}

ProviderNamespace : Microsoft.ResourceHealth
RegistrationState : Registered
ResourceTypes     : {availabilityStatuses, childAvailabilityStatuses, childResources, events…}
Locations         : {Australia Southeast}

ProviderNamespace : Microsoft.PolicyInsights
RegistrationState : Registered
ResourceTypes     : {policyEvents, policyStates, operations, asyncOperationResults…}
Locations         : {}

ProviderNamespace : Microsoft.Storage
RegistrationState : Registered
ResourceTypes     : {storageAccounts, operations, locations/asyncoperations, storageAccounts/listAccountSas…}
Locations         : {East US, East US 2, West US, West Europe…}

ProviderNamespace : Microsoft.Web
RegistrationState : Registered
ResourceTypes     : {publishingUsers, ishostnameavailable, validate, isusernameavailable…}
Locations         : {Central US, North Europe, West Europe, Southeast Asia…}

ProviderNamespace : Sendgrid.Email
RegistrationState : Registered
ResourceTypes     : {accounts, operations}
Locations         : {Australia East, Australia Southeast, Brazil South, Canada Central…}

ProviderNamespace : Microsoft.Authorization
RegistrationState : Registered
ResourceTypes     : {roleAssignments, roleDefinitions, classicAdministrators, permissions…}
Locations         : {}
...
```

<span data-ttu-id="20c13-111">Dieser Befehl ruft alle Ressourcenanbieter aus dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="20c13-111">This command gets all the resource providers from the subscription.</span></span>

### <span data-ttu-id="20c13-112">Beispiel 2: Alle Ressourcenanbieterdetails aus dem angegebenen ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="20c13-112">Example 2: Get all resource provider details from the given ProviderNamespace</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/networkInterfaces}
Locations         : {East US, East US 2, West US, Central US…}
...
```

<span data-ttu-id="20c13-113">Dieser Befehl Ruft alle Ressourcenanbieter unter "Microsoft.Compute" ab.</span><span class="sxs-lookup"><span data-stu-id="20c13-113">This command Gets all the resource providers under "Microsoft.Compute".</span></span>

### <span data-ttu-id="20c13-114">Beispiel 3: Alle Ressourcenanbieterdetails aus dem angegebenen ProviderNamespace-Array</span><span class="sxs-lookup"><span data-stu-id="20c13-114">Example 3: Get all resource provider details from the given ProviderNamespace array</span></span>

```powershell
PS C:\>Get-AzResourceProvider -ProviderNamespace Microsoft.Compute,Microsoft.Network
ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {availabilitySets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachines/extensions}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets}
Locations         : {East US, East US 2, West US, Central US…}

ProviderNamespace : Microsoft.Compute
RegistrationState : Registered
ResourceTypes     : {virtualMachineScaleSets/extensions}
Locations         : {East US, East US 2, West US, Central US…}
...

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {virtualNetworks}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {publicIPAddresses}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkInterfaces}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpoints}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {privateEndpointRedirectMaps}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {loadBalancers}
Locations         : {West US, East US, North Europe, West Europe…}

ProviderNamespace : Microsoft.Network
RegistrationState : Registered
ResourceTypes     : {networkSecurityGroups}
Locations         : {West US, East US, North Europe, West Europe…}
...
```

<span data-ttu-id="20c13-115">Dieser Befehl ruft alle Ressourcenanbieter unter "Microsoft.Compute" und "Microsoft.Network" ab.</span><span class="sxs-lookup"><span data-stu-id="20c13-115">This command Gets all the resource providers under "Microsoft.Compute" and "Microsoft.Network".</span></span>

## <span data-ttu-id="20c13-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="20c13-116">PARAMETERS</span></span>

### <span data-ttu-id="20c13-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="20c13-117">-ApiVersion</span></span>
<span data-ttu-id="20c13-118">Gibt die vom Ressourcenanbieter unterstützte API-Version an.</span><span class="sxs-lookup"><span data-stu-id="20c13-118">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="20c13-119">Sie können eine andere Version als die Standardversion angeben.</span><span class="sxs-lookup"><span data-stu-id="20c13-119">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="20c13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20c13-120">-DefaultProfile</span></span>
<span data-ttu-id="20c13-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="20c13-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c13-122">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="20c13-122">-ListAvailable</span></span>
<span data-ttu-id="20c13-123">Gibt an, dass dieser Vorgang alle verfügbaren Ressourcenanbieter erhält.</span><span class="sxs-lookup"><span data-stu-id="20c13-123">Indicates that this operation gets all available resource providers.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ListAvailable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20c13-124">-Location</span><span class="sxs-lookup"><span data-stu-id="20c13-124">-Location</span></span>
<span data-ttu-id="20c13-125">Gibt den Speicherort des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="20c13-125">Specifies the location of the resource provider.</span></span>

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

### <span data-ttu-id="20c13-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="20c13-126">-Pre</span></span>
<span data-ttu-id="20c13-127">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="20c13-127">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="20c13-128">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="20c13-128">-ProviderNamespace</span></span>
<span data-ttu-id="20c13-129">Gibt den Namespace des Ressourcenanbieters an.</span><span class="sxs-lookup"><span data-stu-id="20c13-129">Specifies the namespace of the resource provider.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IndividualProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20c13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20c13-130">CommonParameters</span></span>
<span data-ttu-id="20c13-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20c13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20c13-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20c13-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20c13-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="20c13-133">INPUTS</span></span>

### <span data-ttu-id="20c13-134">System.String[]</span><span class="sxs-lookup"><span data-stu-id="20c13-134">System.String[]</span></span>

## <span data-ttu-id="20c13-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="20c13-135">OUTPUTS</span></span>

### <span data-ttu-id="20c13-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="20c13-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="20c13-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="20c13-137">NOTES</span></span>

## <span data-ttu-id="20c13-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="20c13-138">RELATED LINKS</span></span>

[<span data-ttu-id="20c13-139">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="20c13-139">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)

[<span data-ttu-id="20c13-140">Aufheben der Registrierung-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="20c13-140">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


