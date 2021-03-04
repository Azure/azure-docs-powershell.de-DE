---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: 92a9e1820af2e850af6c3abaca71a7be1f15ed5f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918112"
---
# <span data-ttu-id="ed223-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed223-101">Get-AzResource</span></span>

## <span data-ttu-id="ed223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed223-102">SYNOPSIS</span></span>

<span data-ttu-id="ed223-103">Ruft Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="ed223-103">Gets resources.</span></span>

## <span data-ttu-id="ed223-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ed223-104">SYNTAX</span></span>

### <span data-ttu-id="ed223-105">ByTagNameValueParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed223-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed223-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed223-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed223-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed223-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed223-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed223-108">DESCRIPTION</span></span>

<span data-ttu-id="ed223-109">Das **Get-AzResource-Cmdlet** ruft Azure-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="ed223-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="ed223-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ed223-110">EXAMPLES</span></span>

### <span data-ttu-id="ed223-111">Beispiel 1: Alle Ressourcen im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="ed223-111">Example 1: Get all resources in the current subscription</span></span>

```
PS C:\> Get-AzResource | ft

Name    ResourceGroupName  ResourceType                            Location
----    -----------------  ------------                            --------
testVM  testRG             Microsoft.Compute/virtualMachines       westus
disk    testRG             Microsoft.Compute/disks                 westus
nic     testRG             Microsoft.Network/networkInterfaces     westus
nsg     testRG             Microsoft.Network/networkSecurityGroups westus
ip      testRG             Microsoft.Network/publicIPAddresses     westus
vnet    testRG             Microsoft.Network/virtualNetworks       westus
testKV  otherRG            Microsoft.KeyVault/vaults               eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts       eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines       eastus
```

<span data-ttu-id="ed223-112">Dieser Befehl ruft alle Ressourcen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="ed223-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="ed223-113">Beispiel 2: Alle Ressourcen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="ed223-113">Example 2: Get all resources in a resource group</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName testRG | ft

Name   ResourceGroupName ResourceType                            Location
----   ----------------- ------------                            --------
testVM testRG            Microsoft.Compute/virtualMachines       westus
disk   testRG            Microsoft.Compute/disks                 westus
nic    testRG            Microsoft.Network/networkInterfaces     westus
nsg    testRG            Microsoft.Network/networkSecurityGroups westus
ip     testRG            Microsoft.Network/publicIPAddresses     westus
vnet   testRG            Microsoft.Network/virtualNetworks       westus
```

<span data-ttu-id="ed223-114">Dieser Befehl ruft alle Ressourcen in der Ressourcengruppe "testRG" ab.</span><span class="sxs-lookup"><span data-stu-id="ed223-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="ed223-115">Beispiel 3: Alle Ressourcen erhalten, deren Ressourcengruppe dem bereitgestellten Platzhalter entspricht</span><span class="sxs-lookup"><span data-stu-id="ed223-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="ed223-116">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcengruppe sie in Wesen mit "andere" gehören.</span><span class="sxs-lookup"><span data-stu-id="ed223-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="ed223-117">Beispiel 4: Alle Ressourcen mit einem angegebenen Namen erhalten</span><span class="sxs-lookup"><span data-stu-id="ed223-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="ed223-118">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname "testVM" ist.</span><span class="sxs-lookup"><span data-stu-id="ed223-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="ed223-119">Beispiel 5: Alle Ressourcen erhalten, deren Name dem bereitgestellten Platzhalter entspricht</span><span class="sxs-lookup"><span data-stu-id="ed223-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="ed223-120">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname mit "test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="ed223-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="ed223-121">Beispiel 6: Alle Ressourcen eines bestimmten Ressourcentyps erhalten</span><span class="sxs-lookup"><span data-stu-id="ed223-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="ed223-122">Dieser Befehl ruft alle Ressourcen in den aktuellen Abonnements ab, die virtuelle Computer sind.</span><span class="sxs-lookup"><span data-stu-id="ed223-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="ed223-123">Beispiel 7: Erhalten einer Ressource nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ed223-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
Tags              :
                    Name    Value
                    ======  ========
                    Dept    IT
                    Year    2002
                    Status  Approved
```

<span data-ttu-id="ed223-124">Dieser Befehl ruft die Ressource mit der bereitgestellten Ressourcen-ID ab, bei der es sich um einen virtuellen Computer namens "testVM" in der Ressourcengruppe "testRG" handelt.</span><span class="sxs-lookup"><span data-stu-id="ed223-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="ed223-125">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ed223-125">PARAMETERS</span></span>

### <span data-ttu-id="ed223-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ed223-126">-ApiVersion</span></span>

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

