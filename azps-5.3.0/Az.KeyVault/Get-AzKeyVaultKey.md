---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2BE34AE1-06FA-4F66-8FDB-CED22C2E0978
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultKey.md
ms.openlocfilehash: fa53affab7fe530defcf23f169458ee6813722a1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472360"
---
# <span data-ttu-id="8821b-101">Get-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8821b-101">Get-AzKeyVaultKey</span></span>

## <span data-ttu-id="8821b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8821b-102">SYNOPSIS</span></span>
<span data-ttu-id="8821b-103">Ruft Die Schlüssel des Tresors ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-103">Gets Key Vault keys.</span></span>

## <span data-ttu-id="8821b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8821b-104">SYNTAX</span></span>

### <span data-ttu-id="8821b-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8821b-105">ByVaultName (Default)</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-106">ByKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-106">ByKeyName</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-107">ByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-107">ByKeyVersions</span></span>
```
Get-AzKeyVaultKey [-VaultName] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-108">HsmByKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-108">HsmByKeyName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-109">HsmByVaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-109">HsmByVaultName</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-110">HsmByKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-110">HsmByKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmName <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-111">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-111">ByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-112">ByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-112">ByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-113">ByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-113">ByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-114">HsmByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-114">HsmByInputObjectVaultName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-115">HsmByInputObjectKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-115">HsmByInputObjectKeyName</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-116">HsmByInputObjectKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-116">HsmByInputObjectKeyVersions</span></span>
```
Get-AzKeyVaultKey [-HsmObject] <PSManagedHsm> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-117">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-117">ByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-118">ByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-118">ByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-119">ByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-119">ByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey [-ResourceId] <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-120">HsmByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-120">HsmByResourceIdVaultName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [[-Name] <String>] [-InRemovedState] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-121">HsmByResourceIdKeyName</span><span class="sxs-lookup"><span data-stu-id="8821b-121">HsmByResourceIdKeyName</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-Version] <String> [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8821b-122">HsmByResourceIdKeyVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-122">HsmByResourceIdKeyVersions</span></span>
```
Get-AzKeyVaultKey -HsmResourceId <String> [-Name] <String> [-IncludeVersions] [-OutFile <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8821b-123">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8821b-123">DESCRIPTION</span></span>
<span data-ttu-id="8821b-124">Das **Cmdlet "Get-AzKeyVaultKey"** ruft Azure Key Vault Keys ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-124">The **Get-AzKeyVaultKey** cmdlet gets Azure Key Vault keys.</span></span>
<span data-ttu-id="8821b-125">Dieses Cmdlet ruft ein bestimmtes **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** oder eine Liste aller **KeyBundle-Objekte** in einem Schlüsseltresor oder nach Version ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-125">This cmdlet gets a specific **Microsoft.Azure.Commands.KeyVault.Models.KeyBundle** or a list of all **KeyBundle** objects in a key vault or by version.</span></span>

## <span data-ttu-id="8821b-126">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8821b-126">EXAMPLES</span></span>

### <span data-ttu-id="8821b-127">Beispiel 1: Alle Schlüssel in einem Schlüsseltresor erhalten</span><span class="sxs-lookup"><span data-stu-id="8821b-127">Example 1: Get all the keys in a key vault</span></span>
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

<span data-ttu-id="8821b-128">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor namens Contoso ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-128">This command gets all the keys in the key vault named Contoso.</span></span>

### <span data-ttu-id="8821b-129">Beispiel 2: Erhalten der aktuellen Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8821b-129">Example 2: Get the current version of a key</span></span>
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

<span data-ttu-id="8821b-130">Dieser Befehl ruft die aktuelle Version des Schlüssels namens "Test1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-130">This command gets the current version of the key named test1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="8821b-131">Beispiel 3: Alle Versionen eines Schlüssels erhalten</span><span class="sxs-lookup"><span data-stu-id="8821b-131">Example 3: Get all versions of a key</span></span>
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

<span data-ttu-id="8821b-132">Dieser Befehl ruft alle Versionen ab, die den Schlüssel "ITPfx" im Schlüsseltresor "Contoso" haben.</span><span class="sxs-lookup"><span data-stu-id="8821b-132">This command gets all versions the key named ITPfx in the key vault named Contoso.</span></span>

### <span data-ttu-id="8821b-133">Beispiel 4: Erhalten einer bestimmten Version eines Schlüssels</span><span class="sxs-lookup"><span data-stu-id="8821b-133">Example 4: Get a specific version of a key</span></span>
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

<span data-ttu-id="8821b-134">Dieser Befehl ruft eine bestimmte Version des Schlüssels namens "Test1" im Schlüsseltresor "Contoso" ab.</span><span class="sxs-lookup"><span data-stu-id="8821b-134">This command gets a specific version of the key named test1 in the key vault named Contoso.</span></span>
<span data-ttu-id="8821b-135">Nachdem Sie diesen Befehl ausgeführt haben, können Sie verschiedene Eigenschaften des Schlüssels prüfen, indem Sie im $Key navigieren.</span><span class="sxs-lookup"><span data-stu-id="8821b-135">After running this command, you can inspect various properties of the key by navigating the $Key object.</span></span>

### <span data-ttu-id="8821b-136">Beispiel 5: Alle Schlüssel für diesen Schlüsseltresor erhalten, die gelöscht, aber nicht gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="8821b-136">Example 5: Get all the keys that have been deleted but not purged for this key vault</span></span>
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

<span data-ttu-id="8821b-137">Dieser Befehl ruft alle Schlüssel ab, die zuvor gelöscht, aber nicht gelöscht wurden, im Schlüsseltresor "Contoso".</span><span class="sxs-lookup"><span data-stu-id="8821b-137">This command gets all the keys that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="8821b-138">Beispiel 6: Ruft den wichtigsten ITPfx-Server ab, der gelöscht, aber nicht für diesen Schlüsseltresor gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="8821b-138">Example 6: Gets the key ITPfx that has been deleted but not purged for this key vault.</span></span>
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

<span data-ttu-id="8821b-139">Dieser Befehl ruft den Schlüsseltest3 ab, der zuvor im Schlüsseltresor "Contoso" gelöscht, aber nicht gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="8821b-139">This command gets the key test3 that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="8821b-140">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum dieses gelöschten Schlüssels zurück.</span><span class="sxs-lookup"><span data-stu-id="8821b-140">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted key.</span></span>

### <span data-ttu-id="8821b-141">Beispiel 7: Erhalten aller Schlüssel in einem Schlüsseltresor mithilfe der Filterung</span><span class="sxs-lookup"><span data-stu-id="8821b-141">Example 7: Get all the keys in a key vault using filtering</span></span>
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

<span data-ttu-id="8821b-142">Dieser Befehl ruft alle Schlüssel im Schlüsseltresor "Contoso" ab, die mit "Test" beginnen.</span><span class="sxs-lookup"><span data-stu-id="8821b-142">This command gets all the keys in the key vault named Contoso that start with "test".</span></span>

### <span data-ttu-id="8821b-143">Beispiel 8: Herunterladen eines öffentlichen Schlüssels als PEM-Datei</span><span class="sxs-lookup"><span data-stu-id="8821b-143">Example 8: Download a public key as a .pem file</span></span>

```powershell
PS C:\> $path = "D:\public.pem"
PS C:\> Get-AzKeyVaultKey -VaultName $vaultName -KeyName $keyName -OutFile $path
```

<span data-ttu-id="8821b-144">Sie können den öffentlichen Schlüssel eines RSA-Schlüssels herunterladen, indem Sie den Parameter `-OutFile` angeben.</span><span class="sxs-lookup"><span data-stu-id="8821b-144">You can download the public key of a RSA key by specifying the `-OutFile` parameter.</span></span>
<span data-ttu-id="8821b-145">Dies ist ein Schritt beim Importieren von HSM-geschützten Schlüsseln in den Azure Key Vault.</span><span class="sxs-lookup"><span data-stu-id="8821b-145">This is one step of importing HSM-protected keys to Azure Key Vault.</span></span> <span data-ttu-id="8821b-146">Sieh https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span><span class="sxs-lookup"><span data-stu-id="8821b-146">See https://docs.microsoft.com/en-us/azure/key-vault/keys/hsm-protected-keys</span></span>

## <span data-ttu-id="8821b-147">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8821b-147">PARAMETERS</span></span>

### <span data-ttu-id="8821b-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8821b-148">-DefaultProfile</span></span>
<span data-ttu-id="8821b-149">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8821b-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8821b-150">-HsmName</span><span class="sxs-lookup"><span data-stu-id="8821b-150">-HsmName</span></span>
<span data-ttu-id="8821b-151">HSM-Name.</span><span class="sxs-lookup"><span data-stu-id="8821b-151">HSM name.</span></span> <span data-ttu-id="8821b-152">Das Cmdlet erstellt den FQDN eines verwalteten HSM basierend auf dem Namen und der aktuell ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8821b-152">Cmdlet constructs the FQDN of a managed HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByKeyName, HsmByVaultName, HsmByKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-153">-HsmObject</span><span class="sxs-lookup"><span data-stu-id="8821b-153">-HsmObject</span></span>
<span data-ttu-id="8821b-154">HSM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8821b-154">HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: HsmByInputObjectVaultName, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-155">-HsmResourceId</span><span class="sxs-lookup"><span data-stu-id="8821b-155">-HsmResourceId</span></span>
<span data-ttu-id="8821b-156">HSM-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8821b-156">HSM Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: HsmByResourceIdVaultName, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-157">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="8821b-157">-IncludeVersions</span></span>
<span data-ttu-id="8821b-158">Gibt an, dass dieses Cmdlet alle Versionen eines Schlüssels erhält.</span><span class="sxs-lookup"><span data-stu-id="8821b-158">Indicates that this cmdlet gets all versions of a key.</span></span>
<span data-ttu-id="8821b-159">Die aktuelle Version eines Schlüssels ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="8821b-159">The current version of a key is the first one on the list.</span></span>
<span data-ttu-id="8821b-160">Wenn Sie diesen Parameter angeben, müssen Sie auch die *Parameter "Name"* und *"VaultName"* angeben.</span><span class="sxs-lookup"><span data-stu-id="8821b-160">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="8821b-161">Wenn Sie den Parameter *"IncludeVersions"* nicht angeben, ruft dieses Cmdlet die aktuelle Version des Schlüssels mit dem angegebenen *Namen ab.*</span><span class="sxs-lookup"><span data-stu-id="8821b-161">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the key with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByKeyVersions, HsmByKeyVersions, ByInputObjectKeyVersions, HsmByInputObjectKeyVersions, ByResourceIdKeyVersions, HsmByResourceIdKeyVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-162">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8821b-162">-InputObject</span></span>
<span data-ttu-id="8821b-163">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8821b-163">KeyVault object.</span></span>

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

### <span data-ttu-id="8821b-164">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="8821b-164">-InRemovedState</span></span>
<span data-ttu-id="8821b-165">Gibt an, ob die zuvor gelöschten Schlüssel in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8821b-165">Specifies whether to show the previously deleted keys in the output</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-166">-Name</span><span class="sxs-lookup"><span data-stu-id="8821b-166">-Name</span></span>
<span data-ttu-id="8821b-167">Gibt den Namen des zu erhaltenden Schlüsselbündels an.</span><span class="sxs-lookup"><span data-stu-id="8821b-167">Specifies the name of the key bundle to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, HsmByVaultName, ByInputObjectVaultName, HsmByInputObjectVaultName, ByResourceIdVaultName, HsmByResourceIdVaultName
Aliases: KeyName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ByKeyName, ByKeyVersions, HsmByKeyName, HsmByKeyVersions, ByInputObjectKeyName, ByInputObjectKeyVersions, HsmByInputObjectKeyName, HsmByInputObjectKeyVersions, ByResourceIdKeyName, ByResourceIdKeyVersions, HsmByResourceIdKeyName, HsmByResourceIdKeyVersions
Aliases: KeyName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="8821b-168">-OutFile</span><span class="sxs-lookup"><span data-stu-id="8821b-168">-OutFile</span></span>
<span data-ttu-id="8821b-169">Gibt die Ausgabedatei an, für die dieser Schlüssel von diesem Cmdlet gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8821b-169">Specifies the output file for which this cmdlet saves the key.</span></span> <span data-ttu-id="8821b-170">Der öffentliche Schlüssel wird standardmäßig im PEM-Format gespeichert.</span><span class="sxs-lookup"><span data-stu-id="8821b-170">The public key is saved in PEM format by default.</span></span>

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

### <span data-ttu-id="8821b-171">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8821b-171">-ResourceId</span></span>
<span data-ttu-id="8821b-172">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8821b-172">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="8821b-173">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8821b-173">-VaultName</span></span>
<span data-ttu-id="8821b-174">Gibt den Namen des Schlüsseltresor an, aus dem dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="8821b-174">Specifies the name of the key vault from which this cmdlet gets keys.</span></span>
<span data-ttu-id="8821b-175">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und der ausgewählten Umgebung.</span><span class="sxs-lookup"><span data-stu-id="8821b-175">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your selected environment.</span></span>

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

### <span data-ttu-id="8821b-176">-Version</span><span class="sxs-lookup"><span data-stu-id="8821b-176">-Version</span></span>
<span data-ttu-id="8821b-177">Gibt die Schlüsselversion an.</span><span class="sxs-lookup"><span data-stu-id="8821b-177">Specifies the key version.</span></span>
<span data-ttu-id="8821b-178">Dieses Cmdlet erstellt den FQDN eines Schlüssels basierend auf dem Namen des Schlüsseltresor, der aktuell ausgewählten Umgebung, dem Schlüsselnamen und der Schlüsselversion.</span><span class="sxs-lookup"><span data-stu-id="8821b-178">This cmdlet constructs the FQDN of a key based on the key vault name, your currently selected environment, the key name, and the key version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByKeyName, HsmByKeyName, ByInputObjectKeyName, HsmByInputObjectKeyName, ByResourceIdKeyName, HsmByResourceIdKeyName
Aliases: KeyVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8821b-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8821b-179">CommonParameters</span></span>
<span data-ttu-id="8821b-180">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8821b-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8821b-181">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8821b-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8821b-182">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8821b-182">INPUTS</span></span>

### <span data-ttu-id="8821b-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8821b-183">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8821b-184">System.String</span><span class="sxs-lookup"><span data-stu-id="8821b-184">System.String</span></span>

## <span data-ttu-id="8821b-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8821b-185">OUTPUTS</span></span>

### <span data-ttu-id="8821b-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8821b-186">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="8821b-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8821b-187">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultKey</span></span>

### <span data-ttu-id="8821b-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span><span class="sxs-lookup"><span data-stu-id="8821b-188">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKeyIdentityItem</span></span>

### <span data-ttu-id="8821b-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8821b-189">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultKey</span></span>

## <span data-ttu-id="8821b-190">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8821b-190">NOTES</span></span>

## <span data-ttu-id="8821b-191">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8821b-191">RELATED LINKS</span></span>

[<span data-ttu-id="8821b-192">Add-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8821b-192">Add-AzKeyVaultKey</span></span>](./Add-AzKeyVaultKey.md)

[<span data-ttu-id="8821b-193">Remove-AzKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="8821b-193">Remove-AzKeyVaultKey</span></span>](./Remove-AzKeyVaultKey.md)

[<span data-ttu-id="8821b-194">Undo-AzKeyVaultKeyRemoval</span><span class="sxs-lookup"><span data-stu-id="8821b-194">Undo-AzKeyVaultKeyRemoval</span></span>](./Undo-AzKeyVaultKeyRemoval.md)

[<span data-ttu-id="8821b-195">Set-AzKeyVaultKeyAttribute</span><span class="sxs-lookup"><span data-stu-id="8821b-195">Set-AzKeyVaultKeyAttribute</span></span>](./Set-AzKeyVaultKeyAttribute.md)

