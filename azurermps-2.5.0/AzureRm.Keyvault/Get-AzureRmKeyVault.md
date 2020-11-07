---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/get-azurermkeyvault
schema: 2.0.0
ms.openlocfilehash: 7cbcf722b71919096ca2c7d1dc3201ad2fe42f2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850004"
---
# <span data-ttu-id="23801-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="23801-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="23801-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23801-102">SYNOPSIS</span></span>
<span data-ttu-id="23801-103">Ruft Schlüsseldepots ab.</span><span class="sxs-lookup"><span data-stu-id="23801-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23801-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23801-104">SYNTAX</span></span>

### <span data-ttu-id="23801-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="23801-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23801-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="23801-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23801-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="23801-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="23801-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="23801-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="23801-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="23801-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23801-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23801-110">DESCRIPTION</span></span>
<span data-ttu-id="23801-111">Das Cmdlet " **Get-AzureRmKeyVault** " Ruft Informationen zu den Schlüsseldepots in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="23801-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="23801-112">Sie können alle wichtigen Vaults-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten schlüsseltresor filtern.</span><span class="sxs-lookup"><span data-stu-id="23801-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="23801-113">Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie einen einzelnen schlüsseltresor erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="23801-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="23801-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23801-114">EXAMPLES</span></span>

### <span data-ttu-id="23801-115">Beispiel 1: Abrufen aller Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="23801-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="23801-116">Dieser Befehl ruft alle Schlüsseldepots Ihres aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="23801-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="23801-117">Beispiel 2: Abrufen eines bestimmten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="23801-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="23801-118">Dieser Befehl ruft den schlüsseltresor mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement ab und speichert ihn dann in der $MyVault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="23801-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="23801-119">Sie können die Eigenschaften von $MyVault überprüfen, um Details zum schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="23801-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="23801-120">Beispiel 3: Abrufen von Schlüsseldepots in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="23801-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="23801-121">Dieser Befehl ruft alle Schlüsseldepots in der Ressourcengruppe mit dem Namen ContosoPayRollResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="23801-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="23801-122">Beispiel 4: Abrufen aller gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="23801-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="23801-123">Dieser Befehl ruft alle gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="23801-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="23801-124">Beispiel 5: Abrufen eines gelöschten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="23801-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="23801-125">Dieser Befehl ruft die gelöschten Schlüssel Vault-Informationen mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement und in der eastus2-Region ab.</span><span class="sxs-lookup"><span data-stu-id="23801-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="23801-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="23801-126">PARAMETERS</span></span>

### <span data-ttu-id="23801-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23801-127">-DefaultProfile</span></span>
<span data-ttu-id="23801-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="23801-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="23801-129">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="23801-129">-InRemovedState</span></span>
<span data-ttu-id="23801-130">Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="23801-130">Specifies whether to show the previously deleted vaults in the output.</span></span>

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

### <span data-ttu-id="23801-131">-Standort</span><span class="sxs-lookup"><span data-stu-id="23801-131">-Location</span></span>
<span data-ttu-id="23801-132">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="23801-132">The location of the deleted vault.</span></span>

```yaml
Type: String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23801-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23801-133">-ResourceGroupName</span></span>
<span data-ttu-id="23801-134">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor oder den Schlüsseldepots zugeordnet ist, die abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="23801-134">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

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

```yaml
Type: String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23801-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="23801-135">-Tag</span></span>
<span data-ttu-id="23801-136">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="23801-136">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="23801-137">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="23801-137">For example:</span></span>

<span data-ttu-id="23801-138">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="23801-138">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="23801-139">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="23801-139">-VaultName</span></span>
<span data-ttu-id="23801-140">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="23801-140">Specifies the name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23801-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23801-141">CommonParameters</span></span>
<span data-ttu-id="23801-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23801-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23801-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="23801-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23801-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23801-144">INPUTS</span></span>

## <span data-ttu-id="23801-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23801-145">OUTPUTS</span></span>

### <span data-ttu-id="23801-146">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="23801-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="23801-147">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="23801-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="23801-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="23801-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="23801-149">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="23801-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="23801-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="23801-150">NOTES</span></span>

## <span data-ttu-id="23801-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23801-151">RELATED LINKS</span></span>

[<span data-ttu-id="23801-152">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="23801-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="23801-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="23801-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
