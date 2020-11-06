---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 8C9B33EE-10DE-4803-B76D-FE9FC2AC3372
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurekeyvaultsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureKeyVaultSecret.md
ms.openlocfilehash: aa8306070eb560deb465cbaa9ddae2bce24c5600
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502090"
---
# <span data-ttu-id="eaa27-101">Get-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eaa27-101">Get-AzureKeyVaultSecret</span></span>

## <span data-ttu-id="eaa27-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="eaa27-102">SYNOPSIS</span></span>
<span data-ttu-id="eaa27-103">Ruft die Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-103">Gets the secrets in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eaa27-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="eaa27-104">SYNTAX</span></span>

### <span data-ttu-id="eaa27-105">ByVaultName (Standard)</span><span class="sxs-lookup"><span data-stu-id="eaa27-105">ByVaultName (Default)</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-106">BySecretName</span><span class="sxs-lookup"><span data-stu-id="eaa27-106">BySecretName</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-107">BySecretVersions</span><span class="sxs-lookup"><span data-stu-id="eaa27-107">BySecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-VaultName] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-108">ByInputObjectVaultName</span><span class="sxs-lookup"><span data-stu-id="eaa27-108">ByInputObjectVaultName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-109">ByInputObjectSecretName</span><span class="sxs-lookup"><span data-stu-id="eaa27-109">ByInputObjectSecretName</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-110">ByInputObjectSecretVersions</span><span class="sxs-lookup"><span data-stu-id="eaa27-110">ByInputObjectSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-InputObject] <PSKeyVault> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-111">ByResourceIdVaultName</span><span class="sxs-lookup"><span data-stu-id="eaa27-111">ByResourceIdVaultName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [[-Name] <String>] [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-112">ByResourceIdSecretName</span><span class="sxs-lookup"><span data-stu-id="eaa27-112">ByResourceIdSecretName</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eaa27-113">ByResourceIdSecretVersions</span><span class="sxs-lookup"><span data-stu-id="eaa27-113">ByResourceIdSecretVersions</span></span>
```
Get-AzureKeyVaultSecret [-ResourceId] <String> [-Name] <String> [-IncludeVersions]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eaa27-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="eaa27-114">DESCRIPTION</span></span>
<span data-ttu-id="eaa27-115">Das Cmdlet " **Get-AzureKeyVaultSecret** " erhält in einem schlüsseltresor Geheimnisse.</span><span class="sxs-lookup"><span data-stu-id="eaa27-115">The **Get-AzureKeyVaultSecret** cmdlet gets secrets in a key vault.</span></span>
<span data-ttu-id="eaa27-116">Dieses Cmdlet ruft einen bestimmten geheimen oder alle Geheimnisse in einem schlüsseltresor ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-116">This cmdlet gets a specific secret or all the secrets in a key vault.</span></span>

## <span data-ttu-id="eaa27-117">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eaa27-117">EXAMPLES</span></span>

### <span data-ttu-id="eaa27-118">Beispiel 1: Abrufen aller aktuellen Versionen aller Geheimnisse in einem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="eaa27-118">Example 1: Get all current versions of all secrets in a key vault</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso'

Vault Name   : contoso
Name         : secret1
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret1
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret2
Version      :
Id           : https://contoso.vault.azure.net:443/secrets/secret2
Enabled      : True
Expires      :
Not Before   :
Created      : 4/11/2018 11:45:06 PM
Updated      : 4/11/2018 11:45:06 PM
Content Type :
Tags         :
```

<span data-ttu-id="eaa27-119">Mit diesem Befehl werden die aktuellen Versionen aller Geheimnisse im schlüsseltresor mit dem Namen contoso abgerufen.</span><span class="sxs-lookup"><span data-stu-id="eaa27-119">This command gets the current versions of all secrets in the key vault named Contoso.</span></span>

### <span data-ttu-id="eaa27-120">Beispiel 2: Abrufen aller Versionen eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="eaa27-120">Example 2: Get all versions of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -IncludeVersions

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="eaa27-121">Dieser Befehl ruft alle Versionen des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-121">This command gets all versions of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="eaa27-122">Beispiel 3: Abrufen der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="eaa27-122">Example 3: Get the current version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1'

