---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: A7C287C4-E9FD-407A-91BD-EFA17C33FC8B
online version: https://go.microsoft.com/fwlink/?LinkID=690161
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Get-AzureRmKeyVault.md
ms.openlocfilehash: 9a4d3399dd19d7dfced4f695623eef2fe0dba29d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479202"
---
# <span data-ttu-id="42fb1-101">Get-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-101">Get-AzureRmKeyVault</span></span>

## <span data-ttu-id="42fb1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="42fb1-102">SYNOPSIS</span></span>
<span data-ttu-id="42fb1-103">Ruft Schlüsseldepots ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-103">Gets key vaults.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42fb1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="42fb1-104">SYNTAX</span></span>

### <span data-ttu-id="42fb1-105">GetVaultByName</span><span class="sxs-lookup"><span data-stu-id="42fb1-105">GetVaultByName</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42fb1-106">ByDeletedVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-106">ByDeletedVault</span></span>
```
Get-AzureRmKeyVault [-VaultName] <String> [-Location] <String> [-InRemovedState]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42fb1-107">ListVaultsByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="42fb1-107">ListVaultsByResourceGroup</span></span>
```
Get-AzureRmKeyVault [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="42fb1-108">ListAllDeletedVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="42fb1-108">ListAllDeletedVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-InRemovedState] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42fb1-109">ListAllVaultsInSubscription</span><span class="sxs-lookup"><span data-stu-id="42fb1-109">ListAllVaultsInSubscription</span></span>
```
Get-AzureRmKeyVault [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42fb1-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="42fb1-110">DESCRIPTION</span></span>
<span data-ttu-id="42fb1-111">Das Cmdlet " **Get-AzureRmKeyVault** " Ruft Informationen zu den Schlüsseldepots in einem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-111">The **Get-AzureRmKeyVault** cmdlet gets information about the key vaults in a subscription.</span></span> <span data-ttu-id="42fb1-112">Sie können alle wichtigen Vaults-Instanzen in einem Abonnement anzeigen oder Ihre Ergebnisse nach einer Ressourcengruppe oder einem bestimmten schlüsseltresor filtern.</span><span class="sxs-lookup"><span data-stu-id="42fb1-112">You can view all key vaults instances in a subscription, or filter your results by a resource group or a particular key vault.</span></span>

<span data-ttu-id="42fb1-113">Beachten Sie, dass die Angabe der Ressourcengruppe zwar für dieses Cmdlet optional ist, wenn Sie einen einzelnen schlüsseltresor erhalten, Sie dies jedoch für eine bessere Leistung tun sollten.</span><span class="sxs-lookup"><span data-stu-id="42fb1-113">Note that although specifying the resource group is optional for this cmdlet when you get a single key vault, you should do so for better performance.</span></span>

## <span data-ttu-id="42fb1-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="42fb1-114">EXAMPLES</span></span>

### <span data-ttu-id="42fb1-115">Beispiel 1: Abrufen aller Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="42fb1-115">Example 1: Get all key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRMKeyVault
```

<span data-ttu-id="42fb1-116">Dieser Befehl ruft alle Schlüsseldepots Ihres aktuellen Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-116">This command gets all the key vaults in your current subscription.</span></span>

### <span data-ttu-id="42fb1-117">Beispiel 2: Abrufen eines bestimmten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="42fb1-117">Example 2: Get a specific key vault</span></span>
```
PS C:\>$MyVault = Get-AzureRMKeyVault -VaultName 'Contoso03Vault'
```

<span data-ttu-id="42fb1-118">Dieser Befehl ruft den schlüsseltresor mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement ab und speichert ihn dann in der $MyVault-Variablen.</span><span class="sxs-lookup"><span data-stu-id="42fb1-118">This command gets the key vault named Contoso03Vault in your current subscription, and then stores it in the $MyVault variable.</span></span> <span data-ttu-id="42fb1-119">Sie können die Eigenschaften von $MyVault überprüfen, um Details zum schlüsseltresor abzurufen.</span><span class="sxs-lookup"><span data-stu-id="42fb1-119">You can inspect the properties of $MyVault to get details about the key vault.</span></span>

### <span data-ttu-id="42fb1-120">Beispiel 3: Abrufen von Schlüsseldepots in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="42fb1-120">Example 3: Get key vaults in a resource group</span></span>
```
PS C:\>Get-AzureRmKeyVault -ResourceGroupName 'ContosoPayRollResourceGroup'
```

<span data-ttu-id="42fb1-121">Dieser Befehl ruft alle Schlüsseldepots in der Ressourcengruppe mit dem Namen ContosoPayRollResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-121">This command gets all the key vaults in the resource group named ContosoPayRollResourceGroup.</span></span>

