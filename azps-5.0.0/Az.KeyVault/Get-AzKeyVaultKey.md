---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: 515a238aa7e6bb49117dd38954dbb67f840abd9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178867"
---
# <span data-ttu-id="d7045-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7045-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="d7045-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d7045-102">SYNOPSIS</span></span>
<span data-ttu-id="d7045-103">Ruft schlüsseltresor Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="d7045-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d7045-104">SYNTAX</span></span>

### <span data-ttu-id="d7045-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d7045-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="d7045-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d7045-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="d7045-108">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-109">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="d7045-109">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-110">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d7045-110">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="d7045-111">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-112">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="d7045-112">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d7045-113">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="d7045-113">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7045-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d7045-114">DESCRIPTION</span></span>
<span data-ttu-id="d7045-115">Das Cmdlet " **Get-AzKeyVaultKey** " ruft Azure Key Vault-Schlüssel ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-115">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="d7045-116">Dieses Cmdlet ruft ein bestimmtes **Microsoft. Azure. Commands. keyvault. Models. keybundle** oder eine Liste aller **keybundle** -Objekte in einem schlüsseltresor oder nach Version ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-116">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="d7045-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d7045-117">EXAMPLES</span></span>

### <span data-ttu-id="d7045-118">Beispiel 1: Abrufen aller Schlüssel in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="d7045-118">Example 1: Get all the keys in a key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso'

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d7045-119">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-119">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7045-120">Beispiel 2: Abrufen der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7045-120">Example 2: Get the current version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1'

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d7045-121">Dieser Befehl ruft die aktuelle Version des Schlüssels mit dem Namen test1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-121">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7045-122">Beispiel 3: Abrufen aller Versionen eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7045-122">Example 3: Get all versions of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -IncludeVersions

Vault Name     : contoso
Name           : test1
Version        : 7fe415d5518240c1a6fce89986b8d334
Id             : https://contoso.vault.azure.net:443/keys/test1/7fe415d5518240c1a6fce89986b8d334
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d7045-123">Dieser Befehl ruft alle Versionen mit dem Schlüssel namens ITPfx im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-123">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7045-124">Beispiel 4: Abrufen einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="d7045-124">Example 4: Get a specific version of a key</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test1' -Version 'e4e95940e669407fbdb4298bc21a3e1d'

Vault Name     : contoso
Name           : test1
Version        : e4e95940e669407fbdb4298bc21a3e1d
Id             : https://contoso.vault.azure.net:443/keys/test1/e4e95940e669407fbdb4298bc21a3e1d
Enabled        : False
Expires        : 11/24/2018 6:08:08 PM
Not Before     : 5/24/2018 5:58:08 PM
Created        : 5/24/2018 6:08:08 PM
Updated        : 5/24/2018 6:08:08 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d7045-125">Dieser Befehl ruft eine bestimmte Version des Schlüssels mit dem Namen test1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-125">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="d7045-126">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels überprüfen, indem Sie im $Key-Objekt navigieren.</span><span class="sxs-lookup"><span data-stu-id="d7045-126">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="d7045-127">Beispiel 5: Abrufen aller Schlüssel, die gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurden</span><span class="sxs-lookup"><span data-stu-id="d7045-127">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d7045-128">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="d7045-128">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="d7045-129">Beispiel 6: Ruft den Schlüssel ITPfx ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="d7045-129">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName 'test3' -InRemovedState

Vault Name           : contoso
Name                 : test3
Id                   : https://contoso.vault.azure.net:443/keys/test3/1af807cc331a49d0b52b7c75e1b2366e
Deleted Date         : 5/24/2018 8:32:42 PM
Scheduled Purge Date : 8/22/2018 8:32:42 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 5/24/2018 8:32:27 PM
Updated              : 5/24/2018 8:32:27 PM
Purge Disabled       : False
Tags                 :
```

<span data-ttu-id="d7045-130">Dieser Befehl ruft den Schlüssel test3 ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="d7045-130">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="d7045-131">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="d7045-131">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="d7045-132">Beispiel 7: Abrufen aller Schlüssel in einem schlüsseltresor mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="d7045-132">Example 7: Get all the keys in a key vault using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultKey -VaultName 'contoso' -KeyName "test*"

Vault Name     : contoso
Name           : test1
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test1
Enabled        : True
Expires        : 11/24/2018 6:08:13 PM
Not Before     : 5/24/2018 5:58:13 PM
Created        : 5/24/2018 6:08:13 PM
Updated        : 5/24/2018 6:08:13 PM
Purge Disabled : False
Tags           :

Vault Name     : contoso
Name           : test2
Version        :
Id             : https://contoso.vault.azure.net:443/keys/test2
Enabled        : True
Expires        : 11/24/2018 6:09:44 PM
Not Before     : 5/24/2018 5:59:44 PM
Created        : 5/24/2018 6:09:44 PM
Updated        : 5/24/2018 6:09:44 PM
Purge Disabled : False
Tags           :
```

