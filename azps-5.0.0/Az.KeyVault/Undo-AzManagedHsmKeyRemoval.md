---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/undo-azmanagedhsmkeyremoval
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Undo-AzManagedHsmKeyRemoval.md
ms.openlocfilehash: be1713584a1d0ce897c1c728f6aa7ae8b6ca3255
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94175486"
---
# <span data-ttu-id="ac8a9-101">Undo-AzManagedHsmKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="ac8a9-101">Undo-AzManagedHsmKeyRemoval</span></span>

## <span data-ttu-id="ac8a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8a9-103">Stellt einen gelöschten Schlüssel in einem verwalteten HSM in einen aktiven Zustand.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-103">Recovers a deleted key in a managed HSM into an active state.</span></span>

## <span data-ttu-id="ac8a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac8a9-104">SYNTAX</span></span>

### <span data-ttu-id="ac8a9-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac8a9-105">Default (Default)</span></span>
```
Undo-AzManagedHsmKeyRemoval [-HsmName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac8a9-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="ac8a9-106">InputObject</span></span>
```
Undo-AzManagedHsmKeyRemoval [-InputObject] <PSDeletedKeyVaultKeyIdentityItem>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac8a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8a9-108">Mit dem Cmdlet **"Undo-AzManagedHsmKeyRemoval"** wird ein zuvor gelöschter Schlüssel wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-108">The **Undo-AzManagedHsmKeyRemoval** cmdlet will recover a previously deleted key.</span></span>
<span data-ttu-id="ac8a9-109">Der wiederhergestellte Schlüssel ist aktiv und kann für alle normalen Schlüsselvorgänge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-109">The recovered key will be active and can be used for all normal key operations.</span></span>
<span data-ttu-id="ac8a9-110">Der Aufrufer muss über die Berechtigung "Wiederherstellen" verfügen, um diesen Vorgang ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-110">Caller needs to have 'recover' permission in order to perform this operation.</span></span>

## <span data-ttu-id="ac8a9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac8a9-111">EXAMPLES</span></span>

### <span data-ttu-id="ac8a9-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac8a9-112">Example 1</span></span>
```powershell
PS C:\> Undo-AzManagedHsmKeyRemoval -HsmName testmhsm -Name testkey001

Vault/HSM Name : testmhsm
Name           : testkey001
Version        : 7cff8510da04433b98144a3e33ad2bae
Id             : https://testmhsm.managedhsm.azure.net:443/keys/testkey001/7cff8510da04433b98144a3e33ad2bae
Enabled        : True
Expires        :
Not Before     :
Created        : 10/14/2020 10:13:03 AM
Updated        : 10/14/2020 10:13:03 AM
Recovery Level : Recoverable+Purgeable
Tags           :
```

<span data-ttu-id="ac8a9-113">Mit diesem Befehl wird der zuvor gelöschte Schlüssel "testkey001" wieder in einen aktiven und nutzbaren Zustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-113">This command will recover the key 'testkey001' that was previously deleted, into an active and usable state.</span></span>

## <span data-ttu-id="ac8a9-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac8a9-114">PARAMETERS</span></span>

### <span data-ttu-id="ac8a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8a9-115">-DefaultProfile</span></span>
<span data-ttu-id="ac8a9-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac8a9-117">-HsmName</span><span class="sxs-lookup"><span data-stu-id="ac8a9-117">-HsmName</span></span>
<span data-ttu-id="ac8a9-118">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-118">HSM name.</span></span> <span data-ttu-id="ac8a9-119">Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-119">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="ac8a9-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac8a9-120">-InputObject</span></span>
<span data-ttu-id="ac8a9-121">Gelöschtes Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="ac8a9-121">Deleted key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ac8a9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ac8a9-122">-Name</span></span>
<span data-ttu-id="ac8a9-123">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-123">Key name.</span></span>
<span data-ttu-id="ac8a9-124">Cmdlet erstellt den FQDN eines Schlüssels aus verwaltetem HSM-Namen, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-124">Cmdlet constructs the FQDN of a key from managed HSM name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8a9-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac8a9-125">-Confirm</span></span>
<span data-ttu-id="ac8a9-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac8a9-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac8a9-127">-WhatIf</span></span>
<span data-ttu-id="ac8a9-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac8a9-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac8a9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8a9-130">CommonParameters</span></span>
<span data-ttu-id="ac8a9-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8a9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8a9-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac8a9-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8a9-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac8a9-133">INPUTS</span></span>

### <span data-ttu-id="ac8a9-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="ac8a9-134">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="ac8a9-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac8a9-135">OUTPUTS</span></span>

### <span data-ttu-id="ac8a9-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="ac8a9-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac8a9-137">NOTES</span></span>

## <span data-ttu-id="ac8a9-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac8a9-138">RELATED LINKS</span></span>

[<span data-ttu-id="ac8a9-139">Add-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-139">Add-AzManagedHsmKey</span></span>](./Add-AzManagedHsmKey.md)

[<span data-ttu-id="ac8a9-140">Backup-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-140">Backup-AzManagedHsmKey</span></span>](./Backup-AzManagedHsmKey.md)

[<span data-ttu-id="ac8a9-141">Remove-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-141">Remove-AzManagedHsmKey</span></span>](./Remove-AzManagedHsmKey.md)

[<span data-ttu-id="ac8a9-142">Wiederherstellen – AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-142">Restore-AzManagedHsmKey</span></span>](./Restore-AzManagedHsmKey.md)

[<span data-ttu-id="ac8a9-143">Get-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-143">Get-AzManagedHsmKey</span></span>](./Get-AzManagedHsmKey.md)

[<span data-ttu-id="ac8a9-144">Update-AzManagedHsmKey</span><span class="sxs-lookup"><span data-stu-id="ac8a9-144">Update-AzManagedHsmKey</span></span>](./Update-AzManagedHsmKey.md)