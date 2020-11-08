---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174431"
---
# <span data-ttu-id="25775-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="25775-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="25775-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="25775-102">SYNOPSIS</span></span>
<span data-ttu-id="25775-103">Get-AzPolicyAlias ruft und gibt Azure-Anbieter-Ressourcentypen aus, deren Aliase definiert sind und den angegebenen Parameterwerten entsprechen.</span><span class="sxs-lookup"><span data-stu-id="25775-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="25775-104">Wenn keine Parameter angegeben werden, werden alle Anbieter Ressourcentypen ausgegeben, die einen Alias enthalten.</span><span class="sxs-lookup"><span data-stu-id="25775-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="25775-105">Der Schalter-ListAvailable ändert dieses Verhalten, indem alle übereinstimmenden Ressourcentypen aufgelistet werden, einschließlich derer ohne Aliase.</span><span class="sxs-lookup"><span data-stu-id="25775-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="25775-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="25775-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25775-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="25775-107">DESCRIPTION</span></span>
<span data-ttu-id="25775-108">Das Cmdlet " **Get-AzPolicyAlias** " Ruft eine Liste der Richtlinien Aliase ab.</span><span class="sxs-lookup"><span data-stu-id="25775-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="25775-109">Richtlinien Aliase werden von Azure-Richtlinie verwendet, um auf Ressourcentypeigenschaften zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="25775-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="25775-110">Es werden Parameter bereitgestellt, die Elemente im Eintrag einschränken, indem Sie verschiedene Eigenschaften des Ressourcentyps oder dessen Aliase vergleichen.</span><span class="sxs-lookup"><span data-stu-id="25775-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="25775-111">Ein angegebener Übereinstimmungs Wert entspricht, wenn die Zielzeichenfolge ihn unter Berücksichtigung der Groß-/Kleinschreibung vergleicht.</span><span class="sxs-lookup"><span data-stu-id="25775-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="25775-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="25775-112">EXAMPLES</span></span>

### <span data-ttu-id="25775-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="25775-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="25775-114">Listet alle Anbieter Ressourcentypen auf, die über einen Alias verfügen.</span><span class="sxs-lookup"><span data-stu-id="25775-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="25775-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="25775-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="25775-116">Listet alle Anbieter Ressourcentypen auf, einschließlich derer ohne Aliase.</span><span class="sxs-lookup"><span data-stu-id="25775-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="25775-117">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="25775-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="25775-118">Listet alle Anbieter Ressourcentypen auf, deren Namespace mit "Compute" übereinstimmt und einen Alias enthält.</span><span class="sxs-lookup"><span data-stu-id="25775-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="25775-119">Beispiel 4</span><span class="sxs-lookup"><span data-stu-id="25775-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="25775-120">Listet alle Anbieter Ressourcentypen auf, deren Ressourcentyp "virtuell" entspricht und einen Alias enthält.</span><span class="sxs-lookup"><span data-stu-id="25775-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="25775-121">Beispiel 5</span><span class="sxs-lookup"><span data-stu-id="25775-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="25775-122">Listet alle Anbieter Ressourcentypen auf, deren Ressourcentyp "virtuell" entspricht, einschließlich derer, die keine Aliase aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25775-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="25775-123">Beispiel 6</span><span class="sxs-lookup"><span data-stu-id="25775-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="25775-124">Listet alle Anbieter Ressourcentypen auf, deren Namespace mit "Compute" und "Ressourcentyp" übereinstimmt und einen Alias enthält.</span><span class="sxs-lookup"><span data-stu-id="25775-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="25775-125">Hinweis:-NamespaceMatch und-ResourceTypeMatch stellen exklusive Übereinstimmungen bereit, während die anderen inklusive sind.</span><span class="sxs-lookup"><span data-stu-id="25775-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="25775-126">Beispiel 7</span><span class="sxs-lookup"><span data-stu-id="25775-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="25775-127">Listet alle Anbieter Ressourcentypen auf, die einen Alias für "virtuell" enthalten.</span><span class="sxs-lookup"><span data-stu-id="25775-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="25775-128">Beispiel 8</span><span class="sxs-lookup"><span data-stu-id="25775-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="25775-129">Listet alle Anbieter Ressourcentypen auf, die einen Alias für "virtuell" oder einen Alias mit einem Pfad entsprechen, der "Network" entspricht.</span><span class="sxs-lookup"><span data-stu-id="25775-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="25775-130">Beispiel 9</span><span class="sxs-lookup"><span data-stu-id="25775-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="25775-131">Listet alle Anbieter Ressourcentypen mit Alpha-API-Version auf oder enthält einen Alias mit einer Alpha-API-Version.</span><span class="sxs-lookup"><span data-stu-id="25775-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="25775-132">Parameter</span><span class="sxs-lookup"><span data-stu-id="25775-132">PARAMETERS</span></span>

