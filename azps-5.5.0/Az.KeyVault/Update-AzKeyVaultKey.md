---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVaultKey.md
ms.openlocfilehash: de8e542079cdeebdb6513c8e0febf8cfe0952889
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100152633"
---
# <span data-ttu-id="b0418-101">Update-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b0418-101">Update-AzKeyVaultKey</span></span>

## <span data-ttu-id="b0418-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0418-102">SYNOPSIS</span></span>
<span data-ttu-id="b0418-103">Aktualisiert die Attribute eines Schlüssels in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="b0418-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="b0418-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b0418-104">SYNTAX</span></span>

### <span data-ttu-id="b0418-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0418-105">Default (Default)</span></span>
```
Update-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0418-106">HsmInteractive</span><span class="sxs-lookup"><span data-stu-id="b0418-106">HsmInteractive</span></span>
```
Update-AzKeyVaultKey -HsmName <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b0418-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b0418-107">InputObject</span></span>
```
Update-AzKeyVaultKey [-InputObject] <PSKeyVaultKeyIdentityItem> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0418-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b0418-108">DESCRIPTION</span></span>
<span data-ttu-id="b0418-109">Das **Cmdlet "Update-AzKeyVaultKey"** aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="b0418-109">The **Update-AzKeyVaultKey** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="b0418-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b0418-110">EXAMPLES</span></span>

### <span data-ttu-id="b0418-111">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="b0418-111">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```powershell
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = 'true'}
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru

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

<span data-ttu-id="b0418-112">Der erste Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="b0418-112">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="b0418-113">Dieses Objekt gibt eine Uhrzeit in zwei Jahren in der Zukunft an.</span><span class="sxs-lookup"><span data-stu-id="b0418-113">That object specifies a time two years in the future.</span></span> <span data-ttu-id="b0418-114">Der Befehl speichert dieses Datum in der $Expires Variable.</span><span class="sxs-lookup"><span data-stu-id="b0418-114">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="b0418-115">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="b0418-115">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="b0418-116">Der zweite Befehl erstellt eine Variable zum Speichern von Tagwerten mit hohem Schweregrad und Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="b0418-116">The second command creates a variable to store tag values of high severity and Accounting.</span></span>
<span data-ttu-id="b0418-117">Der letzte Befehl ändert einen Schlüssel namens "ITSoftware".</span><span class="sxs-lookup"><span data-stu-id="b0418-117">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="b0418-118">Der Befehl aktiviert den Schlüssel, legt seine Ablaufzeit auf die in der $Expires gespeicherte Zeit fest und legt die Tags fest, die in einer $Tags.</span><span class="sxs-lookup"><span data-stu-id="b0418-118">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="b0418-119">Beispiel 2: Ändern einer Taste zum Löschen aller Tags</span><span class="sxs-lookup"><span data-stu-id="b0418-119">Example 2: Modify a key to delete all tags</span></span>
```powershell
PS C:\> Update-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Version '394f9379a47a4e2086585468de6c7ae5' -Tag @{}

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

<span data-ttu-id="b0418-120">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels namens "ITSoftware" gelöscht.</span><span class="sxs-lookup"><span data-stu-id="b0418-120">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="b0418-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0418-121">PARAMETERS</span></span>

### <span data-ttu-id="b0418-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0418-122">-DefaultProfile</span></span>
<span data-ttu-id="b0418-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0418-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0418-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="b0418-124">-Enable</span></span>
<span data-ttu-id="b0418-125">"True" aktiviert den Schlüssel, und mit dem Wert "false" wird der Schlüssel deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="b0418-125">Value of true enables the key and a value of false disabless the key.</span></span>
<span data-ttu-id="b0418-126">Wenn nichts angegeben wird, bleibt der vorhandene Status "Aktiviert/Deaktiviert" unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0418-126">If not specified, the existing enabled/disabled state remains unchanged.</span></span>

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

### <span data-ttu-id="b0418-127">-Expires</span><span class="sxs-lookup"><span data-stu-id="b0418-127">-Expires</span></span>
<span data-ttu-id="b0418-128">Die Ablaufzeit eines Schlüssels in UTC.</span><span class="sxs-lookup"><span data-stu-id="b0418-128">The expiration time of a key in UTC time.</span></span>
<span data-ttu-id="b0418-129">Wenn keine Angabe ausgeführt wird, bleibt die vorhandene Ablaufzeit des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0418-129">If not specified, the existing expiration time of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b0418-130">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b0418-130">-HsmName</span></span>
<span data-ttu-id="b0418-131">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="b0418-131">HSM name.</span></span> <span data-ttu-id="b0418-132">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b0418-132">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractive
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0418-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b0418-133">-InputObject</span></span>
<span data-ttu-id="b0418-134">Schlüsselobjekt</span><span class="sxs-lookup"><span data-stu-id="b0418-134">Key object</span></span>

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

### <span data-ttu-id="b0418-135">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="b0418-135">-KeyOps</span></span>
<span data-ttu-id="b0418-136">Die Vorgänge, die mit dem Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="b0418-136">The operations that can be performed with the key.</span></span>
<span data-ttu-id="b0418-137">Wenn keine Angabe ausgeführt wird, bleiben die vorhandenen Schlüsselvorgänge des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0418-137">If not specified, the existing key operations of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b0418-138">-Name</span><span class="sxs-lookup"><span data-stu-id="b0418-138">-Name</span></span>
<span data-ttu-id="b0418-139">Schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="b0418-139">Key name.</span></span>
<span data-ttu-id="b0418-140">Das Cmdlet erstellt den FQDN eines Schlüssels aus dem Namen des Tresors, der aktuell ausgewählte Umgebung und schlüsselname.</span><span class="sxs-lookup"><span data-stu-id="b0418-140">Cmdlet constructs the FQDN of a key from vault name, currently selected environment and key name.</span></span>

```yaml
Type: System.String
Parameter Sets: Default, HsmInteractive
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0418-141">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="b0418-141">-NotBefore</span></span>
<span data-ttu-id="b0418-142">Die UTC-Zeit, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0418-142">The UTC time before which key can't be used.</span></span>
<span data-ttu-id="b0418-143">Wenn nichts angegeben wird, bleibt das vorhandene "NotBefore"-Attribut des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0418-143">If not specified, the existing NotBefore attribute of the key remains unchanged.</span></span>

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

