---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C2C608E5-3351-4D01-8533-9668B2E9F1D1
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResource.md
ms.openlocfilehash: de91566be3c9bcd62f28dbcba80409622e86a4b5
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/08/2020
ms.locfileid: "93665431"
---
# <span data-ttu-id="6b90c-101">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-101">Get-AzResource</span></span>

## <span data-ttu-id="6b90c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6b90c-102">SYNOPSIS</span></span>

<span data-ttu-id="6b90c-103">Ruft Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="6b90c-103">Gets resources.</span></span>

## <span data-ttu-id="6b90c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b90c-104">SYNTAX</span></span>

### <span data-ttu-id="6b90c-105">ByTagNameValueParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b90c-105">ByTagNameValueParameterSet (Default)</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 [-TagName <String>] [-TagValue <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b90c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6b90c-106">ByResourceId</span></span>
```
Get-AzResource -ResourceId <String> [-ODataQuery <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6b90c-107">ByTagObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6b90c-107">ByTagObjectParameterSet</span></span>
```
Get-AzResource [-Name <String>] [-ResourceType <String>] [-ODataQuery <String>] [-ResourceGroupName <String>]
 -Tag <Hashtable> [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b90c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6b90c-108">DESCRIPTION</span></span>

<span data-ttu-id="6b90c-109">Das Cmdlet " **Get-AzResource** " ruft Azure-Ressourcen ab.</span><span class="sxs-lookup"><span data-stu-id="6b90c-109">The **Get-AzResource** cmdlet gets Azure resources.</span></span>

## <span data-ttu-id="6b90c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6b90c-110">EXAMPLES</span></span>

### <span data-ttu-id="6b90c-111">Beispiel 1: Abrufen aller Ressourcen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6b90c-111">Example 1: Get all resources in the current subscription</span></span>

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

<span data-ttu-id="6b90c-112">Dieser Befehl ruft alle Ressourcen im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6b90c-112">This command gets all of the resources in the current subscription.</span></span>

### <span data-ttu-id="6b90c-113">Beispiel 2: Abrufen aller Ressourcen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6b90c-113">Example 2: Get all resources in a resource group</span></span>

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

<span data-ttu-id="6b90c-114">Dieser Befehl ruft alle Ressourcen in der Ressourcengruppe "testRG" ab.</span><span class="sxs-lookup"><span data-stu-id="6b90c-114">This command gets all of the resources in the resource group "testRG".</span></span>

### <span data-ttu-id="6b90c-115">Beispiel 3: Abrufen aller Ressourcen, deren Ressourcengruppe mit dem bereitgestellten Platzhalter übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="6b90c-115">Example 3: Get all resources whose resource group matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -ResourceGroupName other* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
storage otherResourceGroup Microsoft.Storage/storageAccounts eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6b90c-116">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcengruppe Sie zu Wesen gehören, mit "Other".</span><span class="sxs-lookup"><span data-stu-id="6b90c-116">This command gets all of the resources whose resource group they belong in beings with "other".</span></span>

### <span data-ttu-id="6b90c-117">Beispiel 4: Abrufen aller Ressourcen mit einem angegebenen Namen</span><span class="sxs-lookup"><span data-stu-id="6b90c-117">Example 4: Get all resources with a given name</span></span>

```
PS C:\> Get-AzResource -Name testVM | fl

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="6b90c-118">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname "testVM" lautet.</span><span class="sxs-lookup"><span data-stu-id="6b90c-118">This command gets all of the resources whose resource name is "testVM".</span></span>

### <span data-ttu-id="6b90c-119">Beispiel 5: Abrufen aller Ressourcen, deren Name mit dem bereitgestellten Platzhalter übereinstimmt</span><span class="sxs-lookup"><span data-stu-id="6b90c-119">Example 5: Get all resources whose name matches the provided wildcard</span></span>

```
PS C:\> Get-AzResource -Name test* | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testKV  otherRG            Microsoft.KeyVault/vaults         eastus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6b90c-120">Dieser Befehl ruft alle Ressourcen ab, deren Ressourcenname mit "Test" beginnt.</span><span class="sxs-lookup"><span data-stu-id="6b90c-120">This command gets all of the resources whose resource name begins with "test".</span></span>

### <span data-ttu-id="6b90c-121">Beispiel 6: Abrufen aller Ressourcen eines angegebenen Ressourcentyps</span><span class="sxs-lookup"><span data-stu-id="6b90c-121">Example 6: Get all resources of a given resource type</span></span>

```
PS C:\> Get-AzResource -ResourceType Microsoft.Compute/virtualMachines | ft

Name    ResourceGroupName  ResourceType                      Location
----    -----------------  ------------                      --------
testVM  testRG             Microsoft.Compute/virtualMachines westus
testVM2 otherResourceGroup Microsoft.Compute/virtualMachines eastus
```

<span data-ttu-id="6b90c-122">Dieser Befehl ruft alle Ressourcen in den aktuellen Abonnements ab, die virtuelle Maschinen sind.</span><span class="sxs-lookup"><span data-stu-id="6b90c-122">This command gets all of the resources in the current subscriptions that are virtual machines.</span></span>

### <span data-ttu-id="6b90c-123">Beispiel 7: Abrufen einer Ressource nach Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="6b90c-123">Example 7: Get a resource by resource id</span></span>

```
PS C:\> Get-AzResource -ResourceId /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM

Name              : testVM
ResourceGroupName : testRG
ResourceType      : Microsoft.Compute/virtualMachines
Location          : westus
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testRG/providers/Microsoft.Compute/virtualMachines/testVM
```

<span data-ttu-id="6b90c-124">Dieser Befehl ruft die Ressource mit der bereitgestellten Ressourcen-ID ab, bei der es sich um einen virtuellen Computer mit dem Namen "testVM" in der Ressourcengruppe "testRG" handelt.</span><span class="sxs-lookup"><span data-stu-id="6b90c-124">This command gets the resource with the provided resource id, which is a virtual machine called "testVM" in the resource group "testRG".</span></span>

## <span data-ttu-id="6b90c-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="6b90c-125">PARAMETERS</span></span>

### <span data-ttu-id="6b90c-126">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b90c-126">-ApiVersion</span></span>

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

### <span data-ttu-id="6b90c-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b90c-127">-DefaultProfile</span></span>
<span data-ttu-id="6b90c-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6b90c-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b90c-129">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="6b90c-129">-ExpandProperties</span></span>
<span data-ttu-id="6b90c-130">Wenn angegeben, werden die Eigenschaften der Ressource erweitert.</span><span class="sxs-lookup"><span data-stu-id="6b90c-130">When specified, expands the properties of the resource.</span></span>

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

### <span data-ttu-id="6b90c-131">-Name</span><span class="sxs-lookup"><span data-stu-id="6b90c-131">-Name</span></span>
<span data-ttu-id="6b90c-132">Der Name der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-132">The name of the resource(s) to be retrieved.</span></span> <span data-ttu-id="6b90c-133">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b90c-133">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="6b90c-134">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6b90c-134">-ODataQuery</span></span>

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

### <span data-ttu-id="6b90c-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b90c-135">-Pre</span></span>

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

### <span data-ttu-id="6b90c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b90c-136">-ResourceGroupName</span></span>
<span data-ttu-id="6b90c-137">Die Ressourcengruppe, in der die retireved-Ressourcen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6b90c-137">The resource group the resource(s) that is retireved belongs in.</span></span> <span data-ttu-id="6b90c-138">Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="6b90c-138">This parameter supports wildcards at the beginning and/or end of the string.</span></span>

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

### <span data-ttu-id="6b90c-139">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="6b90c-139">-ResourceId</span></span>
<span data-ttu-id="6b90c-140">Gibt die vollqualifizierte Ressourcen-ID an, wie im folgenden Beispiel gezeigt. `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span><span class="sxs-lookup"><span data-stu-id="6b90c-140">Specifies the fully qualified resource ID, as in the following example `/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/providers/Microsoft.Compute/virtualMachines`</span></span>

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

### <span data-ttu-id="6b90c-141">-</span><span class="sxs-lookup"><span data-stu-id="6b90c-141">-ResourceType</span></span>
<span data-ttu-id="6b90c-142">Der Ressourcentyp der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-142">The resource type of the resource(s) to be retrieved.</span></span> <span data-ttu-id="6b90c-143">Beispiel: Microsoft. Compute/virtualMachines</span><span class="sxs-lookup"><span data-stu-id="6b90c-143">For example, Microsoft.Compute/virtualMachines</span></span>

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

### <span data-ttu-id="6b90c-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b90c-144">-Tag</span></span>

<span data-ttu-id="6b90c-145">Ruft Ressourcen ab, die das angegebene Azure-Tag aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-145">Gets resources that have the specified Azure tag.</span></span> <span data-ttu-id="6b90c-146">Geben Sie eine Hashtabelle mit einem Namensschlüssel oder einem Namen-und Wert Schlüssel ein.</span><span class="sxs-lookup"><span data-stu-id="6b90c-146">Enter a hash table with a Name key or Name and Value keys.</span></span> <span data-ttu-id="6b90c-147">Platzhalterzeichen werden nicht unterstützt. Ein "Tag" ist ein Name-Wert-Paar, das Sie auf Ressourcen und Ressourcengruppen anwenden können.</span><span class="sxs-lookup"><span data-stu-id="6b90c-147">Wildcard characters are not supported.A "tag" is a name-value pair that you can apply to resources and resource groups.</span></span> <span data-ttu-id="6b90c-148">Verwenden Sie Kategorien, um Ihre Ressourcen zu kategorisieren, beispielsweise nach Abteilung oder Kostenstelle, oder um Notizen oder Kommentare zu den Ressourcen zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-148">Use tags to categorize your resources, such as by department or cost center, or to track notes or comments about the resources.</span></span> <span data-ttu-id="6b90c-149">Verwenden Sie zum Hinzufügen einer Kategorie zu einer Ressource den Tag-Parameter der New-AzResource-oder Set-AzResource-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="6b90c-149">To add a tag to a resource, use the Tag parameter of the New-AzResource or Set-AzResource cmdlets.</span></span> <span data-ttu-id="6b90c-150">Verwenden Sie das New-AzTag-Cmdlet, um eine vordefinierte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-150">To create a predefined tag, use the New-AzTag cmdlet.</span></span> <span data-ttu-id="6b90c-151">Wenn Sie Hilfe zu Hashtabellen in Windows PowerShell benötigen, führen Sie "Get-Help about_Hashtables" aus.</span><span class="sxs-lookup"><span data-stu-id="6b90c-151">For help with hash tables in Windows PowerShell, run 'Get-Help about_Hashtables'.</span></span>

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

### <span data-ttu-id="6b90c-152">-Tagname</span><span class="sxs-lookup"><span data-stu-id="6b90c-152">-TagName</span></span>
<span data-ttu-id="6b90c-153">Der Schlüssel im Tag der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-153">The key in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="6b90c-154">-TagValue</span><span class="sxs-lookup"><span data-stu-id="6b90c-154">-TagValue</span></span>
<span data-ttu-id="6b90c-155">Der Wert im Tag der Ressourcen, die abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b90c-155">The value in the tag of the resource(s) to be retrieved.</span></span>

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

### <span data-ttu-id="6b90c-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b90c-156">CommonParameters</span></span>
<span data-ttu-id="6b90c-157">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b90c-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b90c-158">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b90c-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b90c-159">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6b90c-159">INPUTS</span></span>

### <span data-ttu-id="6b90c-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6b90c-160">System.String</span></span>

## <span data-ttu-id="6b90c-161">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6b90c-161">OUTPUTS</span></span>

### <span data-ttu-id="6b90c-162">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-162">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

## <span data-ttu-id="6b90c-163">Notizen</span><span class="sxs-lookup"><span data-stu-id="6b90c-163">NOTES</span></span>

## <span data-ttu-id="6b90c-164">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6b90c-164">RELATED LINKS</span></span>

[<span data-ttu-id="6b90c-165">Verschieben-AzResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-165">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="6b90c-166">Neu – AzResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-166">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="6b90c-167">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-167">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="6b90c-168">Satz-AzResource</span><span class="sxs-lookup"><span data-stu-id="6b90c-168">Set-AzResource</span></span>](./Set-AzResource.md)
