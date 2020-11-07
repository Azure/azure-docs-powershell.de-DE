---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: d79c28b09c9f6ca36ae163566574555bb3c50459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664050"
---
# <span data-ttu-id="f3d1e-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="f3d1e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f3d1e-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d1e-103">Ruft Schlüsseldepots ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3d1e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f3d1e-104">SYNTAX</span></span>

### <span data-ttu-id="f3d1e-105">ListAllVaultsInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3d1e-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d1e-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="f3d1e-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d1e-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3d1e-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="f3d1e-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3d1e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3d1e-109">DESCRIPTION</span></span>
<span data-ttu-id="f3d1e-110">Das Cmdlet " **Get-AzureRmKeyVault** " Ruft Informationen zu den Schlüsseldepots in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="f3d1e-111">Sie können alle wichtigen Vaults-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten schlüsseltresor filtern.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>
<span data-ttu-id="f3d1e-112">Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie einen einzelnen schlüsseltresor erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="f3d1e-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f3d1e-113">EXAMPLES</span></span>

### <span data-ttu-id="f3d1e-114">Beispiel 1: Abrufen aller Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3d1e-114">Example 1: Get all key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault

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

<span data-ttu-id="f3d1e-115">Dieser Befehl ruft alle Schlüsseldepots Ihres aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="f3d1e-116">Beispiel 2: Abrufen eines bestimmten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="f3d1e-116">Example 2: Get a specific key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault'

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

<span data-ttu-id="f3d1e-117">Dieser Befehl ruft den schlüsseltresor mit dem Namen myvault in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-117">This command gets the key vault named myvault in your current subscription.</span></span>

### <span data-ttu-id="f3d1e-118">Beispiel 3: Abrufen von Schlüsseldepots in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="f3d1e-118">Example 3: Get key vaults in a resource group</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -ResourceGroupName 'myrg1'

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

<span data-ttu-id="f3d1e-119">Dieser Befehl ruft alle Schlüsseldepots in der Ressourcengruppe mit dem Namen ContosoPayRollResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-119">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="f3d1e-120">Beispiel 4: Abrufen aller gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3d1e-120">Example 4: Get all deleted key vaults in your current subscription</span></span>
```powershell
PS C:\> Get-AzureRmKeyVault -InRemovedState

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

<span data-ttu-id="f3d1e-121">Dieser Befehl ruft alle gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-121">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="f3d1e-122">Beispiel 5: Abrufen eines gelöschten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="f3d1e-122">Example 5: Get a deleted key vault</span></span>
```powershell
PS C:\> Get-AzureRMKeyVault -VaultName 'myvault4'  -Location 'westus' -InRemovedState

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

<span data-ttu-id="f3d1e-123">Dieser Befehl ruft die gelöschten Schlüssel Vault-Informationen mit dem Namen myvault4 in Ihrem aktuellen Abonnement und in der Region westus ab.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-123">This command gets the deleted key vault information named myvault4 in your current subscription and in westus region.</span></span>

## <span data-ttu-id="f3d1e-124">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3d1e-124">PARAMETERS</span></span>

### <span data-ttu-id="f3d1e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d1e-125">-DefaultProfile</span></span>
<span data-ttu-id="f3d1e-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f3d1e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1e-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="f3d1e-127">-InRemovedState</span></span>
<span data-ttu-id="f3d1e-128">Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="f3d1e-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="f3d1e-129">-Location</span></span>
<span data-ttu-id="f3d1e-130">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-130">The location of the deleted vault.</span></span>

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

### <span data-ttu-id="f3d1e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3d1e-131">-ResourceGroupName</span></span>
<span data-ttu-id="f3d1e-132">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor oder den Schlüsseldepots zugeordnet ist, die abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1e-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="f3d1e-133">-Tag</span></span>
<span data-ttu-id="f3d1e-134">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="f3d1e-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f3d1e-135">Beispiel: @ {Key0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="f3d1e-135">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1e-136">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="f3d1e-136">-VaultName</span></span>
<span data-ttu-id="f3d1e-137">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-137">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d1e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d1e-138">CommonParameters</span></span>
<span data-ttu-id="f3d1e-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d1e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d1e-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d1e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d1e-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f3d1e-141">INPUTS</span></span>

### <span data-ttu-id="f3d1e-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d1e-142">System.String</span></span>

### <span data-ttu-id="f3d1e-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f3d1e-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f3d1e-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f3d1e-144">OUTPUTS</span></span>

### <span data-ttu-id="f3d1e-145">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="f3d1e-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="f3d1e-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="f3d1e-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="f3d1e-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="f3d1e-148">NOTES</span></span>

## <span data-ttu-id="f3d1e-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f3d1e-149">RELATED LINKS</span></span>

[<span data-ttu-id="f3d1e-150">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-150">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="f3d1e-151">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="f3d1e-151">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
