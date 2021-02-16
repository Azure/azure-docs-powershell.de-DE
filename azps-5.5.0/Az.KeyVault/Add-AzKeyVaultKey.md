---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 846F781C-73A3-4BBE-ABD9-897371109FBE
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultKey.md
ms.openlocfilehash: da6460bf0a1126a11345336e4d55c300728bbd66
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170465"
---
# <span data-ttu-id="3eba0-101">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-101">Add-AzKeyVaultKey</span></span>

## <span data-ttu-id="3eba0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3eba0-102">SYNOPSIS</span></span>
<span data-ttu-id="3eba0-103">Erstellt einen Schlüssel in einem Schlüsseltresor oder importiert einen Schlüssel in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3eba0-103">Creates a key in a key vault or imports a key into a key vault.</span></span>

## <span data-ttu-id="3eba0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3eba0-104">SYNTAX</span></span>

### <span data-ttu-id="3eba0-105">InteractiveCreate (Standard)</span><span class="sxs-lookup"><span data-stu-id="3eba0-105">InteractiveCreate (Default)</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-106">InteractiveImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-106">InteractiveImport</span></span>
```
Add-AzKeyVaultKey [-VaultName] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-107">HsmInteractiveCreate</span><span class="sxs-lookup"><span data-stu-id="3eba0-107">HsmInteractiveCreate</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String> [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-108">HsmInteractiveImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-108">HsmInteractiveImport</span></span>
```
Add-AzKeyVaultKey -HsmName <String> [-Name] <String> -KeyFilePath <String> [-KeyFilePassword <SecureString>]
 [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-109">InputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="3eba0-109">InputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -Destination <String> [-Disable]
 [-KeyOps <String[]>] [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-110">InputObjectImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-110">InputObjectImport</span></span>
```
Add-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-111">HsmInputObjectCreate</span><span class="sxs-lookup"><span data-stu-id="3eba0-111">HsmInputObjectCreate</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-112">HsmInputObjectImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-112">HsmInputObjectImport</span></span>
```
Add-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3eba0-113">ResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="3eba0-113">ResourceIdCreate</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -Destination <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-114">ResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-114">ResourceIdImport</span></span>
```
Add-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Destination <String>] [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-KeyType <String>] [-CurveName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-115">HsmResourceIdCreate</span><span class="sxs-lookup"><span data-stu-id="3eba0-115">HsmResourceIdCreate</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Disable] [-KeyOps <String[]>]
 [-Expires <DateTime>] [-NotBefore <DateTime>] [-Tag <Hashtable>] [-Size <Int32>] -KeyType <String>
 [-CurveName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3eba0-116">HsmResourceIdImport</span><span class="sxs-lookup"><span data-stu-id="3eba0-116">HsmResourceIdImport</span></span>
```
Add-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> -KeyFilePath <String>
 [-KeyFilePassword <SecureString>] [-Disable] [-KeyOps <String[]>] [-Expires <DateTime>]
 [-NotBefore <DateTime>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3eba0-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3eba0-117">DESCRIPTION</span></span>
<span data-ttu-id="3eba0-118">Das **Cmdlet "Add-AzKeyVaultKey"** erstellt einen Schlüssel in einem Schlüsseltresor im Azure Key Vault oder importiert einen Schlüssel in einen Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3eba0-118">The **Add-AzKeyVaultKey** cmdlet creates a key in a key vault in Azure Key Vault, or imports a key into a key vault.</span></span>
<span data-ttu-id="3eba0-119">Verwenden Sie dieses Cmdlet zum Hinzufügen von Schlüsseln mit einer der folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="3eba0-119">Use this cmdlet to add keys by using any of the following methods:</span></span>
- <span data-ttu-id="3eba0-120">Erstellen Sie einen Schlüssel in einem Hardwaresicherheitsmodul (Hardware Security Module, HSM) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3eba0-120">Create a key in a hardware security module (HSM) in the Key Vault service.</span></span>
- <span data-ttu-id="3eba0-121">Erstellen Sie einen Schlüssel in der Software im Schlüsseltresordienst.</span><span class="sxs-lookup"><span data-stu-id="3eba0-121">Create a key in software in the Key Vault service.</span></span>
- <span data-ttu-id="3eba0-122">Importieren Sie einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul (Hardware Security Module, HSM) in HSMs im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3eba0-122">Import a key from your own hardware security module (HSM) to HSMs in the Key Vault service.</span></span>
- <span data-ttu-id="3eba0-123">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer.</span><span class="sxs-lookup"><span data-stu-id="3eba0-123">Import a key from a .pfx file on your computer.</span></span>
- <span data-ttu-id="3eba0-124">Importieren Sie einen Schlüssel aus einer PFX-Datei auf Ihrem Computer in Hardwaresicherheitsmodule (Hardware Security Module, HSMs) im Key Vault-Dienst.</span><span class="sxs-lookup"><span data-stu-id="3eba0-124">Import a key from a .pfx file on your computer to hardware security modules (HSMs) in the Key Vault service.</span></span>
<span data-ttu-id="3eba0-125">Für jede dieser Vorgänge können Sie Schlüsselattribute bereitstellen oder Standardeinstellungen akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-125">For any of these operations, you can provide key attributes or accept default settings.</span></span>
<span data-ttu-id="3eba0-126">Wenn Sie einen Schlüssel erstellen oder importieren, der denselben Namen wie ein vorhandener Schlüssel in Ihrem Schlüsseltresor hat, wird der ursprüngliche Schlüssel mit den Werten aktualisiert, die Sie für den neuen Schlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="3eba0-126">If you create or import a key that has the same name as an existing key in your key vault, the original key is updated with the values that you specify for the new key.</span></span> <span data-ttu-id="3eba0-127">Sie können auf die vorherigen Werte zugreifen, indem Sie den versionsspezifischen URI für diese Version des Schlüssels verwenden.</span><span class="sxs-lookup"><span data-stu-id="3eba0-127">You can access the previous values by using the version-specific URI for that version of the key.</span></span> <span data-ttu-id="3eba0-128">Informationen zu Schlüsselversionen und der URI-Struktur finden Sie [in](http://go.microsoft.com/fwlink/?linkid=518560) der Rest-API-Dokumentation zu Schlüsseln und Geheimen Schlüsseln.</span><span class="sxs-lookup"><span data-stu-id="3eba0-128">To learn about key versions and the URI structure, see [About Keys and Secrets](http://go.microsoft.com/fwlink/?linkid=518560) in the Key Vault REST API documentation.</span></span>
<span data-ttu-id="3eba0-129">Hinweis: Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-129">Note: To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span> <span data-ttu-id="3eba0-130">Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="3eba0-130">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>
<span data-ttu-id="3eba0-131">Als bewährte Methode sollten Sie Ihren Schlüssel nach dem Erstellen oder Aktualisieren sichern, indem Sie das cmdlet Backup-AzKeyVaultKey verwenden.</span><span class="sxs-lookup"><span data-stu-id="3eba0-131">As a best practice, back up your key after it is created or updated, by using the Backup-AzKeyVaultKey cmdlet.</span></span> <span data-ttu-id="3eba0-132">Es gibt keine rückgängig gemachten Funktionen. Wenn Sie also versehentlich Ihren Schlüssel löschen oder ihn löschen und dann Ihre Meinung ändern, kann der Schlüssel nur wiederhergestellt werden, wenn Sie über eine Sicherung verfügen, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="3eba0-132">There is no undelete functionality, so if you accidentally delete your key or delete it and then change your mind, the key is not recoverable unless you have a backup of it that you can restore.</span></span>

## <span data-ttu-id="3eba0-133">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3eba0-133">EXAMPLES</span></span>

### <span data-ttu-id="3eba0-134">Beispiel 1: Erstellen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3eba0-134">Example 1: Create a key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITSoftware' -Destination 'Software'

Vault Name     : contoso
Name           : ITSoftware
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="3eba0-135">Mit diesem Befehl wird ein softwaregeschützter Schlüssel namens "ITSoftware" im Schlüsseltresor "Contoso" erstellt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-135">This command creates a software-protected key named ITSoftware in the key vault named Contoso.</span></span>

### <span data-ttu-id="3eba0-136">Beispiel 2: Erstellen eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3eba0-136">Example 2: Create an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsm' -Destination 'HSM'

Vault Name     : contoso
Name           : ITHsm
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITSoftware/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="3eba0-137">Mit diesem Befehl wird ein HSM-geschützter Schlüssel im Schlüsseltresor "Contoso" erstellt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-137">This command creates an HSM-protected key in the key vault named Contoso.</span></span>

### <span data-ttu-id="3eba0-138">Beispiel 3: Erstellen eines Schlüssels mit Nicht-Standardwerten</span><span class="sxs-lookup"><span data-stu-id="3eba0-138">Example 3: Create a key with non-default values</span></span>
```powershell
PS C:\> $KeyOperations = 'decrypt', 'verify'
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $NotBefore = (Get-Date).ToUniversalTime()
PS C:\> $Tags = @{'Severity' = 'high'; 'Accounting' = "true"}
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITHsmNonDefault' -Destination 'HSM' -Expires $Expires -NotBefore $NotBefore -KeyOps $KeyOperations -Disable -Tag $Tags

Vault Name     : contoso
Name           : ITHsmNonDefault
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITHsmNonDefault/929bfc14db84439b823ffd1bedadaf5f
Enabled        : False
Expires        : 5/21/2020 11:12:43 PM
Not Before     : 5/21/2018 11:12:50 PM
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="3eba0-139">Der erste Befehl speichert die Werte zum Entschlüsseln und Überprüfen in der $KeyOperations Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-139">The first command stores the values decrypt and verify in the $KeyOperations variable.</span></span>
<span data-ttu-id="3eba0-140">Der zweite Befehl erstellt ein in UTC definiertes **DateTime-Objekt** mithilfe des **Get-Date-Cmdlets.**</span><span class="sxs-lookup"><span data-stu-id="3eba0-140">The second command creates a **DateTime** object, defined in UTC, by using the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="3eba0-141">Dieses Objekt gibt eine Uhrzeit in zwei Jahren in der Zukunft an.</span><span class="sxs-lookup"><span data-stu-id="3eba0-141">That object specifies a time two years in the future.</span></span> <span data-ttu-id="3eba0-142">Der Befehl speichert dieses Datum in der $Expires Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-142">The command stores that date in the $Expires variable.</span></span> <span data-ttu-id="3eba0-143">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="3eba0-143">For more information, type `Get-Help Get-Date`.</span></span>
<span data-ttu-id="3eba0-144">Der dritte Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="3eba0-144">The third command creates a **DateTime** object by using the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3eba0-145">Dieses Objekt gibt die aktuelle UTC-Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="3eba0-145">That object specifies current UTC time.</span></span> <span data-ttu-id="3eba0-146">Der Befehl speichert dieses Datum in der $NotBefore Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-146">The command stores that date in the $NotBefore variable.</span></span>
<span data-ttu-id="3eba0-147">Der letzte Befehl erstellt einen Schlüssel namens ITHsmNonDefault, bei dem es sich um einen HSM-geschützten Schlüssel handelt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-147">The final command creates a key named ITHsmNonDefault that is an HSM-protected key.</span></span> <span data-ttu-id="3eba0-148">Der Befehl gibt Werte für zugelassene Schlüsselvorgänge an, die $KeyOperations.</span><span class="sxs-lookup"><span data-stu-id="3eba0-148">The command specifies values for allowed key operations stored $KeyOperations.</span></span> <span data-ttu-id="3eba0-149">Der Befehl gibt Zeiten für die in den vorherigen Befehlen erstellten Parameter *"Expires"* und *"NotBefore"* sowie Tags für hohen Schweregrad und IT an.</span><span class="sxs-lookup"><span data-stu-id="3eba0-149">The command specifies times for the *Expires* and *NotBefore* parameters created in the previous commands, and tags for high severity and IT.</span></span> <span data-ttu-id="3eba0-150">Der neue Schlüssel ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3eba0-150">The new key is disabled.</span></span> <span data-ttu-id="3eba0-151">Sie können es mithilfe des **Cmdlets "Set-AzKeyVaultKey"** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-151">You can enable it by using the **Set-AzKeyVaultKey** cmdlet.</span></span>

### <span data-ttu-id="3eba0-152">Beispiel 4: Importieren eines HSM-geschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3eba0-152">Example 4: Import an HSM-protected key</span></span>
```powershell
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITByok' -KeyFilePath 'C:\Contoso\ITByok.byok' -Destination 'HSM'

Vault Name     : contoso
Name           : ITByok
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITByok/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="3eba0-153">Mit diesem Befehl wird der Schlüssel "ITByok" von dem vom *Parameter "KeyFilePath"* angegebenen Speicherort importiert.</span><span class="sxs-lookup"><span data-stu-id="3eba0-153">This command imports the key named ITByok from the location that the *KeyFilePath* parameter specifies.</span></span> <span data-ttu-id="3eba0-154">Der importierte Schlüssel ist ein HSM-geschützter Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3eba0-154">The imported key is an HSM-protected key.</span></span>
<span data-ttu-id="3eba0-155">Um einen Schlüssel aus Ihrem eigenen Hardwaresicherheitsmodul zu importieren, müssen Sie zuerst mithilfe des Azure Key Vault BYOK Toolset ein "BYOK"-Paket (eine Datei mit der Dateinamenerweiterung BYOK) generieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-155">To import a key from your own hardware security module, you must first generate a BYOK package (a file with a .byok file name extension) by using the Azure Key Vault BYOK toolset.</span></span>
<span data-ttu-id="3eba0-156">Weitere Informationen finden Sie unter "Generieren und Übertragen HSM-Protected [Schlüssel für den Azure Key Vault".](http://go.microsoft.com/fwlink/?LinkId=522252)</span><span class="sxs-lookup"><span data-stu-id="3eba0-156">For more information, see [How to Generate and Transfer HSM-Protected Keys for Azure Key Vault](http://go.microsoft.com/fwlink/?LinkId=522252).</span></span>

### <span data-ttu-id="3eba0-157">Beispiel 5: Importieren eines softwaregeschützten Schlüssels</span><span class="sxs-lookup"><span data-stu-id="3eba0-157">Example 5: Import a software-protected key</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'Password' -AsPlainText -Force
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfx' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password

Vault Name     : contoso
Name           : ITPfx
Version        : 67da57e9cadf48a2ad8d366b115843ab
Id             : https://contoso.vault.azure.net:443/keys/ITPfx/67da57e9cadf48a2ad8d366b115843ab
Enabled        : True
Expires        :
Not Before     :
Created        : 5/21/2018 11:10:58 PM
Updated        : 5/21/2018 11:10:58 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="3eba0-158">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-158">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span> <span data-ttu-id="3eba0-159">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help
ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="3eba0-159">For more information, type `Get-Help
ConvertTo-SecureString`.</span></span>
<span data-ttu-id="3eba0-160">Der zweite Befehl erstellt ein Softwarekennwort im Contoso-Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="3eba0-160">The second command creates a software password in the Contoso key vault.</span></span> <span data-ttu-id="3eba0-161">Der Befehl gibt den Speicherort für den Schlüssel und das Kennwort an, die in der Datei $Password.</span><span class="sxs-lookup"><span data-stu-id="3eba0-161">The command specifies the location for the key and the password stored in $Password.</span></span>

### <span data-ttu-id="3eba0-162">Beispiel 6: Importieren eines Schlüssels und Zuweisen von Attributen</span><span class="sxs-lookup"><span data-stu-id="3eba0-162">Example 6: Import a key and assign attributes</span></span>
```powershell
PS C:\> $Password = ConvertTo-SecureString -String 'password' -AsPlainText -Force
PS C:\> $Expires = (Get-Date).AddYears(2).ToUniversalTime()
PS C:\> $Tags = @{ 'Severity' = 'high'; 'Accounting' = "true" }
PS C:\> Add-AzKeyVaultKey -VaultName 'contoso' -Name 'ITPfxToHSM' -Destination 'HSM' -KeyFilePath 'C:\Contoso\ITPfx.pfx' -KeyFilePassword $Password -Expires $Expires -Tag $Tags

Vault Name     : contoso
Name           : ITPfxToHSM
Version        : 929bfc14db84439b823ffd1bedadaf5f
Id             : https://contoso.vault.azure.net:443/keys/ITPfxToHSM/929bfc14db84439b823ffd1bedadaf5f
Enabled        : True
Expires        : 5/21/2020 11:12:43 PM
Not Before     :
Created        : 5/21/2018 11:13:17 PM
Updated        : 5/21/2018 11:13:17 PM
Purge Disabled : False
Tags           : Name        Value
                 Severity    high
                 Accounting  true
```

<span data-ttu-id="3eba0-163">Der erste Befehl konvertiert eine Zeichenfolge mithilfe des **Cmdlets "ConvertTo-SecureString"** in eine sichere Zeichenfolge und speichert diese Zeichenfolge dann in der $Password Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-163">The first command converts a string into a secure string by using the **ConvertTo-SecureString** cmdlet, and then stores that string in the $Password variable.</span></span>
<span data-ttu-id="3eba0-164">Der zweite Befehl erstellt mithilfe des **Get-Date-Cmdlets** ein **DateTime-Objekt** und speichert dieses Objekt dann in der $Expires Variable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-164">The second command creates a **DateTime** object by using the **Get-Date** cmdlet, and then stores that object in the $Expires variable.</span></span>
<span data-ttu-id="3eba0-165">Der dritte Befehl erstellt die $tags Variable zum Festlegen von Tags für hohen Schweregrad und IT.</span><span class="sxs-lookup"><span data-stu-id="3eba0-165">The third command creates the $tags variable to set tags for high severity and IT.</span></span>
<span data-ttu-id="3eba0-166">Der endgültige Befehl importiert einen Schlüssel als HSM-Schlüssel von der angegebenen Position.</span><span class="sxs-lookup"><span data-stu-id="3eba0-166">The final command imports a key as an HSM key from the specified location.</span></span> <span data-ttu-id="3eba0-167">Der Befehl gibt die in der Datei gespeicherte $Expires und das Kennwort an und wendet die in $Password gespeicherten Tags $tags.</span><span class="sxs-lookup"><span data-stu-id="3eba0-167">The command specifies the expiration time stored in $Expires and password stored in $Password, and applies the tags stored in $tags.</span></span>

### <span data-ttu-id="3eba0-168">Beispiel 7: Generieren eines Schlüsselwechselschlüssels (KEY Exchange Key, KEK) für das Feature "Eigenen Schlüssel verwenden" (BYOK)</span><span class="sxs-lookup"><span data-stu-id="3eba0-168">Example 7: Generate a Key Exchange Key (KEK) for "bring your own key" (BYOK) feature</span></span>

```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName $vaultName -Name $keyName -Destination HSM -Size 2048 -KeyOps "import"
```

<span data-ttu-id="3eba0-169">Generiert einen Schlüssel (auch als KEK (Key Exchange Key) bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="3eba0-169">Generates a key (referred to as a Key Exchange Key (KEK)).</span></span> <span data-ttu-id="3eba0-170">Die KEK muss ein RSA-HSM-Schlüssel sein, der nur über den Importschlüsselvorgang verfügt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-170">The KEK must be an RSA-HSM key that has only the import key operation.</span></span> <span data-ttu-id="3eba0-171">Nur Key Vault Premium-SKU unterstützt RSA-HSM-Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3eba0-171">Only Key Vault Premium SKU supports RSA-HSM keys.</span></span>
<span data-ttu-id="3eba0-172">Weitere Details finden Sie unter https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="3eba0-172">For more details please refer to https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="3eba0-173">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3eba0-173">PARAMETERS</span></span>

### <span data-ttu-id="3eba0-174">-CurveName</span><span class="sxs-lookup"><span data-stu-id="3eba0-174">-CurveName</span></span>
<span data-ttu-id="3eba0-175">Gibt den Kurvennamen der Kryptografie mit auslassungspunktenden Kurven an. Dieser Wert ist gültig, wenn der KeyType EC ist.</span><span class="sxs-lookup"><span data-stu-id="3eba0-175">Specifies the curve name of elliptic curve cryptography, this value is valid when KeyType is EC.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveCreate, InputObjectImport, HsmInputObjectCreate, ResourceIdImport, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-176">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3eba0-176">-DefaultProfile</span></span>
<span data-ttu-id="3eba0-177">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3eba0-177">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3eba0-178">-Destination</span><span class="sxs-lookup"><span data-stu-id="3eba0-178">-Destination</span></span>
<span data-ttu-id="3eba0-179">Gibt an, ob der Schlüssel als softwaregeschützter Oder HSM-geschützter Schlüssel im Schlüsseltresordienst hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eba0-179">Specifies whether to add the key as a software-protected key or an HSM-protected key in the Key Vault service.</span></span>
<span data-ttu-id="3eba0-180">Gültige Werte sind: HSM und Software.</span><span class="sxs-lookup"><span data-stu-id="3eba0-180">Valid values are: HSM and Software.</span></span>
<span data-ttu-id="3eba0-181">Hinweis: Wenn Sie HSM als Ziel verwenden möchten, müssen Sie über einen Schlüsseltresor verfügen, der HSMs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-181">Note: To use HSM as your destination, you must have a key vault that supports HSMs.</span></span> <span data-ttu-id="3eba0-182">Weitere Informationen zu den Dienststufen und -funktionen für den Azure Key Vault finden Sie auf der Website "Preise für [den Azure Key Vault".](http://go.microsoft.com/fwlink/?linkid=512521)</span><span class="sxs-lookup"><span data-stu-id="3eba0-182">For more information about the service tiers and capabilities for Azure Key Vault, see the [Azure Key Vault Pricing website](http://go.microsoft.com/fwlink/?linkid=512521).</span></span>
<span data-ttu-id="3eba0-183">Dieser Parameter ist erforderlich, wenn Sie einen neuen Schlüssel erstellen.</span><span class="sxs-lookup"><span data-stu-id="3eba0-183">This parameter is required when you create a new key.</span></span> <span data-ttu-id="3eba0-184">Wenn Sie einen Schlüssel mithilfe des Parameters *"KeyFilePath"* importieren, ist dieser Parameter optional:</span><span class="sxs-lookup"><span data-stu-id="3eba0-184">If you import a key by using the *KeyFilePath* parameter, this parameter is optional:</span></span>
- <span data-ttu-id="3eba0-185">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung BYOK importiert, wird dieser Schlüssel als HSM-geschützter Schlüssel importiert.</span><span class="sxs-lookup"><span data-stu-id="3eba0-185">If you do not specify this parameter, and this cmdlet imports a key that has .byok file name extension, it imports that key as an HSM-protected key.</span></span> <span data-ttu-id="3eba0-186">Das Cmdlet kann diesen Schlüssel nicht als softwaregeschützten Schlüssel importieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-186">The cmdlet cannot import that key as software-protected key.</span></span>
- <span data-ttu-id="3eba0-187">Wenn Sie diesen Parameter nicht angeben und dieses Cmdlet einen Schlüssel mit der Dateinamenerweiterung PFX importiert, importiert es den Schlüssel als softwaregeschützten Schlüssel.</span><span class="sxs-lookup"><span data-stu-id="3eba0-187">If you do not specify this parameter, and this cmdlet imports a key that has a .pfx file name extension, it imports the key as a software-protected key.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InputObjectCreate, ResourceIdCreate
Aliases:
Accepted values: HSM, Software

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:
Accepted values: HSM, Software

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-188">-Disable</span><span class="sxs-lookup"><span data-stu-id="3eba0-188">-Disable</span></span>
<span data-ttu-id="3eba0-189">Gibt an, dass der hinzugefügte Schlüssel auf den anfänglichen Status "Deaktiviert" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3eba0-189">Indicates that the key you are adding is set to an initial state of disabled.</span></span> <span data-ttu-id="3eba0-190">Jeder Versuch, den Schlüssel zu verwenden, ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="3eba0-190">Any attempt to use the key will fail.</span></span> <span data-ttu-id="3eba0-191">Verwenden Sie diesen Parameter, wenn Sie Schlüssel vorab laden, die Sie später aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3eba0-191">Use this parameter if you are preloading keys that you intend to enable later.</span></span>

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

### <span data-ttu-id="3eba0-192">-Expires</span><span class="sxs-lookup"><span data-stu-id="3eba0-192">-Expires</span></span>
<span data-ttu-id="3eba0-193">Gibt die Ablaufzeit als **"DateTime"-Objekt** für den Schlüssel an, den dieses Cmdlet hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-193">Specifies the expiration time, as a **DateTime** object, for the key that this cmdlet adds.</span></span> <span data-ttu-id="3eba0-194">Dieser Parameter verwendet koordinierte Weltzeit (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="3eba0-194">This parameter uses Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="3eba0-195">Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="3eba0-195">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3eba0-196">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Date` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="3eba0-196">For more information, type `Get-Help Get-Date`.</span></span> <span data-ttu-id="3eba0-197">Wenn Sie diesen Parameter nicht angeben, läuft der Schlüssel nicht ab.</span><span class="sxs-lookup"><span data-stu-id="3eba0-197">If you do not specify this parameter, the key does not expire.</span></span>

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

### <span data-ttu-id="3eba0-198">-HsmName</span><span class="sxs-lookup"><span data-stu-id="3eba0-198">-HsmName</span></span>
<span data-ttu-id="3eba0-199">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="3eba0-199">HSM name.</span></span> <span data-ttu-id="3eba0-200">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3eba0-200">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInteractiveImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-201">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="3eba0-201">-HsmObject</span></span>
<span data-ttu-id="3eba0-202">HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-202">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmInputObjectCreate, HsmInputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-203">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="3eba0-203">-HsmResourceId</span></span>
<span data-ttu-id="3eba0-204">Ressourcen-ID des HSM.</span><span class="sxs-lookup"><span data-stu-id="3eba0-204">Resource ID of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmResourceIdCreate, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-205">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3eba0-205">-InputObject</span></span>
<span data-ttu-id="3eba0-206">Vault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-206">Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectCreate, InputObjectImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-207">-KeyFilePassword</span><span class="sxs-lookup"><span data-stu-id="3eba0-207">-KeyFilePassword</span></span>
<span data-ttu-id="3eba0-208">Gibt ein Kennwort für die importierte Datei als **SecureString-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="3eba0-208">Specifies a password for the imported file as a **SecureString** object.</span></span> <span data-ttu-id="3eba0-209">Verwenden Sie zum **Abrufen eines SecureString-Objekts** **das Cmdlet ConvertTo-SecureString.**</span><span class="sxs-lookup"><span data-stu-id="3eba0-209">To obtain a **SecureString** object, use the **ConvertTo-SecureString** cmdlet.</span></span> <span data-ttu-id="3eba0-210">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help ConvertTo-SecureString` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="3eba0-210">For more information, type `Get-Help ConvertTo-SecureString`.</span></span> <span data-ttu-id="3eba0-211">Sie müssen dieses Kennwort angeben, um eine Datei mit der Dateinamenerweiterung PFX zu importieren.</span><span class="sxs-lookup"><span data-stu-id="3eba0-211">You must specify this password to import a file with a .pfx file name extension.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-212">-KeyFilePath</span><span class="sxs-lookup"><span data-stu-id="3eba0-212">-KeyFilePath</span></span>
<span data-ttu-id="3eba0-213">Gibt den Pfad einer lokalen Datei an, die Schlüsselmaterial enthält, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="3eba0-213">Specifies the path of a local file that contains key material that this cmdlet imports.</span></span>
<span data-ttu-id="3eba0-214">Die gültigen Dateinamenerweiterungen sind BYOK und PFX.</span><span class="sxs-lookup"><span data-stu-id="3eba0-214">The valid file name extensions are .byok and .pfx.</span></span>
- <span data-ttu-id="3eba0-215">Wenn es sich bei der Datei um eine byok-Datei handelt, wird der Schlüssel nach dem Import automatisch durch HSMs geschützt, und Sie können diesen Standard nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="3eba0-215">If the file is a .byok file, the key is automatically protected by HSMs after the import and you cannot override this default.</span></span>
- <span data-ttu-id="3eba0-216">Handelt es sich bei der Datei um eine PFX-Datei, wird der Schlüssel nach dem Import automatisch durch Software geschützt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-216">If the file is a .pfx file, the key is automatically protected by software after the import.</span></span> <span data-ttu-id="3eba0-217">Um diesen Standard außer Kraft zu setzen, legen Sie den *Zielparameter* auf HSM fest, damit der Schlüssel HSM-geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="3eba0-217">To override this default, set the *Destination* parameter to HSM so that the key is HSM-protected.</span></span>
<span data-ttu-id="3eba0-218">Wenn Sie diesen Parameter angeben, ist der *Parameter "Destination"* optional.</span><span class="sxs-lookup"><span data-stu-id="3eba0-218">When you specify this parameter, the *Destination* parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, HsmInteractiveImport, InputObjectImport, HsmInputObjectImport, ResourceIdImport, HsmResourceIdImport
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-219">-KeyOps</span><span class="sxs-lookup"><span data-stu-id="3eba0-219">-KeyOps</span></span>
<span data-ttu-id="3eba0-220">Gibt ein Array von Vorgängen an, die mit dem von diesem Cmdlet hinzugefügten Schlüssel ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3eba0-220">Specifies an array of operations that can be performed by using the key that this cmdlet adds.</span></span>
<span data-ttu-id="3eba0-221">Wenn Sie diesen Parameter nicht angeben, können alle Vorgänge ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3eba0-221">If you do not specify this parameter, all operations can be performed.</span></span>
<span data-ttu-id="3eba0-222">Bei den zulässigen Werten für diesen Parameter handelt es sich um eine durch Kommas getrennte Liste von Schlüsselvorgängen gemäß der [JSON Web Key (JWK)-Spezifikation:](http://go.microsoft.com/fwlink/?LinkID=613300)</span><span class="sxs-lookup"><span data-stu-id="3eba0-222">The acceptable values for this parameter are a comma-separated list of key operations as defined by the [JSON Web Key (JWK) specification](http://go.microsoft.com/fwlink/?LinkID=613300):</span></span>
- <span data-ttu-id="3eba0-223">Verschlüsseln</span><span class="sxs-lookup"><span data-stu-id="3eba0-223">encrypt</span></span>
- <span data-ttu-id="3eba0-224">entschlüsseln</span><span class="sxs-lookup"><span data-stu-id="3eba0-224">decrypt</span></span>
- <span data-ttu-id="3eba0-225">wrapKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-225">wrapKey</span></span>
- <span data-ttu-id="3eba0-226">unwrapKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-226">unwrapKey</span></span>
- <span data-ttu-id="3eba0-227">Signieren</span><span class="sxs-lookup"><span data-stu-id="3eba0-227">sign</span></span>
- <span data-ttu-id="3eba0-228">Überprüfen</span><span class="sxs-lookup"><span data-stu-id="3eba0-228">verify</span></span>
- <span data-ttu-id="3eba0-229">Importieren (nur für KEK siehe Beispiel 7)</span><span class="sxs-lookup"><span data-stu-id="3eba0-229">import (for KEK only, see example 7)</span></span>

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

### <span data-ttu-id="3eba0-230">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3eba0-230">-KeyType</span></span>
<span data-ttu-id="3eba0-231">Gibt den Schlüsseltyp dieses Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="3eba0-231">Specifies the key type of this key.</span></span> <span data-ttu-id="3eba0-232">Beim Importieren von BYOK-Schlüsseln wird standardmäßig "RSA" verwendet.</span><span class="sxs-lookup"><span data-stu-id="3eba0-232">When importing BYOK keys, it defaults to 'RSA'.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveImport, InputObjectImport, ResourceIdImport
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: HsmInteractiveCreate, HsmInputObjectCreate, HsmResourceIdCreate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-233">-Name</span><span class="sxs-lookup"><span data-stu-id="3eba0-233">-Name</span></span>
<span data-ttu-id="3eba0-234">Gibt den Namen des Schlüssels an, der dem Schlüsseltresor hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="3eba0-234">Specifies the name of the key to add to the key vault.</span></span> <span data-ttu-id="3eba0-235">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüssels basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3eba0-235">This cmdlet constructs the fully qualified domain name (FQDN) of a key based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span> <span data-ttu-id="3eba0-236">Der Name muss eine Zeichenfolge von 1 bis 63 Zeichen lang sein, die nur 0-9, a-z, A-Z und - (das Strichsymbol) enthält.</span><span class="sxs-lookup"><span data-stu-id="3eba0-236">The name must be a string of 1 through 63 characters in length that contains only 0-9, a-z, A-Z, and - (the dash symbol).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-237">-NotBefore</span><span class="sxs-lookup"><span data-stu-id="3eba0-237">-NotBefore</span></span>
<span data-ttu-id="3eba0-238">Gibt die Uhrzeit als **"DateTime"-Objekt** an, vor dem der Schlüssel nicht verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3eba0-238">Specifies the time, as a **DateTime** object, before which the key cannot be used.</span></span> <span data-ttu-id="3eba0-239">Dieser Parameter verwendet UTC.</span><span class="sxs-lookup"><span data-stu-id="3eba0-239">This parameter uses UTC.</span></span> <span data-ttu-id="3eba0-240">Verwenden Sie das Get-Date-Cmdlet, um **ein "DateTime"-Objekt** zu erhalten. </span><span class="sxs-lookup"><span data-stu-id="3eba0-240">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span> <span data-ttu-id="3eba0-241">Wenn Sie diesen Parameter nicht angeben, kann der Schlüssel sofort verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3eba0-241">If you do not specify this parameter, the key can be used immediately.</span></span>

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

### <span data-ttu-id="3eba0-242">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3eba0-242">-ResourceId</span></span>
<span data-ttu-id="3eba0-243">Vault Resource Id.</span><span class="sxs-lookup"><span data-stu-id="3eba0-243">Vault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdCreate, ResourceIdImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-244">-Size</span><span class="sxs-lookup"><span data-stu-id="3eba0-244">-Size</span></span>
<span data-ttu-id="3eba0-245">RSA-Schlüsselgröße in Bits.</span><span class="sxs-lookup"><span data-stu-id="3eba0-245">RSA key size, in bits.</span></span> <span data-ttu-id="3eba0-246">Wenn diese Angabe nicht angegeben ist, stellt der Dienst einen sicheren Standardwert zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="3eba0-246">If not specified, the service will provide a safe default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: InteractiveCreate, HsmInteractiveCreate, InputObjectCreate, HsmInputObjectCreate, ResourceIdCreate, HsmResourceIdCreate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-247">-Tag</span><span class="sxs-lookup"><span data-stu-id="3eba0-247">-Tag</span></span>
<span data-ttu-id="3eba0-248">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="3eba0-248">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3eba0-249">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="3eba0-249">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3eba0-250">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3eba0-250">-VaultName</span></span>
<span data-ttu-id="3eba0-251">Gibt den Namen des Schlüsseltresor an, dem dieses Cmdlet den Schlüssel hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-251">Specifies the name of the key vault to which this cmdlet adds the key.</span></span> <span data-ttu-id="3eba0-252">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="3eba0-252">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveCreate, InteractiveImport
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3eba0-253">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3eba0-253">-Confirm</span></span>
<span data-ttu-id="3eba0-254">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3eba0-254">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3eba0-255">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3eba0-255">-WhatIf</span></span>
<span data-ttu-id="3eba0-256">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3eba0-256">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3eba0-257">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3eba0-257">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3eba0-258">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3eba0-258">CommonParameters</span></span>
<span data-ttu-id="3eba0-259">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3eba0-259">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3eba0-260">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3eba0-260">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3eba0-261">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3eba0-261">INPUTS</span></span>

### <span data-ttu-id="3eba0-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3eba0-262">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3eba0-263">System.String</span><span class="sxs-lookup"><span data-stu-id="3eba0-263">System.String</span></span>

## <span data-ttu-id="3eba0-264">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3eba0-264">OUTPUTS</span></span>

### <span data-ttu-id="3eba0-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

## <span data-ttu-id="3eba0-266">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3eba0-266">NOTES</span></span>

## <span data-ttu-id="3eba0-267">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3eba0-267">RELATED LINKS</span></span>

[<span data-ttu-id="3eba0-268">Backup-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-268">Backup-AzKeyVaultKey</span></span>](./Backup-AzKeyVaultKey.md)

[<span data-ttu-id="3eba0-269">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-269">Get-AzKeyVaultKey</span></span>](./Get-AzKeyVaultKey.md)

[<span data-ttu-id="3eba0-270">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="3eba0-270">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="3eba0-271">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="3eba0-271">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)
