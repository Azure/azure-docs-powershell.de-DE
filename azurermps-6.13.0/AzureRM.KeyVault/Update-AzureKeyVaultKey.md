---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/update-azurekeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Update-AzureKeyVaultKey.md
ms.openlocfilehash: e9e2401ab96da63c3fe6b5978916b96f98db9f54
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496026"
---
# <span data-ttu-id="c4c0f-101">Update-AzureKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c4c0f-101">Update-AzureKeyVaultKey</span></span>

## <span data-ttu-id="c4c0f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c4c0f-102">SYNOPSIS</span></span>
<span data-ttu-id="c4c0f-103">Aktualisiert die Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-103">Updates the attributes of a key in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c4c0f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c4c0f-104">SYNTAX</span></span>

### <span data-ttu-id="c4c0f-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="c4c0f-105">Default (Default)</span></span>
```
Update-AzureKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4c0f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="c4c0f-106">InputObject</span></span>
```
Update-AzureKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4c0f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c4c0f-107">DESCRIPTION</span></span>
<span data-ttu-id="c4c0f-108">Das Cmdlet **Update-AzureKeyVaultKey** aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-108">The **Update-AzureKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="c4c0f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c4c0f-109">EXAMPLES</span></span>

### <span data-ttu-id="c4c0f-110">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="c4c0f-110">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 7:59:02 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="c4c0f-111">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-111">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="c4c0f-112">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-112">That object specifies a time two years in the future.</span></span> <span data-ttu-id="c4c0f-113">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-113">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="c4c0f-114">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c4c0f-114">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="c4c0f-115">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-115">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="c4c0f-116">Der endgültige Befehl ändert einen Schlüssel mit dem Namen ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-116">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="c4c0f-117">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-117">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="c4c0f-118">Beispiel 2: Ändern einer Taste zum Löschen aller Kategorien</span><span class="sxs-lookup"><span data-stu-id="c4c0f-118">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzureKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

Vault Name     : Contoso
Name           : ITSoftware
Version        : 394f9379a47a4e2086585468de6c7ae5
Id             : https://Contoso.vault.azure.net:443/keys/ITSoftware/394f9379a47a4e2086585468de6c7ae5
Enabled        : True
Expires        : 5/25/2020 7:58:07 PM
Not Before     :
Created        : 4/6/2018 11:31:36 PM
Updated        : 5/25/2018 8:00:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="c4c0f-119">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels mit dem Namen ITSoftware gelöscht.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-119">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="c4c0f-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4c0f-120">PARAMETERS</span></span>

### <span data-ttu-id="c4c0f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4c0f-121">-DefaultProfile</span></span>
<span data-ttu-id="c4c0f-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4c0f-123">-Enable</span><span class="sxs-lookup"><span data-stu-id="c4c0f-123">-Enable</span></span>
<span data-ttu-id="c4c0f-124">Der Wert true aktiviert den Schlüssel und den Wert false.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-124">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="c4c0f-125">Wenn diese Option nicht angegeben ist, bleibt der vorhandene aktiviert/deaktivierte Status unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-125">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-126">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="c4c0f-126">-Expires</span></span>
<span data-ttu-id="c4c0f-127">Die Ablaufzeit eines Schlüssels in UTC-Zeit.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-127">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="c4c0f-128">Wenn Sie nicht angegeben wird, bleibt die vorhandene Ablaufzeit des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-128">If not specified, the existing expiration time of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c4c0f-129">-InputObject</span></span>
<span data-ttu-id="c4c0f-130">Key-Objekt</span><span class="sxs-lookup"><span data-stu-id="c4c0f-130">Key object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="c4c0f-131">-KeyOps</span></span>
<span data-ttu-id="c4c0f-132">Die Vorgänge, die mit dem Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-132">The operations that can be performed with the key.</span></span>
<span data-ttu-id="c4c0f-133">Wenn nicht angegeben, bleiben die vorhandenen Schlüsselvorgänge des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-133">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="c4c0f-134">-Name</span><span class="sxs-lookup"><span data-stu-id="c4c0f-134">-Name</span></span>
<span data-ttu-id="c4c0f-135">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-135">Key name.</span></span>
<span data-ttu-id="c4c0f-136">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung und Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-136">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

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

### <span data-ttu-id="c4c0f-137">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="c4c0f-137">-NotBefore</span></span>
<span data-ttu-id="c4c0f-138">Die UTC-Zeit, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-138">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="c4c0f-139">Wenn keine Angabe erfolgt, bleibt das vorhandene NotBefore-Attribut des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-139">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4c0f-140">-PassThru</span></span>
<span data-ttu-id="c4c0f-141">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-141">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c4c0f-142">Wenn dieser Schalter angegeben wird, wird das aktualisierte Schlüssel Bündel Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-142">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="c4c0f-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="c4c0f-143">-Tag</span></span>
<span data-ttu-id="c4c0f-144">Eine Hashtable stellt Schlüsselkategorien dar.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-144">A hashtable represents key tags.</span></span>
<span data-ttu-id="c4c0f-145">Wenn Sie nicht angegeben wird, bleiben die vorhandenen Tags des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-145">If not specified, the existings tags of the key remain unchanged.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-146">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="c4c0f-146">-VaultName</span></span>
<span data-ttu-id="c4c0f-147">Vault-Name.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-147">Vault name.</span></span>
<span data-ttu-id="c4c0f-148">Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-148">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="c4c0f-149">-Version</span><span class="sxs-lookup"><span data-stu-id="c4c0f-149">-Version</span></span>
<span data-ttu-id="c4c0f-150">Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-150">Key version.</span></span>
<span data-ttu-id="c4c0f-151">Cmdlet erstellt den FQDN eines Schlüssels aus Vault-Name, aktuell ausgewählter Umgebung, Schlüsselname und Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-151">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c4c0f-152">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c4c0f-152">-Confirm</span></span>
<span data-ttu-id="c4c0f-153">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4c0f-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4c0f-154">-WhatIf</span></span>
<span data-ttu-id="c4c0f-155">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4c0f-156">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4c0f-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4c0f-157">CommonParameters</span></span>
<span data-ttu-id="c4c0f-158">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4c0f-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4c0f-159">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c4c0f-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4c0f-160">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c4c0f-160">INPUTS</span></span>

### <span data-ttu-id="c4c0f-161">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c4c0f-161">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>
<span data-ttu-id="c4c0f-162">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c4c0f-162">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="c4c0f-163">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c4c0f-163">OUTPUTS</span></span>

### <span data-ttu-id="c4c0f-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c4c0f-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="c4c0f-165">Notizen</span><span class="sxs-lookup"><span data-stu-id="c4c0f-165">NOTES</span></span>

## <span data-ttu-id="c4c0f-166">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c4c0f-166">RELATED LINKS</span></span>
