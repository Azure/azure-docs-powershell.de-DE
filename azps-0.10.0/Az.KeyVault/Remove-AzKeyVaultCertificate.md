---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: b2e7264b5c0f54f18e295a86f9abb1cbd51dc4b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842124"
---
# <span data-ttu-id="144ca-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="144ca-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="144ca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="144ca-102">SYNOPSIS</span></span>
<span data-ttu-id="144ca-103">Entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="144ca-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="144ca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="144ca-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="144ca-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="144ca-105">DESCRIPTION</span></span>
<span data-ttu-id="144ca-106">Das Cmdlet **Remove-AzKeyVaultCertificate** entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="144ca-106">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="144ca-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="144ca-107">EXAMPLES</span></span>

### <span data-ttu-id="144ca-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="144ca-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force
Name        : selfSigned01
Certificate : 
Thumbprint  : 
Tags        : 
Enabled     : True
Created     : 2/8/2016 11:29:33 PM
Updated     : 2/8/2016 11:29:33 PM
```

<span data-ttu-id="144ca-109">Dieser Befehl entfernt das Zertifikat mit dem Namen SelfSigned01 aus dem schlüsseltresor mit dem Namen ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="144ca-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="144ca-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="144ca-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="144ca-111">Daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="144ca-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="144ca-112">Beispiel 3: Dauerhaftes Löschen des gelöschten Zertifikats aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="144ca-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="144ca-113">Mit diesem Befehl wird das Zertifikat "MyCert" endgültig aus dem schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="144ca-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="144ca-114">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="144ca-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="144ca-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="144ca-115">PARAMETERS</span></span>

### <span data-ttu-id="144ca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144ca-116">-DefaultProfile</span></span>
<span data-ttu-id="144ca-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="144ca-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="144ca-118">-Force</span><span class="sxs-lookup"><span data-stu-id="144ca-118">-Force</span></span>
<span data-ttu-id="144ca-119">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="144ca-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="144ca-120">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="144ca-120">-InRemovedState</span></span>
<span data-ttu-id="144ca-121">Wenn vorhanden, entfernt das zuvor gelöschte Zertifikat endgültig</span><span class="sxs-lookup"><span data-stu-id="144ca-121">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="144ca-122">-Name</span><span class="sxs-lookup"><span data-stu-id="144ca-122">-Name</span></span>
<span data-ttu-id="144ca-123">Gibt den Namen des Zertifikats an, das dieses Cmdlet aus einem schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="144ca-123">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="144ca-124">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="144ca-124">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

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

### <span data-ttu-id="144ca-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="144ca-125">-PassThru</span></span>
<span data-ttu-id="144ca-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="144ca-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="144ca-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="144ca-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="144ca-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="144ca-128">-VaultName</span></span>
<span data-ttu-id="144ca-129">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="144ca-129">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="144ca-130">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="144ca-130">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

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

### <span data-ttu-id="144ca-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="144ca-131">-Confirm</span></span>
<span data-ttu-id="144ca-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="144ca-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="144ca-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="144ca-133">-WhatIf</span></span>
<span data-ttu-id="144ca-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="144ca-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="144ca-135">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="144ca-135">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="144ca-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="144ca-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="144ca-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144ca-137">CommonParameters</span></span>
<span data-ttu-id="144ca-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="144ca-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144ca-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="144ca-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144ca-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="144ca-140">INPUTS</span></span>

### <span data-ttu-id="144ca-141">Keine</span><span class="sxs-lookup"><span data-stu-id="144ca-141">None</span></span>
<span data-ttu-id="144ca-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="144ca-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="144ca-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="144ca-143">OUTPUTS</span></span>

### <span data-ttu-id="144ca-144">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="144ca-144">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="144ca-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="144ca-145">NOTES</span></span>

## <span data-ttu-id="144ca-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="144ca-146">RELATED LINKS</span></span>

[<span data-ttu-id="144ca-147">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="144ca-147">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="144ca-148">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="144ca-148">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="144ca-149">Importieren-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="144ca-149">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="144ca-150">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="144ca-150">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
