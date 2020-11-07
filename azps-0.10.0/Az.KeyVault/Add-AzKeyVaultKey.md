---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azKeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: b01ed80385726660198d3f6fbb20ab1e5ec57dfe
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843911"
---
# <span data-ttu-id="04396-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04396-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="04396-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="04396-102">SYNOPSIS</span></span>
<span data-ttu-id="04396-103">Erstellt einen Schlüssel in einem schlüsseltresor oder importiert einen Schlüssel in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="04396-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="04396-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="04396-104">SYNTAX</span></span>

### <span data-ttu-id="04396-105">Erstellen (Standard)</span><span class="sxs-lookup"><span data-stu-id="04396-105">Create (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04396-106">Importieren</span><span class="sxs-lookup"><span data-stu-id="04396-106">Import</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04396-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="04396-107">DESCRIPTION</span></span>
<span data-ttu-id="04396-108">Das Cmdlet **Add-AzKeyVaultKey** erstellt einen Schlüssel in einem schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="04396-108">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="04396-109">Verwenden Sie dieses Cmdlet, um Schlüssel mithilfe einer der folgenden Methoden hinzuzufügen:</span><span class="sxs-lookup"><span data-stu-id="04396-109">Use this cmdlet to add keys by using any of the following methods:</span></span>

- <span data-ttu-id="04396-110">Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (HSM) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="04396-110">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="04396-111">Erstellen Sie einen Schlüssel in Software im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="04396-111">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="04396-112">Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (HSM) zu HSMs im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="04396-112">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="04396-113">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="04396-113">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="04396-114">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in die Hardwaresicherheitsmodule (HSMs) des Key Vault-Diensts.</span><span class="sxs-lookup"><span data-stu-id="04396-114">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>

<span data-ttu-id="04396-115">Für alle diese Vorgänge können Sie wichtige Attribute bereitstellen oder Standardeinstellungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="04396-115">For any of these operations, you can provide key attributes or accept default settings.</span></span>