<span data-ttu-id="d7045-133">Dieser Befehl ruft alle Schlüssel im schlüsseltresor mit dem Namen "Contoso" ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="d7045-133">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="d7045-134">Beispiel 8: Herunterladen eines öffentlichen Schlüssels als PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="d7045-134">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="d7045-135">Sie können den öffentlichen Schlüssel eines RSA-Schlüssels herunterladen, indem Sie den `-OutFile` Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="d7045-135">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="d7045-136">Dies ist ein Schritt beim Importieren von HSM-geschützten Schlüsseln in Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="d7045-136">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="d7045-137">Sieh https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="d7045-137">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="d7045-138">Parameter</span><span class="sxs-lookup"><span data-stu-id="d7045-138">PARAMETERS</span></span>

### <span data-ttu-id="d7045-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7045-139">-DefaultProfile</span></span>
<span data-ttu-id="d7045-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d7045-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7045-141">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="d7045-141">-IncludeVersions</span></span>
<span data-ttu-id="d7045-142">Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="d7045-142">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="d7045-143">Die aktuelle Version eines Schlüssels ist der erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="d7045-143">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="d7045-144">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="d7045-144">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="d7045-145">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="d7045-145">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, ByInputObjectKeyVersions, ByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-146">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d7045-146">-InputObject</span></span>
<span data-ttu-id="d7045-147">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d7045-147">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectKeyName, ByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-148">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="d7045-148">-InRemovedState</span></span>
<span data-ttu-id="d7045-149">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d7045-149">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-150">-Name</span><span class="sxs-lookup"><span data-stu-id="d7045-150">-Name</span></span>
<span data-ttu-id="d7045-151">Gibt den Namen des abzurufenden Schlüsselpakets an.</span><span class="sxs-lookup"><span data-stu-id="d7045-151">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-152">-Datei</span><span class="sxs-lookup"><span data-stu-id="d7045-152">-OutFile</span></span>
<span data-ttu-id="d7045-153">Gibt die Ausgabedatei an, für die dieses Cmdlet den Schlüssel speichert.</span><span class="sxs-lookup"><span data-stu-id="d7045-153">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="d7045-154">Der öffentliche Schlüssel wird standardmäßig im PEM-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d7045-154">The public key is saved in PEM format by default.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-155">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="d7045-155">-ResourceId</span></span>
<span data-ttu-id="d7045-156">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d7045-156">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdKeyName, ByResourceIdKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-157">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="d7045-157">-VaultName</span></span>
<span data-ttu-id="d7045-158">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="d7045-158">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="d7045-159">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="d7045-159">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByKeyName, ByKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-160">-Version</span><span class="sxs-lookup"><span data-stu-id="d7045-160">-Version</span></span>
<span data-ttu-id="d7045-161">Gibt die Schlüssel Version an.</span><span class="sxs-lookup"><span data-stu-id="d7045-161">Specifies the key version.</span></span>
<span data-ttu-id="d7045-162">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüssel Version.</span><span class="sxs-lookup"><span data-stu-id="d7045-162">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByInputObjectKeyName, ByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d7045-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7045-163">CommonParameters</span></span>
<span data-ttu-id="d7045-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7045-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7045-165">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7045-165">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7045-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d7045-166">INPUTS</span></span>

### <span data-ttu-id="d7045-167">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="d7045-167">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="d7045-168">System. String</span><span class="sxs-lookup"><span data-stu-id="d7045-168">System.String</span></span>

## <span data-ttu-id="d7045-169">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d7045-169">OUTPUTS</span></span>

### <span data-ttu-id="d7045-170">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d7045-170">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d7045-171">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7045-171">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="d7045-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="d7045-172">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="d7045-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7045-173">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="d7045-174">Notizen</span><span class="sxs-lookup"><span data-stu-id="d7045-174">NOTES</span></span>

## <span data-ttu-id="d7045-175">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d7045-175">RELATED LINKS</span></span>

[<span data-ttu-id="d7045-176">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7045-176">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="d7045-177">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="d7045-177">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="d7045-178">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="d7045-178">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="d7045-179">Satz-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="d7045-179">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

