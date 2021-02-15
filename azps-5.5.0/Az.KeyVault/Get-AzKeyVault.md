---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVault.md
ms.openlocfilehash: 37ed0c0cb29e69aa2e8018bb193fa4c82b0c3bcb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159633"
---
# <span data-ttu-id="83af3-101">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="83af3-101">Get-AzKeyVault</span></span>

## <span data-ttu-id="83af3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83af3-102">SYNOPSIS</span></span>
<span data-ttu-id="83af3-103">Ruft wichtige Tresore ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-103">Gets key vaults.</span></span>

## <span data-ttu-id="83af3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="83af3-104">SYNTAX</span></span>

### <span data-ttu-id="83af3-105">GetVaultByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="83af3-105">GetVaultByName (Default)</span></span>
```
Get-AzKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83af3-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="83af3-106">ByDeletedVault</span></span>
```
Get-AzKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="83af3-107">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="83af3-107">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83af3-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="83af3-108">DESCRIPTION</span></span>
<span data-ttu-id="83af3-109">Das **Get-AzKeyVault-Cmdlet** ruft Informationen zu den wichtigsten Tresoren in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-109">The **Get-AzKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="83af3-110">Sie können alle Schlüsseltresorinstanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten Schlüsseltresor filtern.</span><span class="sxs-lookup"><span data-stu-id="83af3-110">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="83af3-111">Beachten Sie: Obwohl die Angabe der Ressourcengruppe für dieses Cmdlet optional ist, wenn Sie einen einzelnen Schlüsseltresor erhalten, sollten Sie dies zur Leistungssteigerung tun.</span><span class="sxs-lookup"><span data-stu-id="83af3-111">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="83af3-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="83af3-112">EXAMPLES</span></span>

### <span data-ttu-id="83af3-113">Beispiel 1: Alle wichtigen Tresore in Ihrem aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="83af3-113">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault

Vault Name          : myvault1
Resource Group Name : myrg
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.Ke
                      yVault/vaults/myvault1
Tags                :


Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="83af3-114">Dieser Befehl ruft alle wichtigen Tresore in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-114">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="83af3-115">Beispiel 2: Einen bestimmten Schlüsseltresor erhalten</span><span class="sxs-lookup"><span data-stu-id="83af3-115">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault'

Vault Name                       : myvault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
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

Tags                             :
```

<span data-ttu-id="83af3-116">Dieser Befehl ruft den Schlüsseltresor namens "myvault" in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-116">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="83af3-117">Beispiel 3: Erhalten von Schlüsseltresorn in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="83af3-117">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVault -ResourceGroupName 'myrg1'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="83af3-118">Dieser Befehl ruft alle Schlüsseltresor in der Ressourcengruppe namens "ContosoPayRollResourceGroup" ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-118">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="83af3-119">Beispiel 4: Alle gelöschten Schlüsseltresor in Ihrem aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="83af3-119">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVault -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="83af3-120">Dieser Befehl ruft alle gelöschten Schlüsseltresor in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-120">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="83af3-121">Beispiel 5: Einen gelöschten Schlüsseltresor erhalten</span><span class="sxs-lookup"><span data-stu-id="83af3-121">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

Vault Name           : myvault4
Location             : westus
Id                   : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/providers/Microsoft.KeyVault/locations/westu
                       s/deletedVaults/myvault4
Resource ID          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers/Microsoft.K
                       eyVault/vaults/myvault4
Deletion Date        : 5/24/2018 9:33:24 PM
Scheduled Purge Date : 8/22/2018 9:33:24 PM
Tags                 :
```

<span data-ttu-id="83af3-122">Dieser Befehl ruft die gelöschten Schlüsseltresorinformationen namens "myvault4" in Ihrem aktuellen Abonnement und in der Region "Westus" ab.</span><span class="sxs-lookup"><span data-stu-id="83af3-122">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

### <span data-ttu-id="83af3-123">Beispiel 6: Erhalten von Schlüsseltresorn mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="83af3-123">Example 6: Get key vaults using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName 'myvault*'

Vault Name          : myvault2
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault2
Tags                :

Vault Name          : myvault3
Resource Group Name : myrg1
Location            : westus
Resource ID         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg1/providers/Microsoft.Ke
                      yVault/vaults/myvault3
Tags                :
```

<span data-ttu-id="83af3-124">Dieser Befehl ruft alle wichtigen Tresore im Abonnement ab, die mit "myvault" beginnen.</span><span class="sxs-lookup"><span data-stu-id="83af3-124">This command gets all the key vaults in the subscription that start with "myvault".</span></span>

## <span data-ttu-id="83af3-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83af3-125">PARAMETERS</span></span>

### <span data-ttu-id="83af3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83af3-126">-DefaultProfile</span></span>
<span data-ttu-id="83af3-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="83af3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="83af3-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="83af3-128">-InRemovedState</span></span>
<span data-ttu-id="83af3-129">Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="83af3-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="83af3-130">-Location</span><span class="sxs-lookup"><span data-stu-id="83af3-130">-Location</span></span>
<span data-ttu-id="83af3-131">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="83af3-131">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83af3-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83af3-132">-ResourceGroupName</span></span>
<span data-ttu-id="83af3-133">Gibt den Namen der Ressourcengruppe an, die dem abgefragten Schlüsseltresor oder Schlüsseltresor zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="83af3-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="83af3-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="83af3-134">-Tag</span></span>
<span data-ttu-id="83af3-135">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="83af3-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="83af3-136">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="83af3-136">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="83af3-137">-VaultName</span><span class="sxs-lookup"><span data-stu-id="83af3-137">-VaultName</span></span>
<span data-ttu-id="83af3-138">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="83af3-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="83af3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83af3-139">CommonParameters</span></span>
<span data-ttu-id="83af3-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83af3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83af3-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83af3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83af3-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="83af3-142">INPUTS</span></span>

### <span data-ttu-id="83af3-143">System.String</span><span class="sxs-lookup"><span data-stu-id="83af3-143">System.String</span></span>

### <span data-ttu-id="83af3-144">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="83af3-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="83af3-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="83af3-145">OUTPUTS</span></span>

### <span data-ttu-id="83af3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="83af3-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="83af3-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="83af3-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="83af3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="83af3-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="83af3-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="83af3-149">NOTES</span></span>

## <span data-ttu-id="83af3-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="83af3-150">RELATED LINKS</span></span>

[<span data-ttu-id="83af3-151">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="83af3-151">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="83af3-152">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="83af3-152">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)
