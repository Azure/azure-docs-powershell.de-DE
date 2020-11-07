---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-AzKeyvaultkeyattribute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultKeyAttribute.md
ms.openlocfilehash: df861a5efa87126b5eac1657a2b33b6fbae2110b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843851"
---
# <span data-ttu-id="96e4c-101">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="96e4c-101">Set-AzKeyVaultKeyAttribute</span></span>

## <span data-ttu-id="96e4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="96e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="96e4c-103">Aktualisiert die Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="96e4c-103">Updates the attributes of a key in a key vault.</span></span>

## <span data-ttu-id="96e4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="96e4c-104">SYNTAX</span></span>

```
Set-AzKeyVaultKeyAttribute [-VaultName] <String> [-Name] <String> [[-Version] <String>] [-Enable <Boolean>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-KeyOps <String[]>] [-Tag <Hashtable>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="96e4c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="96e4c-105">DESCRIPTION</span></span>
<span data-ttu-id="96e4c-106">Das Cmdlet " **Satz-AzKeyVaultKeyAttribute** " aktualisiert die bearbeitbaren Attribute eines Schlüssels in einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="96e4c-106">The **Set-AzKeyVaultKeyAttribute** cmdlet updates the editable attributes of a key in a key vault.</span></span>

## <span data-ttu-id="96e4c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="96e4c-107">EXAMPLES</span></span>

### <span data-ttu-id="96e4c-108">Beispiel 1: Ändern eines Schlüssels, um ihn zu aktivieren, und Festlegen des Ablaufdatums und der Tags</span><span class="sxs-lookup"><span data-stu-id="96e4c-108">Example 1: Modify a key to enable it, and set the expiration date and tags</span></span>
```
PS C:\>$Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Expires $Expires -Enable $True -Tag $Tags -PassThru
```

<span data-ttu-id="96e4c-109">Mit dem ersten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="96e4c-109">The first command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="96e4c-110">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="96e4c-110">That object specifies a time two years in the future.</span></span> <span data-ttu-id="96e4c-111">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="96e4c-111">The command stores that date in the $Expires variable.</span></span>
<span data-ttu-id="96e4c-112">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="96e4c-112">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="96e4c-113">Der zweite Befehl erstellt eine Variable zum Speichern von Tag-Werten mit einem höheren Schweregrad und einer Buchhaltung.</span><span class="sxs-lookup"><span data-stu-id="96e4c-113">The second command creates a variable to store tag values of high severity and Accounting.</span></span>

<span data-ttu-id="96e4c-114">Der endgültige Befehl ändert einen Schlüssel mit dem Namen ITSoftware.</span><span class="sxs-lookup"><span data-stu-id="96e4c-114">The final command modifies a key named ITSoftware.</span></span> <span data-ttu-id="96e4c-115">Der Befehl aktiviert den Schlüssel, legt dessen Ablaufzeit auf die in $Expires gespeicherte Zeit fest und legt die in $Tags gespeicherten Tags fest.</span><span class="sxs-lookup"><span data-stu-id="96e4c-115">The command enables the key, sets its expiration time to the time stored in $Expires, and sets the tags that are stored in $Tags.</span></span>

### <span data-ttu-id="96e4c-116">Beispiel 2: Ändern einer Taste zum Löschen aller Kategorien</span><span class="sxs-lookup"><span data-stu-id="96e4c-116">Example 2: Modify a key to delete all tags</span></span>
```
PS C:\>Set-AzKeyVaultKeyAttribute -VaultName 'Contoso' -Name 'ITSoftware' -Version '7EEA45C6EE50490B9C3176F80AC1A0DG' -Tag @{}
```

<span data-ttu-id="96e4c-117">Mit diesen Befehlen werden alle Tags für eine bestimmte Version eines Schlüssels mit dem Namen ITSoftware gelöscht.</span><span class="sxs-lookup"><span data-stu-id="96e4c-117">This commands deletes all tags for a specific version of a key named ITSoftware.</span></span>

## <span data-ttu-id="96e4c-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="96e4c-118">PARAMETERS</span></span>

### <span data-ttu-id="96e4c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e4c-119">-DefaultProfile</span></span>
<span data-ttu-id="96e4c-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="96e4c-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-121">-Enable</span><span class="sxs-lookup"><span data-stu-id="96e4c-121">-Enable</span></span>
<span data-ttu-id="96e4c-122">Gibt an, ob ein Schlüssel aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e4c-122">Specifies whether to enable or disable a key.</span></span> <span data-ttu-id="96e4c-123">Der Wert $true aktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="96e4c-123">A value of $True enables the key.</span></span> <span data-ttu-id="96e4c-124">Der Wert $false deaktiviert den Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="96e4c-124">A value of $False disables the key.</span></span> <span data-ttu-id="96e4c-125">Wenn Sie diesen Parameter nicht angeben, ändert dieses Cmdlet nicht den Status des Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="96e4c-125">If you do not specify this parameter, this cmdlet does not modify the status of the key.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-126">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="96e4c-126">-Expires</span></span>
<span data-ttu-id="96e4c-127">Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, der vom Cmdlet aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="96e4c-127">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet updates.</span></span> <span data-ttu-id="96e4c-128">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="96e4c-128">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="96e4c-129">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="96e4c-129">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="96e4c-130">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="96e4c-130">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-131">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="96e4c-131">-KeyOps</span></span>
<span data-ttu-id="96e4c-132">Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="96e4c-132">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="96e4c-133">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="96e4c-133">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="96e4c-134">Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der JSON Web Key-Spezifikation definiert sind.</span><span class="sxs-lookup"><span data-stu-id="96e4c-134">The acceptable values for this parameter are a comma-separated list of key operations as defined by the JSON Web Key specification.</span></span> <span data-ttu-id="96e4c-135">Diese Werte (Groß-/Kleinschreibung beachten) sind:</span><span class="sxs-lookup"><span data-stu-id="96e4c-135">These values (case-sensitive) are:</span></span>

- <span data-ttu-id="96e4c-136">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="96e4c-136">encrypt</span></span>
- <span data-ttu-id="96e4c-137">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="96e4c-137">decrypt</span></span>
- <span data-ttu-id="96e4c-138">Umbrechen</span><span class="sxs-lookup"><span data-stu-id="96e4c-138">wrap</span></span>
- <span data-ttu-id="96e4c-139">Unwrap</span><span class="sxs-lookup"><span data-stu-id="96e4c-139">unwrap</span></span>
- <span data-ttu-id="96e4c-140">melden sich</span><span class="sxs-lookup"><span data-stu-id="96e4c-140">sign</span></span>
- <span data-ttu-id="96e4c-141">prüfen</span><span class="sxs-lookup"><span data-stu-id="96e4c-141">verify</span></span>
- <span data-ttu-id="96e4c-142">Backup</span><span class="sxs-lookup"><span data-stu-id="96e4c-142">backup</span></span>
- <span data-ttu-id="96e4c-143">Wiederherstellungs</span><span class="sxs-lookup"><span data-stu-id="96e4c-143">restore</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-144">-Name</span><span class="sxs-lookup"><span data-stu-id="96e4c-144">-Name</span></span>
<span data-ttu-id="96e4c-145">Gibt den Namen des Schlüssels an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="96e4c-145">Specifies the name of the key to update.</span></span> <span data-ttu-id="96e4c-146">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="96e4c-146">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-147">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="96e4c-147">-NotBefore</span></span>
<span data-ttu-id="96e4c-148">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="96e4c-148">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span>
<span data-ttu-id="96e4c-149">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="96e4c-149">This parameter uses UTC.</span></span>
<span data-ttu-id="96e4c-150">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="96e4c-150">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-151">-PassThru</span><span class="sxs-lookup"><span data-stu-id="96e4c-151">-PassThru</span></span>
<span data-ttu-id="96e4c-152">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="96e4c-152">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="96e4c-153">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="96e4c-153">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="96e4c-154">-Tag</span></span>
<span data-ttu-id="96e4c-155">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="96e4c-155">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="96e4c-156">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="96e4c-156">For example:</span></span>

<span data-ttu-id="96e4c-157">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="96e4c-157">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-158">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="96e4c-158">-VaultName</span></span>
<span data-ttu-id="96e4c-159">Gibt den Namen des Schlüsseldepots an, in dem dieses Cmdlet den Schlüssel ändert.</span><span class="sxs-lookup"><span data-stu-id="96e4c-159">Specifies the name of the key vault in which this cmdlet modifies the key.</span></span>
<span data-ttu-id="96e4c-160">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="96e4c-160">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-161">-Version</span><span class="sxs-lookup"><span data-stu-id="96e4c-161">-Version</span></span>
<span data-ttu-id="96e4c-162">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="96e4c-162">Specifies the key version.</span></span>
<span data-ttu-id="96e4c-163">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="96e4c-163">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyVersion

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-164">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="96e4c-164">-Confirm</span></span>
<span data-ttu-id="96e4c-165">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="96e4c-165">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-166">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e4c-166">-WhatIf</span></span>
<span data-ttu-id="96e4c-167">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96e4c-167">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96e4c-168">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="96e4c-168">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e4c-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e4c-169">CommonParameters</span></span>
<span data-ttu-id="96e4c-170">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96e4c-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e4c-171">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96e4c-171">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e4c-172">Eingaben</span><span class="sxs-lookup"><span data-stu-id="96e4c-172">INPUTS</span></span>

### <span data-ttu-id="96e4c-173">Keine</span><span class="sxs-lookup"><span data-stu-id="96e4c-173">None</span></span>
<span data-ttu-id="96e4c-174">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="96e4c-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="96e4c-175">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="96e4c-175">OUTPUTS</span></span>

### <span data-ttu-id="96e4c-176">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="96e4c-176">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="96e4c-177">Notizen</span><span class="sxs-lookup"><span data-stu-id="96e4c-177">NOTES</span></span>

## <span data-ttu-id="96e4c-178">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="96e4c-178">RELATED LINKS</span></span>

[<span data-ttu-id="96e4c-179">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96e4c-179">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="96e4c-180">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96e4c-180">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="96e4c-181">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="96e4c-181">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)