### <span data-ttu-id="25775-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="25775-133">-AliasMatch</span></span>
<span data-ttu-id="25775-134">Enthält die Ausgabeelemente mit Aliasen, deren Name mit diesem Wert übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="25775-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25775-135">-ApiVersion</span></span>
<span data-ttu-id="25775-136">Gibt an, dass die Version der zu verwendenden Ressourcenanbieter-API verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="25775-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="25775-137">Wenn Sie nicht angegeben wird, wird die API-Version automatisch als die neueste verfügbare Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="25775-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="25775-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="25775-138">-ApiVersionMatch</span></span>
<span data-ttu-id="25775-139">Enthält die Ausgabeelemente, deren Ressourcentypen oder Aliase über eine übereinstimmende API-Version verfügen.</span><span class="sxs-lookup"><span data-stu-id="25775-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="25775-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25775-140">-DefaultProfile</span></span>
<span data-ttu-id="25775-141">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="25775-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="25775-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="25775-142">-ListAvailable</span></span>
<span data-ttu-id="25775-143">Enthält in der Ausgabe übereinstimmende Elemente mit und ohne Aliase.</span><span class="sxs-lookup"><span data-stu-id="25775-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="25775-144">-LocationMatch</span></span>
<span data-ttu-id="25775-145">Enthält die Ausgabeelemente, deren Ressourcentypen einen übereinstimmenden Speicherort aufweisen.</span><span class="sxs-lookup"><span data-stu-id="25775-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="25775-146">-NamespaceMatch</span></span>
<span data-ttu-id="25775-147">Schränkt die Ausgabe auf Elemente ein, deren Namespace diesem Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="25775-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="25775-148">-PathMatch</span></span>
<span data-ttu-id="25775-149">Enthält die Ausgabeelemente mit Aliasen, die einen Pfad enthalten, der diesem Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="25775-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="25775-150">-Pre</span></span>
<span data-ttu-id="25775-151">Wenn festgelegt, gibt an, dass das Cmdlet Vorabversion-API-Versionen verwenden soll, wenn die zu verwendende Version automatisch ermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="25775-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="25775-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="25775-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="25775-153">Schränkt die Ausgabe auf Elemente ein, deren Ressourcentyp diesem Wert entspricht.</span><span class="sxs-lookup"><span data-stu-id="25775-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="25775-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25775-154">CommonParameters</span></span>
<span data-ttu-id="25775-155">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25775-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25775-156">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25775-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25775-157">Eingaben</span><span class="sxs-lookup"><span data-stu-id="25775-157">INPUTS</span></span>

### <span data-ttu-id="25775-158">Keine</span><span class="sxs-lookup"><span data-stu-id="25775-158">None</span></span>

## <span data-ttu-id="25775-159">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="25775-159">OUTPUTS</span></span>

### <span data-ttu-id="25775-160">Microsoft. Azure. Commands. ResourceManager. Cmdlets. Implementation. PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="25775-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="25775-161">Notizen</span><span class="sxs-lookup"><span data-stu-id="25775-161">NOTES</span></span>

* <span data-ttu-id="25775-162">Um die Aliase oder eine beliebige andere Eigenschaft zu erweitern, geben Sie die Ausgabe an `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="25775-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="25775-163">Zum Beispiel: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="25775-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="25775-164">Zusätzliche Eigenschaften stehen in der Ausgabe zur Verfügung und können angezeigt werden, indem Sie die Ausgabe an weiterleiten `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="25775-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="25775-165">Zum Beispiel: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="25775-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="25775-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="25775-166">RELATED LINKS</span></span>