Vault Name   : contoso
Name         : secret1
Version      : 7128133570f84a71b48d7d0550deb74c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/7128133570f84a71b48d7d0550deb74c
Enabled      : True
Expires      : 4/6/2018 3:59:43 PM
Not Before   :
Created      : 4/5/2018 11:46:28 PM
Updated      : 4/6/2018 11:30:17 PM
Content Type :
Tags         :
```

<span data-ttu-id="eaa27-123">Dieser Befehl ruft die aktuelle Version des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-123">This command gets the current version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="eaa27-124">Beispiel 4: Abrufen einer bestimmten Version eines bestimmten Geheimnisses</span><span class="sxs-lookup"><span data-stu-id="eaa27-124">Example 4: Get a specific version of a specific secret</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'secret1' -Version '5d1a74ba2c454439886fb8509b6cab3c'

Vault Name   : contoso
Name         : secret1
Version      : 5d1a74ba2c454439886fb8509b6cab3c
Id           : https://contoso.vault.azure.net:443/secrets/secret1/5d1a74ba2c454439886fb8509b6cab3c
Enabled      : True
Expires      :
Not Before   :
Created      : 4/5/2018 11:44:50 PM
Updated      : 4/5/2018 11:44:50 PM
Content Type :
Tags         :
```

<span data-ttu-id="eaa27-125">Dieser Befehl ruft eine bestimmte Version des geheimen namens secret1 im schlüsseltresor mit dem Namen contoso ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-125">This command gets a specific version of the secret named secret1 in the key vault named Contoso.</span></span>

### <span data-ttu-id="eaa27-126">Beispiel 5: Abrufen des nur-Text-Werts der aktuellen Version eines bestimmten geheimen Schlüssels</span><span class="sxs-lookup"><span data-stu-id="eaa27-126">Example 5: Get the plain text value of the current version of a specific secret</span></span>
```powershell
PS C:\> $secret = Get-AzureKeyVaultSecret -VaultName 'Contoso' -Name 'ITSecret'
PS C:\> Write-Host "Secret Value is:" $secret.SecretValueText

Secret Value is: P@ssw0rd
```

<span data-ttu-id="eaa27-127">Diese Befehle rufen die aktuelle Version eines geheimen namens ITSecret ab und zeigen dann den nur-Text-Wert dieses geheimen Schlüssels an.</span><span class="sxs-lookup"><span data-stu-id="eaa27-127">These commands get the current version of a secret named ITSecret, and then displays the plain text value of that secret.</span></span>

### <span data-ttu-id="eaa27-128">Beispiel 6: Abrufen aller für diesen schlüsseltresor gelöschten, aber nicht bereinigten Geheimnisse</span><span class="sxs-lookup"><span data-stu-id="eaa27-128">Example 6: Get all the secrets that have been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Id                   : https://contoso.vault.azure.net:443/secrets/secret1
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :

Vault Name           : contoso
Name                 : secret2
Id                   : https://contoso.vault.azure.net:443/secrets/secret2
Deleted Date         : 5/7/2018 7:56:34 PM
Scheduled Purge Date : 8/5/2018 7:56:34 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/6/2018 8:39:15 PM
Updated              : 4/6/2018 10:11:24 PM
Content Type         : 
Tags                 :
```

<span data-ttu-id="eaa27-129">Dieser Befehl ruft alle Geheimnisse ab, die zuvor gelöscht, aber nicht bereinigt wurden, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="eaa27-129">This command gets all the secrets that have been previously deleted, but not purged, in the key vault named Contoso.</span></span>

### <span data-ttu-id="eaa27-130">Beispiel 7: Ruft den geheimen ITSecret ab, der gelöscht, aber für diesen schlüsseltresor nicht bereinigt wurde.</span><span class="sxs-lookup"><span data-stu-id="eaa27-130">Example 7: Gets the secret ITSecret that has been deleted but not purged for this key vault.</span></span>
```powershell
PS C:\> Get-AzureKeyVaultSecret -VaultName 'Contoso' -KeyName 'secret1' -InRemovedState

