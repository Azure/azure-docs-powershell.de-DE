---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94007982"
---
# <span data-ttu-id="87573-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="87573-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="87573-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="87573-102">SYNOPSIS</span></span>
<span data-ttu-id="87573-103">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="87573-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="87573-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="87573-104">SYNTAX</span></span>

### <span data-ttu-id="87573-105">NamespaceParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="87573-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87573-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="87573-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="87573-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="87573-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87573-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87573-108">DESCRIPTION</span></span>
<span data-ttu-id="87573-109">Das Set-AzEventHubNamespace-Cmdlet aktualisiert die Eigenschaften des angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="87573-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="87573-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="87573-110">EXAMPLES</span></span>

### <span data-ttu-id="87573-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="87573-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="87573-112">Aktualisiert die Tags für Namespace \` mynamespacename \` auf created.</span><span class="sxs-lookup"><span data-stu-id="87573-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="87573-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="87573-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="87573-114">Aktualisiert den Zustand des Namespace \` mynamespacename \` mit autopump = Enabled und MaximumThroughputUnits = 10.</span><span class="sxs-lookup"><span data-stu-id="87573-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="87573-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="87573-115">Example 3</span></span>

<span data-ttu-id="87573-116">Aktualisiert den angegebenen Event Hubs-Namespace.</span><span class="sxs-lookup"><span data-stu-id="87573-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="87573-117">automatisch</span><span class="sxs-lookup"><span data-stu-id="87573-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="87573-118">Beispiel 5: Erstellen und Aktualisieren von Namespace mit Verwalten der Identität in einem Cluster</span><span class="sxs-lookup"><span data-stu-id="87573-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :

# Get created namespace
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="87573-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="87573-119">PARAMETERS</span></span>

### <span data-ttu-id="87573-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87573-120">-DefaultProfile</span></span>
<span data-ttu-id="87573-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="87573-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87573-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="87573-122">-EnableAutoInflate</span></span>
<span data-ttu-id="87573-123">Gibt an, ob autopump aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="87573-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87573-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="87573-124">-EnableKafka</span></span>
<span data-ttu-id="87573-125">Aktivieren oder Deaktivieren von Kafka für Namespace</span><span class="sxs-lookup"><span data-stu-id="87573-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="87573-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="87573-126">-Identity</span></span>
<span data-ttu-id="87573-127">Aktivieren oder Deaktivieren der Identität für Namespace</span><span class="sxs-lookup"><span data-stu-id="87573-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="87573-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="87573-128">-IdentityUserDefined</span></span>
<span data-ttu-id="87573-129">Benutzerdefinierte Identität oder keine</span><span class="sxs-lookup"><span data-stu-id="87573-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87573-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="87573-130">-KeyProperty</span></span>
<span data-ttu-id="87573-131">Liste der wichtigsten Eigenschaften, @ (@ (keyName, KeyVaultUri, keyversion), @ (keyName, KeyVaultUri, keyversion))</span><span class="sxs-lookup"><span data-stu-id="87573-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87573-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="87573-132">-KeySource</span></span>
<span data-ttu-id="87573-133">Schlüsselquelle</span><span class="sxs-lookup"><span data-stu-id="87573-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87573-134">-Standort</span><span class="sxs-lookup"><span data-stu-id="87573-134">-Location</span></span>
<span data-ttu-id="87573-135">Speicherort des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="87573-135">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="87573-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="87573-137">Obergrenze von Durchsatz Einheiten wenn autopump aktiviert ist, sollte der Wert innerhalb von 0 bis 20 Durchsatz Einheiten liegen.</span><span class="sxs-lookup"><span data-stu-id="87573-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-138">-Name</span><span class="sxs-lookup"><span data-stu-id="87573-138">-Name</span></span>
<span data-ttu-id="87573-139">Name des EventHub-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="87573-139">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87573-140">-ResourceGroupName</span></span>
<span data-ttu-id="87573-141">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="87573-141">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="87573-142">-SkuCapacity</span></span>
<span data-ttu-id="87573-143">Die eventhub-Durchsatz Einheiten.</span><span class="sxs-lookup"><span data-stu-id="87573-143">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="87573-144">-SkuName</span></span>
<span data-ttu-id="87573-145">Namespace-SKU-Name.</span><span class="sxs-lookup"><span data-stu-id="87573-145">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-146">-Bundesland</span><span class="sxs-lookup"><span data-stu-id="87573-146">-State</span></span>
<span data-ttu-id="87573-147">Deaktivieren/Aktivieren von Namespace.</span><span class="sxs-lookup"><span data-stu-id="87573-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="87573-148">-Tag</span></span>
<span data-ttu-id="87573-149">Hashtables, die das Ressourcen-Tag darstellen.</span><span class="sxs-lookup"><span data-stu-id="87573-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="87573-150">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="87573-150">-Confirm</span></span>
<span data-ttu-id="87573-151">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="87573-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87573-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87573-152">-WhatIf</span></span>
<span data-ttu-id="87573-153">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="87573-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87573-154">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="87573-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87573-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87573-155">CommonParameters</span></span>
<span data-ttu-id="87573-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87573-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87573-157">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="87573-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87573-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="87573-158">INPUTS</span></span>

### <span data-ttu-id="87573-159">System. String</span><span class="sxs-lookup"><span data-stu-id="87573-159">System.String</span></span>

### <span data-ttu-id="87573-160">System. Nullable ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="87573-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="87573-161">System. Nullable ' 1 [[Microsoft. Azure. Commands. EventHub. Models. NamespaceState, Microsoft. Azure. PowerShell. Cmdlets. EventHub, Version = 1.4.3.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="87573-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="87573-162">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="87573-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="87573-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="87573-163">OUTPUTS</span></span>

### <span data-ttu-id="87573-164">Microsoft. Azure. Commands. EventHub. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="87573-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="87573-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="87573-165">NOTES</span></span>

## <span data-ttu-id="87573-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="87573-166">RELATED LINKS</span></span>
