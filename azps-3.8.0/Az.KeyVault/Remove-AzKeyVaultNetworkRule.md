---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultNetworkRule.md
ms.openlocfilehash: b1c0326be98efed91ce53c9cf04cdee6fce658f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996336"
---
# <span data-ttu-id="0bddc-101">Remove-AzKeyVaultNetworkRule</span><span class="sxs-lookup"><span data-stu-id="0bddc-101">Remove-AzKeyVaultNetworkRule</span></span>

## <span data-ttu-id="0bddc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0bddc-102">SYNOPSIS</span></span>
<span data-ttu-id="0bddc-103">Entfernt eine Netzwerkregel aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0bddc-103">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="0bddc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0bddc-104">SYNTAX</span></span>

### <span data-ttu-id="0bddc-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="0bddc-105">ByVaultName (Default)</span></span>
```
Remove-AzKeyVaultNetworkRule [-VaultName] <String> [[-ResourceGroupName] <String>] [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bddc-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="0bddc-106">ByInputObject</span></span>
```
Remove-AzKeyVaultNetworkRule [-InputObject] <PSKeyVault> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bddc-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0bddc-107">ByResourceId</span></span>
```
Remove-AzKeyVaultNetworkRule [-ResourceId] <String> [-IpAddressRange <String[]>]
 [-VirtualNetworkResourceId <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bddc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0bddc-108">DESCRIPTION</span></span>
<span data-ttu-id="0bddc-109">Entfernt eine Netzwerkregel aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="0bddc-109">Removes a network rule from a key vault.</span></span>

## <span data-ttu-id="0bddc-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0bddc-110">EXAMPLES</span></span>

### <span data-ttu-id="0bddc-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0bddc-111">Example 1</span></span>
```powershell
PS C:\> $myNetworkResId = (Get-AzVirtualNetwork -Name myVNetName -ResourceGroupName myRG).Subnets[0].Id
PS C:\> Remove-AzKeyVaultNetworkRule -VaultName myVault -IpAddressRange "10.0.0.1/26" -VirtualNetworkResourceId $myNetworkResId -PassThru

Vault Name                       : myVault
Resource Group Name              : myrg
Location                         : West US
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/myvault
Vault URI                        : https://myvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
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
                                   setissuers, recover, backup, restore
                                   Permissions to (Key Vault Managed) Storage : delete, deletesas, get, getsas, list,
                                   listsas, regeneratekey, set, setsas, update, recover, backup, restore


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="0bddc-112">Mit diesem Befehl wird eine Netzwerkregel aus dem angegebenen Tresor entfernt, vorausgesetzt, es wird eine Regel gefunden, die der angegebenen IP-Adresse und dem virtuellen Netzwerk-Ressourcenbezeichner entspricht.</span><span class="sxs-lookup"><span data-stu-id="0bddc-112">This command removes a network rule from the specified vault, provided a rule is found matching the specified IP address and the virtual network resource identifier.</span></span>

## <span data-ttu-id="0bddc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="0bddc-113">PARAMETERS</span></span>

### <span data-ttu-id="0bddc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bddc-114">-DefaultProfile</span></span>
<span data-ttu-id="0bddc-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0bddc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0bddc-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0bddc-116">-InputObject</span></span>
<span data-ttu-id="0bddc-117">Keyvault-Objekt</span><span class="sxs-lookup"><span data-stu-id="0bddc-117">KeyVault object</span></span>

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

### <span data-ttu-id="0bddc-118">-IpAddressRange</span><span class="sxs-lookup"><span data-stu-id="0bddc-118">-IpAddressRange</span></span>
<span data-ttu-id="0bddc-119">Gibt den zulässigen Netzwerk-IP-Adressbereich der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="0bddc-119">Specifies allowed network IP address range of network rule.</span></span>

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

### <span data-ttu-id="0bddc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0bddc-120">-PassThru</span></span>
<span data-ttu-id="0bddc-121">Dieses Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="0bddc-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="0bddc-122">Wenn dieser Schalter angegeben wird, wird das aktualisierte schlüsseltresor-Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0bddc-122">If this switch is specified, it returns the updated key vault object.</span></span>

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

### <span data-ttu-id="0bddc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bddc-123">-ResourceGroupName</span></span>
<span data-ttu-id="0bddc-124">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor zugeordnet ist, dessen Netzwerkregel geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bddc-124">Specifies the name of the resource group associated with the key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="0bddc-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0bddc-125">-ResourceId</span></span>
<span data-ttu-id="0bddc-126">Keyvault-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0bddc-126">KeyVault Resource Id</span></span>

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

### <span data-ttu-id="0bddc-127">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="0bddc-127">-VaultName</span></span>
<span data-ttu-id="0bddc-128">Gibt den Namen eines Schlüsseldepots an, dessen Netzwerkregel geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0bddc-128">Specifies the name of a key vault whose network rule is being modified.</span></span>

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

### <span data-ttu-id="0bddc-129">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="0bddc-129">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="0bddc-130">Gibt den zulässigen virtuellen Netzwerk-Ressourcenbezeichner der Netzwerkregel an.</span><span class="sxs-lookup"><span data-stu-id="0bddc-130">Specifies allowed virtual network resource identifier of network rule.</span></span>

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

### <span data-ttu-id="0bddc-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0bddc-131">-Confirm</span></span>
<span data-ttu-id="0bddc-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0bddc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bddc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bddc-133">-WhatIf</span></span>
<span data-ttu-id="0bddc-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0bddc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0bddc-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0bddc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bddc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bddc-136">CommonParameters</span></span>
<span data-ttu-id="0bddc-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0bddc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bddc-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0bddc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bddc-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0bddc-139">INPUTS</span></span>

### <span data-ttu-id="0bddc-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0bddc-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="0bddc-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0bddc-141">System.String</span></span>

## <span data-ttu-id="0bddc-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0bddc-142">OUTPUTS</span></span>

### <span data-ttu-id="0bddc-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="0bddc-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="0bddc-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="0bddc-144">NOTES</span></span>

## <span data-ttu-id="0bddc-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0bddc-145">RELATED LINKS</span></span>