Vault Name           : contoso
Name                 : secret1
Version              : 689d23346e9c42a2a64f4e3d75094dcc
Id                   : https://contoso.vault.azure.net:443/secrets/secret1/689d23346e9c42a2a64f4e3d75094dcc
Deleted Date         : 4/4/2018 8:51:58 PM
Scheduled Purge Date : 7/3/2018 8:51:58 PM
Enabled              : True
Expires              :
Not Before           :
Created              : 4/4/2018 8:51:03 PM
Updated              : 4/4/2018 8:51:03 PM
Content Type         :
Tags                 :
```

<span data-ttu-id="eaa27-131">Dieser Befehl ruft den geheimen "secret1" ab, der zuvor gelöscht, aber nicht bereinigt wurde, im schlüsseltresor mit dem Namen contoso.</span><span class="sxs-lookup"><span data-stu-id="eaa27-131">This command gets the secret 'secret1' that has been previously deleted, but not purged, in the key vault named Contoso.</span></span>
<span data-ttu-id="eaa27-132">Dieser Befehl gibt Metadaten wie das Löschdatum und das geplante Löschdatum für diesen gelöschten Schlüssel zurück.</span><span class="sxs-lookup"><span data-stu-id="eaa27-132">This command will return metadata such as the deletion date, and the scheduled purging date of this deleted secret.</span></span>

## <span data-ttu-id="eaa27-133">Parameter</span><span class="sxs-lookup"><span data-stu-id="eaa27-133">PARAMETERS</span></span>

### <span data-ttu-id="eaa27-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eaa27-134">-DefaultProfile</span></span>
<span data-ttu-id="eaa27-135">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="eaa27-135">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="eaa27-136">-IncludeVersions</span><span class="sxs-lookup"><span data-stu-id="eaa27-136">-IncludeVersions</span></span>
<span data-ttu-id="eaa27-137">Gibt an, dass dieses Cmdlet alle Versionen eines geheimen Schlüssels abruft.</span><span class="sxs-lookup"><span data-stu-id="eaa27-137">Indicates that this cmdlet gets all versions of a secret.</span></span>
<span data-ttu-id="eaa27-138">Die aktuelle Version eines Geheimnisses ist die erste in der Liste.</span><span class="sxs-lookup"><span data-stu-id="eaa27-138">The current version of a secret is the first one on the list.</span></span>
<span data-ttu-id="eaa27-139">Wenn Sie diesen Parameter angeben, müssen Sie auch die Parameter *Name* und *vaultname* angeben.</span><span class="sxs-lookup"><span data-stu-id="eaa27-139">If you specify this parameter you must also specify the *Name* and *VaultName* parameters.</span></span>
<span data-ttu-id="eaa27-140">Wenn Sie den *IncludeVersions* -Parameter nicht angeben, ruft dieses Cmdlet die aktuelle Version des geheimen Schlüssels mit dem angegebenen *Namen* ab.</span><span class="sxs-lookup"><span data-stu-id="eaa27-140">If you do not specify the *IncludeVersions* parameter, this cmdlet gets the current version of the secret with the specified *Name*.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: BySecretVersions, ByInputObjectSecretVersions, ByResourceIdSecretVersions
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-141">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="eaa27-141">-InputObject</span></span>
<span data-ttu-id="eaa27-142">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="eaa27-142">KeyVault Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByInputObjectVaultName, ByInputObjectSecretName, ByInputObjectSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-143">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="eaa27-143">-InRemovedState</span></span>
<span data-ttu-id="eaa27-144">Gibt an, ob die zuvor gelöschten Geheimnisse in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="eaa27-144">Specifies whether to show the previously deleted secrets in the output</span></span>

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

### <span data-ttu-id="eaa27-145">-Name</span><span class="sxs-lookup"><span data-stu-id="eaa27-145">-Name</span></span>
<span data-ttu-id="eaa27-146">Gibt den Namen des abzurufenden Geheimnisses an.</span><span class="sxs-lookup"><span data-stu-id="eaa27-146">Specifies the name of the secret to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, ByInputObjectVaultName, ByResourceIdVaultName
Aliases: SecretName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySecretName, BySecretVersions, ByInputObjectSecretName, ByInputObjectSecretVersions, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases: SecretName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-147">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="eaa27-147">-ResourceId</span></span>
<span data-ttu-id="eaa27-148">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="eaa27-148">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdVaultName, ByResourceIdSecretName, ByResourceIdSecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-149">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="eaa27-149">-VaultName</span></span>
<span data-ttu-id="eaa27-150">Gibt den Namen des Schlüsseldepots an, zu dem der geheime Schlüssel gehört.</span><span class="sxs-lookup"><span data-stu-id="eaa27-150">Specifies the name of the key vault to which the secret belongs.</span></span>
<span data-ttu-id="eaa27-151">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="eaa27-151">This cmdlet constructs the fully qualified domain name (FQDN) of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultName, BySecretName, BySecretVersions
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-152">-Version</span><span class="sxs-lookup"><span data-stu-id="eaa27-152">-Version</span></span>
<span data-ttu-id="eaa27-153">Gibt die geheime Version an.</span><span class="sxs-lookup"><span data-stu-id="eaa27-153">Specifies the secret version.</span></span>
<span data-ttu-id="eaa27-154">Dieses Cmdlet erstellt den FQDN eines geheimen Schlüssels basierend auf dem schlüsseltresor Namen, der aktuell ausgewählten Umgebung, dem geheimen Namen und der geheimen Version.</span><span class="sxs-lookup"><span data-stu-id="eaa27-154">This cmdlet constructs the FQDN of a secret based on the key vault name, your currently selected environment, the secret name, and the secret version.</span></span>

```yaml
Type: System.String
Parameter Sets: BySecretName, ByInputObjectSecretName, ByResourceIdSecretName
Aliases: SecretVersion

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eaa27-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eaa27-155">CommonParameters</span></span>
<span data-ttu-id="eaa27-156">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eaa27-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eaa27-157">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eaa27-157">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eaa27-158">Eingaben</span><span class="sxs-lookup"><span data-stu-id="eaa27-158">INPUTS</span></span>

