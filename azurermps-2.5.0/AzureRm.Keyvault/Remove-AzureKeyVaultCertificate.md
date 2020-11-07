---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificate
schema: 2.0.0
ms.openlocfilehash: 662304cff991da0d9ffe9d946e63bc94ba51e4a9
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848240"
---
# <span data-ttu-id="28c50-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="28c50-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="28c50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28c50-102">SYNOPSIS</span></span>
<span data-ttu-id="28c50-103">Entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="28c50-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28c50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28c50-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28c50-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28c50-105">DESCRIPTION</span></span>
<span data-ttu-id="28c50-106">Das Cmdlet **Remove-AzureKeyVaultCertificate** entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="28c50-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="28c50-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28c50-107">EXAMPLES</span></span>

### <span data-ttu-id="28c50-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="28c50-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="28c50-109">Dieser Befehl entfernt das Zertifikat mit dem Namen SelfSigned01 aus dem schlüsseltresor mit dem Namen ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="28c50-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="28c50-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="28c50-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="28c50-111">Daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="28c50-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="28c50-112">Beispiel 3: Dauerhaftes Löschen des gelöschten Zertifikats aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="28c50-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="28c50-113">Mit diesem Befehl wird das Zertifikat "MyCert" endgültig aus dem schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="28c50-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="28c50-114">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="28c50-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="28c50-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="28c50-115">PARAMETERS</span></span>

### <span data-ttu-id="28c50-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28c50-116">-DefaultProfile</span></span>
<span data-ttu-id="28c50-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="28c50-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28c50-118">-Force</span><span class="sxs-lookup"><span data-stu-id="28c50-118">-Force</span></span>
<span data-ttu-id="28c50-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="28c50-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28c50-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="28c50-120">-InRemovedState</span></span>
<span data-ttu-id="28c50-121">Wenn vorhanden, entfernt das zuvor gelöschte Zertifikat endgültig</span><span class="sxs-lookup"><span data-stu-id="28c50-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="28c50-122">-Name</span><span class="sxs-lookup"><span data-stu-id="28c50-122">-Name</span></span>
<span data-ttu-id="28c50-123">Gibt den Namen des Zertifikats an, das dieses Cmdlet aus einem schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="28c50-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="28c50-124">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="28c50-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28c50-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28c50-125">-PassThru</span></span>
<span data-ttu-id="28c50-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="28c50-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28c50-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="28c50-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28c50-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="28c50-128">-VaultName</span></span>
<span data-ttu-id="28c50-129">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="28c50-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="28c50-130">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="28c50-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="28c50-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28c50-131">-Confirm</span></span>
<span data-ttu-id="28c50-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28c50-132">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c50-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28c50-133">-WhatIf</span></span>
<span data-ttu-id="28c50-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28c50-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c50-135">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28c50-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28c50-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28c50-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28c50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28c50-137">CommonParameters</span></span>
<span data-ttu-id="28c50-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28c50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28c50-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28c50-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28c50-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28c50-140">INPUTS</span></span>

## <span data-ttu-id="28c50-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28c50-141">OUTPUTS</span></span>

### <span data-ttu-id="28c50-142">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="28c50-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="28c50-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="28c50-143">NOTES</span></span>

## <span data-ttu-id="28c50-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28c50-144">RELATED LINKS</span></span>

[<span data-ttu-id="28c50-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="28c50-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="28c50-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="28c50-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="28c50-147">Importieren-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="28c50-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="28c50-148">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="28c50-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