<span data-ttu-id="04396-116">Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="04396-116">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="04396-117">Sie können mithilfe des versionsspezifischen URIs für diese Version des Schlüssels auf die vorherigen Werte zugreifen.</span><span class="sxs-lookup"><span data-stu-id="04396-117">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="04396-118">Informationen zu Schlüssel Versionen und der URI-Struktur finden Sie unter [Informationen zu Schlüsseln](http://go.microsoft.com/fwlink/?linkid=518560) in der andSecrets-API-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="04396-118">To learn about key versions and the URI structure, see [About Keys andSecrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>

<span data-ttu-id="04396-119">Hinweis: Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen.</span><span class="sxs-lookup"><span data-stu-id="04396-119">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="04396-120">Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="04396-120">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

<span data-ttu-id="04396-121">Als bewährte Methode können Sie mithilfe des Backup-AzKeyVaultKey-Cmdlets Ihren Schlüssel nach dem Erstellen oder aktualisieren sichern.</span><span class="sxs-lookup"><span data-stu-id="04396-121">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="04396-122">Es gibt keine Funktion zur Undelete-Funktion, wenn Sie Ihren Schlüssel versehentlich löschen oder löschen und dann Ihre Vorstellung ändern, ist der Schlüssel nicht wiederherstellbar, es sei denn, Sie haben eine Sicherungskopie davon, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="04396-122">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="04396-123">Beispiele</span><span class="sxs-lookup"><span data-stu-id="04396-123">EXAMPLES</span></span>

### <span data-ttu-id="04396-124">Beispiel 1: Erstellen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="04396-124">Example 1: Create a key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITSoftware' -Destination 'Software'
```

<span data-ttu-id="04396-125">Dieser Befehl erstellt einen Software geschützten Schlüssel mit dem Namen ITSoftware im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="04396-125">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="04396-126">Beispiel 2: Erstellen eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="04396-126">Example 2: Create an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsm' -Destination 'HSM'
```

<span data-ttu-id="04396-127">Mit diesem Befehl wird im schlüsseltresor mit dem Namen Contoso ein HSM-geschützter Schlüssel erstellt.</span><span class="sxs-lookup"><span data-stu-id="04396-127">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="04396-128">Beispiel 3: Erstellen eines Schlüssels mit nicht standardmäßigen Werten</span><span class="sxs-lookup"><span data-stu-id="04396-128">Example 3: Create a key with non-default values</span></span>
```
PS C:\>$KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = null}
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags
```

<span data-ttu-id="04396-129">Der erste Befehl speichert die Werte, die entschlüsselt und in der $KeyOperations Variablen überprüft werden.</span><span class="sxs-lookup"><span data-stu-id="04396-129">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>

<span data-ttu-id="04396-130">Mit dem zweiten Befehl wird mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt erstellt, das in UTC definiert ist.</span><span class="sxs-lookup"><span data-stu-id="04396-130">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="04396-131">Dieses Objekt gibt eine Uhrzeit in der Zukunft zwei Jahre an.</span><span class="sxs-lookup"><span data-stu-id="04396-131">That object specifies a time two years in the future.</span></span> <span data-ttu-id="04396-132">Der Befehl speichert dieses Datum in der $Expires Variablen.</span><span class="sxs-lookup"><span data-stu-id="04396-132">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="04396-133">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="04396-133">For more information, type `Get-Help Get-Date`.</span></span>

<span data-ttu-id="04396-134">Der dritte Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="04396-134">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="04396-135">Dieses Objekt gibt die aktuelle UTC-Zeit an.</span><span class="sxs-lookup"><span data-stu-id="04396-135">That object specifies current UTC time.</span></span> <span data-ttu-id="04396-136">Der Befehl speichert dieses Datum in der $NotBefore Variablen.</span><span class="sxs-lookup"><span data-stu-id="04396-136">The command stores that date in the $NotBefore variable.</span></span>

<span data-ttu-id="04396-137">Der endgültige Befehl erstellt einen Schlüssel mit dem Namen ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="04396-137">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="04396-138">Der Befehl gibt Werte für zulässige Schlüsselvorgänge an, die $KeyOperations gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="04396-138">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="04396-139">Der Befehl gibt die Zeiten für die in den vorherigen Befehlen erstellten Ablauf-und *NotBefore* -Parameter sowie die Tags für den höchsten Schweregrad und das *Datum* an.</span><span class="sxs-lookup"><span data-stu-id="04396-139">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="04396-140">Der neue Schlüssel ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="04396-140">The new key is disabled.</span></span> <span data-ttu-id="04396-141">Sie können es mithilfe des Cmdlets " **festlegen-AzKeyVaultKey** " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="04396-141">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="04396-142">Beispiel 4: Importieren eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="04396-142">Example 4: Import an HSM-protected key</span></span>
```
PS C:\>Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'
```

<span data-ttu-id="04396-143">Dieser Befehl importiert den Schlüssel mit dem Namen ITByok von dem Speicherort, der vom *keyFilePath* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="04396-143">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="04396-144">Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="04396-144">The imported key is an HSM-protected key.</span></span>

<span data-ttu-id="04396-145">Wenn Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul importieren möchten, müssen Sie zunächst ein BYOK-Paket (eine Datei mit der Dateinamenerweiterung. BYOK) mithilfe des Azure Key Vault-BYOK-Toolsets erstellen.</span><span class="sxs-lookup"><span data-stu-id="04396-145">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="04396-146">Weitere Informationen finden Sie unter [so wird es gemacht: generieren und übertragen von HSM-Protected Schlüsseln für Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span><span class="sxs-lookup"><span data-stu-id="04396-146">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="04396-147">Beispiel 5: Importieren eines Software geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="04396-147">Example 5: Import a software-protected key</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password
```

<span data-ttu-id="04396-148">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="04396-148">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="04396-149">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help
ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="04396-149">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>

<span data-ttu-id="04396-150">Der zweite Befehl erstellt ein Software Kennwort im Contoso-Schlüsselspeicher.</span><span class="sxs-lookup"><span data-stu-id="04396-150">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="04396-151">Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, das in $Password gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="04396-151">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="04396-152">Beispiel 6: Importieren eines Schlüssels und Zuweisen von Attributen</span><span class="sxs-lookup"><span data-stu-id="04396-152">Example 6: Import a key and assign attributes</span></span>
```
PS C:\>$Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = null }
PS C:\> Add-AzKeyVaultKey -VaultName 'Contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags
```

<span data-ttu-id="04396-153">Der erste Befehl wandelt eine Zeichenfolge mithilfe des Cmdlets **ConvertTo-SecureString** in eine sichere Zeichenfolge um und speichert diese Zeichenfolge dann in der $Password Variablen.</span><span class="sxs-lookup"><span data-stu-id="04396-153">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>

<span data-ttu-id="04396-154">Der zweite Befehl erstellt mithilfe des **Get-Date-** Cmdlets ein **DateTime** -Objekt und speichert dieses Objekt dann in der $Expires-Variablen.</span><span class="sxs-lookup"><span data-stu-id="04396-154">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>

<span data-ttu-id="04396-155">Mit dem dritten Befehl wird die $Tags-Variable erstellt, um Tags für einen höheren Schweregrad und die Variable festzulegen.</span><span class="sxs-lookup"><span data-stu-id="04396-155">The third command creates the $tags variable to set tags for high severity and IT.</span></span>

<span data-ttu-id="04396-156">Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel vom angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="04396-156">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="04396-157">Der Befehl gibt die Ablaufzeit an, die in $Expires und dem in $Password gespeicherten Kennwort gespeichert ist, und wendet die in $Tags gespeicherten Tags an.</span><span class="sxs-lookup"><span data-stu-id="04396-157">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

## <span data-ttu-id="04396-158">Parameter</span><span class="sxs-lookup"><span data-stu-id="04396-158">PARAMETERS</span></span>

### <span data-ttu-id="04396-159">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04396-159">-DefaultProfile</span></span>
<span data-ttu-id="04396-160">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="04396-160">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="04396-161">-Ziel</span><span class="sxs-lookup"><span data-stu-id="04396-161">-Destination</span></span>
<span data-ttu-id="04396-162">Gibt an, ob der Schlüssel als Software geschützter Schlüssel oder als HSM-geschützter Schlüssel im Key Vault-Dienst hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04396-162">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="04396-163">Gültige Werte sind: HSM und Software.</span><span class="sxs-lookup"><span data-stu-id="04396-163">Valid values are: HSM and Software.</span></span>

<span data-ttu-id="04396-164">Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen schlüsseltresor verfügen, der HSMs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="04396-164">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="04396-165">Weitere Informationen zu den Dienstebenen und Funktionen für Azure Key Vault finden Sie auf der [Azure Key Vault-Preis Website](http://go.microsoft.com/fwlink/?linkid=512521).</span><span class="sxs-lookup"><span data-stu-id="04396-165">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>

<span data-ttu-id="04396-166">Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="04396-166">This parameter is required when you create a new key.</span></span> <span data-ttu-id="04396-167">Wenn Sie einen Schlüssel mithilfe des *keyFilePath* -Parameters importieren, ist dieser Parameter optional:</span><span class="sxs-lookup"><span data-stu-id="04396-167">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>

- <span data-ttu-id="04396-168">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung Byok verfügt, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="04396-168">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="04396-169">Das Cmdlet kann diesen Schlüssel nicht als Software geschützten Schlüssel importieren.</span><span class="sxs-lookup"><span data-stu-id="04396-169">The cmdlet cannot import that key as software-protected key.</span></span>

- <span data-ttu-id="04396-170">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel importiert, der über die Dateinamenerweiterung PFX verfügt, wird der Schlüssel als Software geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="04396-170">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: String
Parameter Sets: Create
Aliases: 
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Import
Aliases: 
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04396-171">-Deaktivieren Sie</span><span class="sxs-lookup"><span data-stu-id="04396-171">-Disable</span></span>
<span data-ttu-id="04396-172">Gibt an, dass der hinzuzufügende Schlüssel auf den Anfangszustand disabled festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="04396-172">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="04396-173">Jeder Versuch, den Schlüssel zu verwenden, schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="04396-173">Any attempt to use the key will fail.</span></span> <span data-ttu-id="04396-174">Verwenden Sie diesen Parameter, wenn Sie Schlüssel Vorabladen, die Sie später aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="04396-174">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="04396-175">-Läuft ab</span><span class="sxs-lookup"><span data-stu-id="04396-175">-Expires</span></span>
<span data-ttu-id="04396-176">Gibt die Ablaufzeit als **DateTime** -Objekt für den Schlüssel an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="04396-176">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="04396-177">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="04396-177">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="04396-178">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04396-178">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="04396-179">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="04396-179">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="04396-180">Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.</span><span class="sxs-lookup"><span data-stu-id="04396-180">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="04396-181">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="04396-181">-KeyFilePassword</span></span>
<span data-ttu-id="04396-182">Gibt ein Kennwort für die importierte Datei als **SecureString** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="04396-182">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="04396-183">Verwenden Sie zum Abrufen eines **SecureString** -Objekts das Cmdlet **ConvertTo-SecureString** .</span><span class="sxs-lookup"><span data-stu-id="04396-183">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="04396-184">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help ConvertTo-SecureString` .</span><span class="sxs-lookup"><span data-stu-id="04396-184">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="04396-185">Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.</span><span class="sxs-lookup"><span data-stu-id="04396-185">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: SecureString
Parameter Sets: Import
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04396-186">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="04396-186">-KeyFilePath</span></span>
<span data-ttu-id="04396-187">Gibt den Pfad einer lokalen Datei an, die das Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="04396-187">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="04396-188">Die gültigen Dateinamenerweiterungen sind Byok und PFX.</span><span class="sxs-lookup"><span data-stu-id="04396-188">The valid file name extensions are .byok and .pfx.</span></span>

- <span data-ttu-id="04396-189">Wenn es sich bei der Datei um eine Byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standardwert nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="04396-189">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>

- <span data-ttu-id="04396-190">Wenn es sich bei der Datei um eine PFX-Datei handelt, wird der Schlüssel nach dem Import automatisch durch Software geschützt.</span><span class="sxs-lookup"><span data-stu-id="04396-190">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="04396-191">Um diesen Standardwert zu überschreiben, setzen Sie den *Ziel* Parameter auf HSM, damit der Schlüssel HSM-geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="04396-191">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>

<span data-ttu-id="04396-192">Wenn Sie diesen Parameter angeben, ist der *Ziel* Parameter optional.</span><span class="sxs-lookup"><span data-stu-id="04396-192">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: String
Parameter Sets: Import
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04396-193">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="04396-193">-KeyOps</span></span>
<span data-ttu-id="04396-194">Gibt ein Array von Vorgängen an, die mit dem vom Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="04396-194">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="04396-195">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="04396-195">If you do not specify this parameter, all operations can be performed.</span></span>

<span data-ttu-id="04396-196">Bei den akzeptablen Werten für diesen Parameter handelt es sich um eine durch trennzeichengetrennte Liste der wichtigsten Vorgänge, wie Sie in der [JSON Web Key (JWK)-Spezifikation](http://go.microsoft.com/fwlink/?LinkID=613300)definiert ist:</span><span class="sxs-lookup"><span data-stu-id="04396-196">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>

- <span data-ttu-id="04396-197">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="04396-197">Encrypt</span></span>
- <span data-ttu-id="04396-198">Entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="04396-198">Decrypt</span></span>
- <span data-ttu-id="04396-199">Umbrechen</span><span class="sxs-lookup"><span data-stu-id="04396-199">Wrap</span></span>
- <span data-ttu-id="04396-200">Unwrap</span><span class="sxs-lookup"><span data-stu-id="04396-200">Unwrap</span></span>
- <span data-ttu-id="04396-201">Melden sich</span><span class="sxs-lookup"><span data-stu-id="04396-201">Sign</span></span>
- <span data-ttu-id="04396-202">Prüfen</span><span class="sxs-lookup"><span data-stu-id="04396-202">Verify</span></span>

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

### <span data-ttu-id="04396-203">-Name</span><span class="sxs-lookup"><span data-stu-id="04396-203">-Name</span></span>
<span data-ttu-id="04396-204">Gibt den Namen des Schlüssels an, der dem schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="04396-204">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="04396-205">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="04396-205">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="04396-206">Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, a-z und-(das Strichsymbol) enthält.</span><span class="sxs-lookup"><span data-stu-id="04396-206">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04396-207">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="04396-207">-NotBefore</span></span>
<span data-ttu-id="04396-208">Gibt die Uhrzeit als **DateTime** -Objekt an, vor der der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="04396-208">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="04396-209">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="04396-209">This parameter uses UTC.</span></span> <span data-ttu-id="04396-210">Verwenden Sie das Cmdlet " **Get-Date** ", um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="04396-210">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="04396-211">Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="04396-211">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="04396-212">-Tag</span><span class="sxs-lookup"><span data-stu-id="04396-212">-Tag</span></span>
<span data-ttu-id="04396-213">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="04396-213">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="04396-214">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="04396-214">For example:</span></span>

<span data-ttu-id="04396-215">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="04396-215">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="04396-216">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="04396-216">-VaultName</span></span>
<span data-ttu-id="04396-217">Gibt den Namen des Schlüsselspeichers an, dem dieses Cmdlet den Schlüssel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="04396-217">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="04396-218">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="04396-218">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="04396-219">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="04396-219">-Confirm</span></span>
<span data-ttu-id="04396-220">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="04396-220">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04396-221">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04396-221">-WhatIf</span></span>
<span data-ttu-id="04396-222">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="04396-222">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04396-223">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="04396-223">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04396-224">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04396-224">CommonParameters</span></span>
<span data-ttu-id="04396-225">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04396-225">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04396-226">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04396-226">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04396-227">Eingaben</span><span class="sxs-lookup"><span data-stu-id="04396-227">INPUTS</span></span>

### <span data-ttu-id="04396-228">Keine</span><span class="sxs-lookup"><span data-stu-id="04396-228">None</span></span>
<span data-ttu-id="04396-229">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="04396-229">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="04396-230">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="04396-230">OUTPUTS</span></span>

### <span data-ttu-id="04396-231">Microsoft. Azure. Commands. keyvault. Models. keybundle</span><span class="sxs-lookup"><span data-stu-id="04396-231">Microsoft.Azure.Commands.KeyVault.Models.KeyBundle</span></span>

## <span data-ttu-id="04396-232">Notizen</span><span class="sxs-lookup"><span data-stu-id="04396-232">NOTES</span></span>

## <span data-ttu-id="04396-233">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="04396-233">RELATED LINKS</span></span>

[<span data-ttu-id="04396-234">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04396-234">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="04396-235">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04396-235">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="04396-236">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="04396-236">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="04396-237">Satz-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="04396-237">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