### <span data-ttu-id="eaa27-159">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="eaa27-159">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="eaa27-160">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eaa27-160">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="eaa27-161">System. String</span><span class="sxs-lookup"><span data-stu-id="eaa27-161">System.String</span></span>

## <span data-ttu-id="eaa27-162">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="eaa27-162">OUTPUTS</span></span>

### <span data-ttu-id="eaa27-163">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eaa27-163">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="eaa27-164">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eaa27-164">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultSecret</span></span>

### <span data-ttu-id="eaa27-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span><span class="sxs-lookup"><span data-stu-id="eaa27-165">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecretIdentityItem</span></span>

### <span data-ttu-id="eaa27-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eaa27-166">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultSecret</span></span>

## <span data-ttu-id="eaa27-167">Notizen</span><span class="sxs-lookup"><span data-stu-id="eaa27-167">NOTES</span></span>

## <span data-ttu-id="eaa27-168">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="eaa27-168">RELATED LINKS</span></span>

[<span data-ttu-id="eaa27-169">Remove-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eaa27-169">Remove-AzureKeyVaultSecret</span></span>](./Remove-AzureKeyVaultSecret.md)

[<span data-ttu-id="eaa27-170">Undo-AzureKeyVaultSecretRemoval</span><span class="sxs-lookup"><span data-stu-id="eaa27-170">Undo-AzureKeyVaultSecretRemoval</span></span>](./Undo-AzureKeyVaultSecretRemoval.md)

[<span data-ttu-id="eaa27-171">Satz-AzureKeyVaultSecret</span><span class="sxs-lookup"><span data-stu-id="eaa27-171">Set-AzureKeyVaultSecret</span></span>](./Set-AzureKeyVaultSecret.md)