### <span data-ttu-id="b0418-144">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b0418-144">-PassThru</span></span>
<span data-ttu-id="b0418-145">Das Cmdlet gibt standardmäßig kein Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="b0418-145">Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="b0418-146">Wenn dieser Schalter angegeben ist, wird das aktualisierte Schlüsselbündelobjekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b0418-146">If this switch is specified, returns the updated key bundle object.</span></span>

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

### <span data-ttu-id="b0418-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="b0418-147">-Tag</span></span>
<span data-ttu-id="b0418-148">Eine Hashtable stellt Schlüsseltags dar.</span><span class="sxs-lookup"><span data-stu-id="b0418-148">A hashtable represents key tags.</span></span>
<span data-ttu-id="b0418-149">Wenn nichts angegeben wird, bleiben die vorhandenen Tags des Schlüssels unverändert.</span><span class="sxs-lookup"><span data-stu-id="b0418-149">If not specified, the existings tags of the key remain unchanged.</span></span>

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

### <span data-ttu-id="b0418-150">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b0418-150">-VaultName</span></span>
<span data-ttu-id="b0418-151">Name des Tresors.</span><span class="sxs-lookup"><span data-stu-id="b0418-151">Vault name.</span></span>
<span data-ttu-id="b0418-152">Das Cmdlet erstellt den FQDN eines Tresors basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="b0418-152">Cmdlet constructs the FQDN of a vault based on the name and currently selected environment.</span></span>

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

### <span data-ttu-id="b0418-153">-Version</span><span class="sxs-lookup"><span data-stu-id="b0418-153">-Version</span></span>
<span data-ttu-id="b0418-154">Schlüsselversion.</span><span class="sxs-lookup"><span data-stu-id="b0418-154">Key version.</span></span>
<span data-ttu-id="b0418-155">Das Cmdlet erstellt den FQDN eines Schlüssels aus dem Namen des Tresors, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüsselversion.</span><span class="sxs-lookup"><span data-stu-id="b0418-155">Cmdlet constructs the FQDN of a key from vault name, currently selected environment, key name and key version.</span></span>

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

### <span data-ttu-id="b0418-156">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b0418-156">-Confirm</span></span>
<span data-ttu-id="b0418-157">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b0418-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0418-158">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="b0418-158">-WhatIf</span></span>
<span data-ttu-id="b0418-159">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b0418-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0418-160">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b0418-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0418-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0418-161">CommonParameters</span></span>
<span data-ttu-id="b0418-162">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0418-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0418-163">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b0418-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0418-164">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b0418-164">INPUTS</span></span>

### <span data-ttu-id="b0418-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b0418-165">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

## <span data-ttu-id="b0418-166">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b0418-166">OUTPUTS</span></span>

### <span data-ttu-id="b0418-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="b0418-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="b0418-168">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b0418-168">NOTES</span></span>

## <span data-ttu-id="b0418-169">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b0418-169">RELATED LINKS</span></span>
