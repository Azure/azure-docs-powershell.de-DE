---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 7b26eeb94854d21791bb662b4c1d9ce19973a193
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505506"
---
# <span data-ttu-id="6a9d8-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="6a9d8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6a9d8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9d8-103">Ruft Schlüsseldepots ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a9d8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6a9d8-104">SYNTAX</span></span>

### <span data-ttu-id="6a9d8-105">ListAllVaultsInSubscription (Standard)</span><span class="sxs-lookup"><span data-stu-id="6a9d8-105">ListAllVaultsInSubscription (Default)</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9d8-106">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="6a9d8-106">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [[-VaultName] <String>] [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9d8-107">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-107">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9d8-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="6a9d8-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9d8-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6a9d8-109">DESCRIPTION</span></span>
<span data-ttu-id="6a9d8-110">Das Cmdlet " **Get-AzureRmKeyVault** " Ruft Informationen zu den Schlüsseldepots in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-110">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="6a9d8-111">Sie können alle wichtigen Vaults-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten schlüsseltresor filtern.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-111">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="6a9d8-112">Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie einen einzelnen schlüsseltresor erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-112">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="6a9d8-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6a9d8-113">EXAMPLES</span></span>

### <span data-ttu-id="6a9d8-114">Beispiel 1: Abrufen aller Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6a9d8-114">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="6a9d8-115">Dieser Befehl ruft alle Schlüsseldepots Ihres aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-115">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="6a9d8-116">Beispiel 2: Abrufen eines bestimmten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="6a9d8-116">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="6a9d8-117">Dieser Befehl ruft den schlüsseltresor mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement ab und speichert ihn dann in der $MyVault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-117">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="6a9d8-118">Sie können die Eigenschaften von $MyVault überprüfen, um Details zum schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-118">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="6a9d8-119">Beispiel 3: Abrufen von Schlüsseldepots in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6a9d8-119">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="6a9d8-120">Dieser Befehl ruft alle Schlüsseldepots in der Ressourcengruppe mit dem Namen ContosoPayRollResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-120">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="6a9d8-121">Beispiel 4: Abrufen aller gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="6a9d8-121">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="6a9d8-122">Dieser Befehl ruft alle gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-122">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="6a9d8-123">Beispiel 5: Abrufen eines gelöschten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="6a9d8-123">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="6a9d8-124">Dieser Befehl ruft die gelöschten Schlüssel Vault-Informationen mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement und in der eastus2-Region ab.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-124">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="6a9d8-125">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a9d8-125">PARAMETERS</span></span>

### <span data-ttu-id="6a9d8-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9d8-126">-DefaultProfile</span></span>
<span data-ttu-id="6a9d8-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6a9d8-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-128">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="6a9d8-128">-InRemovedState</span></span>
<span data-ttu-id="6a9d8-129">Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-129">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-130">-Standort</span><span class="sxs-lookup"><span data-stu-id="6a9d8-130">-Location</span></span>
<span data-ttu-id="6a9d8-131">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-131">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a9d8-132">-ResourceGroupName</span></span>
<span data-ttu-id="6a9d8-133">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor oder den Schlüsseldepots zugeordnet ist, die abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-133">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="6a9d8-134">-Tag</span></span>
<span data-ttu-id="6a9d8-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="6a9d8-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6a9d8-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6a9d8-136">For example:</span></span>

<span data-ttu-id="6a9d8-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6a9d8-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-138">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="6a9d8-138">-VaultName</span></span>
<span data-ttu-id="6a9d8-139">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-139">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName
Aliases: Name

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6a9d8-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9d8-140">CommonParameters</span></span>
<span data-ttu-id="6a9d8-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9d8-142">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a9d8-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9d8-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6a9d8-143">INPUTS</span></span>

### <span data-ttu-id="6a9d8-144">Keine</span><span class="sxs-lookup"><span data-stu-id="6a9d8-144">None</span></span>
<span data-ttu-id="6a9d8-145">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6a9d8-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6a9d8-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6a9d8-146">OUTPUTS</span></span>

### <span data-ttu-id="6a9d8-147">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-147">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="6a9d8-148">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="6a9d8-148">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem]</span></span>

### <span data-ttu-id="6a9d8-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-149">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault</span></span>

### <span data-ttu-id="6a9d8-150">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span><span class="sxs-lookup"><span data-stu-id="6a9d8-150">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVault]</span></span>

## <span data-ttu-id="6a9d8-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="6a9d8-151">NOTES</span></span>

## <span data-ttu-id="6a9d8-152">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6a9d8-152">RELATED LINKS</span></span>

[<span data-ttu-id="6a9d8-153">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-153">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="6a9d8-154">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="6a9d8-154">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