### <span data-ttu-id="42fb1-122">Beispiel 4: Abrufen aller gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="42fb1-122">Example 4: Get all deleted key vaults in your current subscription</span></span>
```
PS C:\>Get-AzureRmKeyVault -InRemovedState
```

<span data-ttu-id="42fb1-123">Dieser Befehl ruft alle gelöschten Schlüsseldepots in Ihrem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-123">This command gets all the deleted key vaults in your current subscription.</span></span>

### <span data-ttu-id="42fb1-124">Beispiel 5: Abrufen eines gelöschten Schlüsseldepots</span><span class="sxs-lookup"><span data-stu-id="42fb1-124">Example 5: Get a deleted key vault</span></span>
```
PS C:\>Get-AzureRMKeyVault -VaultName 'Contoso03Vault'  -Location 'eastus2' -InRemovedState
```

<span data-ttu-id="42fb1-125">Dieser Befehl ruft die gelöschten Schlüssel Vault-Informationen mit dem Namen Contoso03Vault in Ihrem aktuellen Abonnement und in der eastus2-Region ab.</span><span class="sxs-lookup"><span data-stu-id="42fb1-125">This command gets the deleted key vault information named Contoso03Vault in your current subscription and in eastus2 region.</span></span>

## <span data-ttu-id="42fb1-126">Parameter</span><span class="sxs-lookup"><span data-stu-id="42fb1-126">PARAMETERS</span></span>

### <span data-ttu-id="42fb1-127">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="42fb1-127">-InRemovedState</span></span>
<span data-ttu-id="42fb1-128">Gibt an, ob die zuvor gelöschten Tresore in der Ausgabe angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="42fb1-128">Specifies whether to show the previously deleted vaults in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByDeletedVault, ListAllDeletedVaultsInSubscription
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42fb1-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="42fb1-129">-Location</span></span>
<span data-ttu-id="42fb1-130">Der Speicherort des gelöschten Tresors.</span><span class="sxs-lookup"><span data-stu-id="42fb1-130">The location of the deleted vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByDeletedVault
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42fb1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42fb1-131">-ResourceGroupName</span></span>
<span data-ttu-id="42fb1-132">Gibt den Namen der Ressourcengruppe an, die dem schlüsseltresor oder den Schlüsseldepots zugeordnet ist, die abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="42fb1-132">Specifies the name of the resource group associated with the key vault or key vaults being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListVaultsByResourceGroup
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42fb1-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="42fb1-133">-Tag</span></span>
<span data-ttu-id="42fb1-134">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="42fb1-134">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42fb1-135">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="42fb1-135">For example:</span></span>

<span data-ttu-id="42fb1-136">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="42fb1-136">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ListAllVaultsInSubscription
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42fb1-137">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="42fb1-137">-VaultName</span></span>
<span data-ttu-id="42fb1-138">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="42fb1-138">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVaultByName, ByDeletedVault
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42fb1-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42fb1-139">-DefaultProfile</span></span>
<span data-ttu-id="42fb1-140">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="42fb1-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="42fb1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42fb1-141">CommonParameters</span></span>
<span data-ttu-id="42fb1-142">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42fb1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42fb1-143">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42fb1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42fb1-144">Eingaben</span><span class="sxs-lookup"><span data-stu-id="42fb1-144">INPUTS</span></span>

## <span data-ttu-id="42fb1-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="42fb1-145">OUTPUTS</span></span>

### <span data-ttu-id="42fb1-146">Microsoft. Azure. Commands. keyvault. Models. PSVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-146">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

### <span data-ttu-id="42fb1-147">System. Collections. Generic. List ' 1 [Microsoft. Azure. Commands. keyvault. Models. PSVaultIdentityItem]</span><span class="sxs-lookup"><span data-stu-id="42fb1-147">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSVaultIdentityItem]</span></span>

### <span data-ttu-id="42fb1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-148">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault</span></span>

### <span data-ttu-id="42fb1-149">System. Collections. Generic. List ' 1 [Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span><span class="sxs-lookup"><span data-stu-id="42fb1-149">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.KeyVault.Models.PSDeletedVault]</span></span>

## <span data-ttu-id="42fb1-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="42fb1-150">NOTES</span></span>

## <span data-ttu-id="42fb1-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="42fb1-151">RELATED LINKS</span></span>

[<span data-ttu-id="42fb1-152">Neu – AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-152">New-AzureRmKeyVault</span></span>](./New-AzureRmKeyVault.md)

[<span data-ttu-id="42fb1-153">Remove-AzureRmKeyVault</span><span class="sxs-lookup"><span data-stu-id="42fb1-153">Remove-AzureRmKeyVault</span></span>](./Remove-AzureRmKeyVault.md)
