---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultNetworkRule.md
ms.openlocfilehash: c437611603bab6b2c4b9fff5cd0696e306182afa
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472373"
---
# <span data-ttu-id="85db8-101">Add-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="85db8-101">Add-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="85db8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85db8-102">SYNOPSIS</span></span>
<span data-ttu-id="85db8-103">Fügt eine Regel hinzu, die den Zugriff auf einen Schlüsseltresor basierend auf der Internetadresse des Clients einschränken soll.</span><span class="sxs-lookup"><span data-stu-id="85db8-103">Adds a rule meant to restrict access to a key vault based on the client's internet address.</span></span>

## <span data-ttu-id="85db8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85db8-104">SYNTAX</span></span>

### <span data-ttu-id="85db8-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="85db8-105">ByVaultName (Default)</span></span>
```
Add-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85db8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85db8-106">ByInputObject</span></span>
```
Add-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="85db8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="85db8-107">ByResourceId</span></span>
```
Add-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85db8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85db8-108">DESCRIPTION</span></span>
<span data-ttu-id="85db8-109">Das **Cmdlet "Add-AzKeyVaultNetworkRule"** gewährt oder schränkt den Zugriff auf einen Schlüsseltresor auf eine Reihe von Anrufern ein, die von deren IP-Adressen oder dem virtuellen Netzwerk bestimmt werden, zu dem sie gehören.</span><span class="sxs-lookup"><span data-stu-id="85db8-109">The **Add-AzKeyVaultNetworkRule** cmdlet grants or restricts access to a key vault to a set of caller designated by their IP addresses or the virtual network to which they belong.</span></span> <span data-ttu-id="85db8-110">Die Regel kann den Zugriff für andere Benutzer, Anwendungen oder Sicherheitsgruppen einschränken, denen berechtigungen über die Zugriffsrichtlinie erteilt wurden.</span><span class="sxs-lookup"><span data-stu-id="85db8-110">The rule has the potential to restrict access for other users, applications, or security groups which have been granted permissions via the access policy.</span></span>

<span data-ttu-id="85db8-111">Beachten Sie, dass netzwerkregeln nicht über einen beliebigen ip-Bereich `10.0.0.0-10.255.255.255` (private IP-Adressen) hinzugefügt werden können.</span><span class="sxs-lookup"><span data-stu-id="85db8-111">Please note that any IP range inside `10.0.0.0-10.255.255.255` (private IP addresses) cannot be used to add network rules.</span></span>

## <span data-ttu-id="85db8-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85db8-112">EXAMPLES</span></span>

### <span data-ttu-id="85db8-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="85db8-113">Example 1</span></span>
```powershell
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24" -ServiceEndpoint Microsoft.KeyVault 
PS C:\> $virtualNetwork = New-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG -Location westus -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNet -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Add-AzKeyVaultNetworkRule -VaultName myvault -IpAddressRange "10.0.1.0/24" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myvault
Resource Group Name              : myRG
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myRG/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : get, create, delete, list, update,
                                   import, backup, restore, recover
                                   Permissions to Secrets                     : get, list, set, delete, backup,
                                   restore, recover
                                   Permissions to Certificates                : get, delete, list, create, import,
                                   update, deleteissuers, getissuers, listissuers, managecontacts, manageissuers,
                                   setissuers, recover
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   : 10.0.1.0/24
                                   Virtual Network Rules                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-
                                   xxxxxxxxxxxxx/resourcegroups/myRG/providers/microsoft.network/virtualnetworks/myvn
                                   et/subnets/frontendsubnet

Tags                             :
```

<span data-ttu-id="85db8-114">Dieser Befehl fügt dem angegebenen Tresor eine Netzwerkregel hinzu und ermöglicht so den Zugriff auf die angegebene IP-Adresse aus dem virtuellen Netzwerk, das von der $myNetworkResId.</span><span class="sxs-lookup"><span data-stu-id="85db8-114">This command adds a network rule to the specified vault, allowing access to the specified IP address from the virtual network identified by $myNetworkResId.</span></span>

## <span data-ttu-id="85db8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85db8-115">PARAMETERS</span></span>

### <span data-ttu-id="85db8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85db8-116">-DefaultProfile</span></span>
<span data-ttu-id="85db8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85db8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85db8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85db8-118">-InputObject</span></span>
<span data-ttu-id="85db8-119">KeyVault-Objekt</span><span class="sxs-lookup"><span data-stu-id="85db8-119">KeyVault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="85db8-120">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="85db8-120">-IpAddressRange</span></span>
<span data-ttu-id="85db8-121">Gibt den zulässigen Netzwerk-IP-Adressbereich einer Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="85db8-121">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="85db8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="85db8-122">-PassThru</span></span>
<span data-ttu-id="85db8-123">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="85db8-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="85db8-124">Wenn dieser Schalter angegeben ist, wird das aktualisierte Schlüsseltresorobjekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="85db8-124">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="85db8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85db8-125">-ResourceGroupName</span></span>
<span data-ttu-id="85db8-126">Gibt den Namen der Ressourcengruppe an, die dem Schlüsseltresor zugeordnet ist, dessen Netzwerkregel geändert wird.</span><span class="sxs-lookup"><span data-stu-id="85db8-126">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85db8-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="85db8-127">-ResourceId</span></span>
<span data-ttu-id="85db8-128">KeyVault Resource Id</span><span class="sxs-lookup"><span data-stu-id="85db8-128">KeyVault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85db8-129">-VaultName</span><span class="sxs-lookup"><span data-stu-id="85db8-129">-VaultName</span></span>
<span data-ttu-id="85db8-130">Gibt den Namen eines Schlüsseltresor an, dessen Netzwerkregel geändert wird.</span><span class="sxs-lookup"><span data-stu-id="85db8-130">Specifies the name of a key vault whose network rule is being modified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85db8-131">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="85db8-131">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="85db8-132">Gibt die zulässige virtuelle Netzwerkressourcen-ID der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="85db8-132">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="85db8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="85db8-133">-Confirm</span></span>
<span data-ttu-id="85db8-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="85db8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85db8-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="85db8-135">-WhatIf</span></span>
<span data-ttu-id="85db8-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85db8-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85db8-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="85db8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85db8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85db8-138">CommonParameters</span></span>
<span data-ttu-id="85db8-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85db8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85db8-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85db8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85db8-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85db8-141">INPUTS</span></span>

### <span data-ttu-id="85db8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="85db8-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="85db8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="85db8-143">System.String</span></span>

## <span data-ttu-id="85db8-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85db8-144">OUTPUTS</span></span>

### <span data-ttu-id="85db8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="85db8-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="85db8-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85db8-146">NOTES</span></span>

## <span data-ttu-id="85db8-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85db8-147">RELATED LINKS</span></span>
