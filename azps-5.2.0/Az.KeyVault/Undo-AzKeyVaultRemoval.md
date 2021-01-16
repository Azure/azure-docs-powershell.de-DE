---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azkeyvaultremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzKeyVaultRemoval.md
ms.openlocfilehash: 98a3a023564c2c61f1398856e8a089276aeae7bc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98295264"
---
# <span data-ttu-id="591b0-101">Undo-AzKeyVaultRemoval</span><span class="sxs-lookup"><span data-stu-id="591b0-101">Undo-AzKeyVaultRemoval</span></span>

## <span data-ttu-id="591b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="591b0-102">SYNOPSIS</span></span>
<span data-ttu-id="591b0-103">Stellt einen gelöschten Schlüsseltresor in einen aktiven Zustand wiederher.</span><span class="sxs-lookup"><span data-stu-id="591b0-103">Recovers a deleted key vault into an active state.</span></span>

## <span data-ttu-id="591b0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="591b0-104">SYNTAX</span></span>

### <span data-ttu-id="591b0-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="591b0-105">Default (Default)</span></span>
```
Undo-AzKeyVaultRemoval [-VaultName] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="591b0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="591b0-106">InputObject</span></span>
```
Undo-AzKeyVaultRemoval [-InputObject] <PSDeletedKeyVault> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="591b0-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="591b0-107">DESCRIPTION</span></span>
<span data-ttu-id="591b0-108">Das **Cmdlet "Undo-AzKeyVaultRemoval"** stellt einen zuvor gelöschten Schlüsseltresor wiederher.</span><span class="sxs-lookup"><span data-stu-id="591b0-108">The **Undo-AzKeyVaultRemoval** cmdlet will recover a previously deleted key vault.</span></span> <span data-ttu-id="591b0-109">Der wiederhergestellte Tresor ist nach der Wiederherstellung aktiv.</span><span class="sxs-lookup"><span data-stu-id="591b0-109">The recovered vault will be active after recovery</span></span>

## <span data-ttu-id="591b0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="591b0-110">EXAMPLES</span></span>

### <span data-ttu-id="591b0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="591b0-111">Example 1</span></span>
```powershell
PS C:\> Undo-AzKeyVaultRemoval -VaultName 'MyKeyVault' -ResourceGroupName 'MyResourceGroup' -Location 'eastus2' -Tag @{"x"= "y"}

Vault Name                       : MyKeyVault
Resource Group Name              : MyResourceGroup
Location                         : eastus2
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers
                                   /Microsoft.KeyVault/vaults/mykeyvault
Vault URI                        : https://mykeyvault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : True
Enabled For Disk Encryption?     : True
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
                                   Name  Value
                                   ====  =====
                                   x     y
```

<span data-ttu-id="591b0-112">Mit diesem Befehl wird der Schlüsseltresor "MyKeyVault" wiederhergestellt, der zuvor aus der Region "eastus2" und der Ressourcengruppe "MyResourceGroup" gelöscht wurde, in einen aktiven und verwendbaren Zustand.</span><span class="sxs-lookup"><span data-stu-id="591b0-112">This command will recover the key vault 'MyKeyVault' that was previously deleted from eastus2 region and 'MyResourceGroup' resource group, into an active and usable state.</span></span> <span data-ttu-id="591b0-113">Außerdem werden die Tags durch ein neues Tag ersetzt.</span><span class="sxs-lookup"><span data-stu-id="591b0-113">It also replaces the tags with new tag.</span></span>

## <span data-ttu-id="591b0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="591b0-114">PARAMETERS</span></span>

### <span data-ttu-id="591b0-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="591b0-115">-DefaultProfile</span></span>
<span data-ttu-id="591b0-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="591b0-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="591b0-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="591b0-117">-InputObject</span></span>
<span data-ttu-id="591b0-118">Gelöschtes Tresorobjekt</span><span class="sxs-lookup"><span data-stu-id="591b0-118">Deleted vault object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="591b0-119">-Location</span><span class="sxs-lookup"><span data-stu-id="591b0-119">-Location</span></span>
<span data-ttu-id="591b0-120">Gibt den gelöschten Tresor an, der in der ursprünglichen Region von Azure gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="591b0-120">Specifies the deleted vault original Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="591b0-121">-ResourceGroupName</span></span>
<span data-ttu-id="591b0-122">Gibt den Namen einer vorhandenen Ressourcengruppe an, in der der Schlüsseltresor erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="591b0-122">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b0-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="591b0-123">-Tag</span></span>
<span data-ttu-id="591b0-124">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="591b0-124">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="591b0-125">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="591b0-125">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b0-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="591b0-126">-VaultName</span></span>
<span data-ttu-id="591b0-127">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="591b0-127">Vault name.</span></span>
<span data-ttu-id="591b0-128">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="591b0-128">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="591b0-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="591b0-129">-Confirm</span></span>
<span data-ttu-id="591b0-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="591b0-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="591b0-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="591b0-131">-WhatIf</span></span>
<span data-ttu-id="591b0-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="591b0-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="591b0-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="591b0-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="591b0-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="591b0-134">CommonParameters</span></span>
<span data-ttu-id="591b0-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="591b0-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="591b0-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="591b0-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="591b0-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="591b0-137">INPUTS</span></span>

### <span data-ttu-id="591b0-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b0-138">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

## <span data-ttu-id="591b0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="591b0-139">OUTPUTS</span></span>

### <span data-ttu-id="591b0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b0-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="591b0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="591b0-141">NOTES</span></span>

## <span data-ttu-id="591b0-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="591b0-142">RELATED LINKS</span></span>

[<span data-ttu-id="591b0-143">Remove-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b0-143">Remove-AzKeyVault</span></span>](./Remove-AzKeyVault.md)

[<span data-ttu-id="591b0-144">New-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b0-144">New-AzKeyVault</span></span>](./New-AzKeyVault.md)

[<span data-ttu-id="591b0-145">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="591b0-145">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)