### <span data-ttu-id="ed223-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed223-127">-DefaultProfile</span></span>
<span data-ttu-id="ed223-128">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ed223-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed223-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="ed223-129">-ExpandProperties</span></span>
<span data-ttu-id="ed223-130">Wenn angegeben, werden die Eigenschaften der Ressource erweitert.</span><span class="sxs-lookup"><span data-stu-id="ed223-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="ed223-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ed223-131">-Name</span></span>
<span data-ttu-id="ed223-132">Der Name der ressource(n), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed223-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="ed223-133">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ed223-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ed223-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="ed223-134">-ODataQuery</span></span>

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

### <span data-ttu-id="ed223-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="ed223-135">-Pre</span></span>

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

### <span data-ttu-id="ed223-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed223-136">-ResourceGroupName</span></span>
<span data-ttu-id="ed223-137">Die Ressourcengruppe, in der die abgerufenen Ressourcen gehören.</span><span class="sxs-lookup"><span data-stu-id="ed223-137">The resource group the resource(s) that is retrieved belongs in.</span></span> <span data-ttu-id="ed223-138">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ed223-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="ed223-139">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ed223-139">-ResourceId</span></span>
<span data-ttu-id="ed223-140">Gibt die vollqualifizierte Ressourcen-ID an, wie im folgenden Beispiel. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="ed223-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed223-141">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ed223-141">-ResourceType</span></span>
<span data-ttu-id="ed223-142">Der Ressourcentyp der ressource(n), die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ed223-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="ed223-143">Microsoft.Compute/virtualMachines beispielsweise</span><span class="sxs-lookup"><span data-stu-id="ed223-143">For example, Microsoft.Compute/virtualMachines</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet, ByTagObjectParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed223-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="ed223-144">-Tag</span></span>

<span data-ttu-id="ed223-145">Ruft Ressourcen ab, die das angegebene Azure-Tag haben.</span><span class="sxs-lookup"><span data-stu-id="ed223-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="ed223-146">Geben Sie eine Hashtabelle mit einem Namens- oder Namens- und Wertschlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="ed223-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="ed223-147">Platzhalterzeichen werden nicht unterstützt. Ein "Tag" ist ein Name-Wert-Paar, das Sie auf Ressourcen und Ressourcengruppen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="ed223-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="ed223-148">Verwenden Sie Kategorien, um Ihre Ressourcen zu kategorisieren, z. B. nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen nachverfolgt zu werden.</span><span class="sxs-lookup"><span data-stu-id="ed223-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="ed223-149">Wenn Sie einer Ressource ein Tag hinzufügen möchten, verwenden Sie den Parameter Tag der New-AzResource oder Set-AzResource cmdlets.</span><span class="sxs-lookup"><span data-stu-id="ed223-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="ed223-150">Zum Erstellen eines vordefinierten Tags verwenden Sie das New-AzTag Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed223-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="ed223-151">Wenn Sie Hilfe zu #A0 in Windows PowerShell, führen Sie "Get-Help about_Hashtables" aus.</span><span class="sxs-lookup"><span data-stu-id="ed223-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByTagObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed223-152">-TagName</span><span class="sxs-lookup"><span data-stu-id="ed223-152">-TagName</span></span>
<span data-ttu-id="ed223-153">Der Schlüssel im Tag der abzurufende Ressource(n).</span><span class="sxs-lookup"><span data-stu-id="ed223-153">The key in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed223-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="ed223-154">-TagValue</span></span>
<span data-ttu-id="ed223-155">Der Wert im Tag der abzurufende Ressource(en).</span><span class="sxs-lookup"><span data-stu-id="ed223-155">The value in the tag of the resource(s) to be retrieved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagNameValueParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed223-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed223-156">CommonParameters</span></span>
<span data-ttu-id="ed223-157">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed223-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed223-158">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ed223-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed223-159">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ed223-159">INPUTS</span></span>

### <span data-ttu-id="ed223-160">System.String</span><span class="sxs-lookup"><span data-stu-id="ed223-160">System.String</span></span>

## <span data-ttu-id="ed223-161">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ed223-161">OUTPUTS</span></span>

### <span data-ttu-id="ed223-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="ed223-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="ed223-163">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ed223-163">NOTES</span></span>

## <span data-ttu-id="ed223-164">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ed223-164">RELATED LINKS</span></span>

[<span data-ttu-id="ed223-165">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed223-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="ed223-166">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed223-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="ed223-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed223-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="ed223-168">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="ed223-168">Set-AzResource</span></span>](./Set-AzResource.md)