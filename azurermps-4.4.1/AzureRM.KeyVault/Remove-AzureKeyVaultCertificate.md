---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureKeyVaultCertificate.md
ms.openlocfilehash: 9a33d4efdd82ad03b94ea9a7e862fb5e13eb30d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504921"
---
# <span data-ttu-id="2c4e8-101">Remove-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c4e8-101">Remove-AzureKeyVaultCertificate</span></span>

## <span data-ttu-id="2c4e8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="2c4e8-103">Entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-103">Removes a certificate from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2c4e8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c4e8-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-Force] [-InRemovedState] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c4e8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c4e8-105">DESCRIPTION</span></span>
<span data-ttu-id="2c4e8-106">Das Cmdlet **Remove-AzureKeyVaultCertificate** entfernt ein Zertifikat aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-106">The **Remove-AzureKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="2c4e8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c4e8-107">EXAMPLES</span></span>

### <span data-ttu-id="2c4e8-108">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="2c4e8-108">Example 1: Remove a certificate</span></span>
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

<span data-ttu-id="2c4e8-109">Dieser Befehl entfernt das Zertifikat mit dem Namen SelfSigned01 aus dem schlüsseltresor mit dem Namen ContosoKV01.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-109">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="2c4e8-110">Mit diesem Befehl wird der *Force* -Parameter angegeben.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-110">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="2c4e8-111">Daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-111">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="2c4e8-112">Beispiel 3: Dauerhaftes Löschen des gelöschten Zertifikats aus dem schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="2c4e8-112">Example 3: Purge the deleted certificate from the key vault permanently</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="2c4e8-113">Mit diesem Befehl wird das Zertifikat "MyCert" endgültig aus dem schlüsseltresor "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-113">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="2c4e8-114">Zum Ausführen dieses Cmdlets ist die "Purge"-Berechtigung erforderlich, die dem Benutzer zuvor und explizit für diesen schlüsseltresor gewährt werden muss.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-114">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="2c4e8-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c4e8-115">PARAMETERS</span></span>

### <span data-ttu-id="2c4e8-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2c4e8-116">-Force</span></span>
<span data-ttu-id="2c4e8-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2c4e8-118">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="2c4e8-118">-InRemovedState</span></span>
<span data-ttu-id="2c4e8-119">Wenn vorhanden, wird das zuvor gelöschte Zertifikat dauerhaft entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-119">If present, removes the previously deleted certificate permanently.</span></span>

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

### <span data-ttu-id="2c4e8-120">-Name</span><span class="sxs-lookup"><span data-stu-id="2c4e8-120">-Name</span></span>
<span data-ttu-id="2c4e8-121">Gibt den Namen des Zertifikats an, das dieses Cmdlet aus einem schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-121">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="2c4e8-122">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsselspeichers und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-122">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e8-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c4e8-123">-PassThru</span></span>
<span data-ttu-id="2c4e8-124">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2c4e8-125">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2c4e8-126">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="2c4e8-126">-VaultName</span></span>
<span data-ttu-id="2c4e8-127">Gibt den Namen des Schlüsselspeichers an, aus dem dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-127">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="2c4e8-128">Dieses Cmdlet erstellt den FQDN eines Schlüsseldepots basierend auf dem Namen, den dieser Parameter angibt, und der aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-128">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e8-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c4e8-129">-Confirm</span></span>
<span data-ttu-id="2c4e8-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c4e8-131">-WhatIf</span></span>
<span data-ttu-id="2c4e8-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c4e8-133">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-133">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c4e8-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c4e8-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c4e8-135">-DefaultProfile</span></span>
<span data-ttu-id="2c4e8-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c4e8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c4e8-137">CommonParameters</span></span>
<span data-ttu-id="2c4e8-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c4e8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c4e8-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c4e8-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c4e8-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c4e8-140">INPUTS</span></span>

## <span data-ttu-id="2c4e8-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c4e8-141">OUTPUTS</span></span>

### <span data-ttu-id="2c4e8-142">Microsoft. Azure. Commands. keyvault. Models. CertificateBundle</span><span class="sxs-lookup"><span data-stu-id="2c4e8-142">Microsoft.Azure.Commands.KeyVault.Models.CertificateBundle</span></span>

## <span data-ttu-id="2c4e8-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c4e8-143">NOTES</span></span>

## <span data-ttu-id="2c4e8-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c4e8-144">RELATED LINKS</span></span>

[<span data-ttu-id="2c4e8-145">Add-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c4e8-145">Add-AzureKeyVaultCertificate</span></span>](./Add-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2c4e8-146">Get-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c4e8-146">Get-AzureKeyVaultCertificate</span></span>](./Get-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2c4e8-147">Importieren-AzureKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="2c4e8-147">Import-AzureKeyVaultCertificate</span></span>](./Import-AzureKeyVaultCertificate.md)

[<span data-ttu-id="2c4e8-148">Undo-AzureKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="2c4e8-148">Undo-AzureKeyVaultCertificateRemoval</span></span>](./Undo-AzureKeyVaultCertificateRemoval.md)
