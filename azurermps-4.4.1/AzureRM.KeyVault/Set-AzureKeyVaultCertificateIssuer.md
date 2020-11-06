---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: eac75ae5c9828493244ace01b6c090fda7e6ef5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500014"
---
# <span data-ttu-id="52a80-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52a80-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="52a80-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52a80-102">SYNOPSIS</span></span>
<span data-ttu-id="52a80-103">Legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="52a80-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a80-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a80-104">SYNTAX</span></span>

### <span data-ttu-id="52a80-105">Erweitert (Standard)</span><span class="sxs-lookup"><span data-stu-id="52a80-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-IssuerProvider <String>]
 [-AccountId <String>] [-ApiKey <SecureString>] [-OrganizationDetails <KeyVaultCertificateOrganizationDetails>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52a80-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="52a80-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -Issuer <KeyVaultCertificateIssuer>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52a80-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52a80-107">DESCRIPTION</span></span>
<span data-ttu-id="52a80-108">Das Set-AzureKeyVaultCertificateIssuer-Cmdlet legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="52a80-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="52a80-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52a80-109">EXAMPLES</span></span>

### <span data-ttu-id="52a80-110">Beispiel 1: Einrichten eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="52a80-110">Example 1: Set a certificate issuer</span></span>
```
PS C:\>$Issuer = Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru
```

<span data-ttu-id="52a80-111">Mit diesem Befehl werden die Eigenschaften für einen Aussteller des Zertifikats festgelegt und dann in der $Issuer-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="52a80-111">This command sets the properties for a certificate issuer, and then stores it in the $Issuer variable.</span></span>

## <span data-ttu-id="52a80-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a80-112">PARAMETERS</span></span>

### <span data-ttu-id="52a80-113">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="52a80-113">-AccountId</span></span>
<span data-ttu-id="52a80-114">Gibt die Konto-ID für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="52a80-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-115">-Apischluessel</span><span class="sxs-lookup"><span data-stu-id="52a80-115">-ApiKey</span></span>
<span data-ttu-id="52a80-116">Gibt den API-Schlüssel für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="52a80-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-117">-Emittent</span><span class="sxs-lookup"><span data-stu-id="52a80-117">-Issuer</span></span>
<span data-ttu-id="52a80-118">Gibt den Zertifikataussteller an, der aktualisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a80-118">Specifies the certificate issuer to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer
Parameter Sets: ByValue
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-119">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="52a80-119">-IssuerProvider</span></span>
<span data-ttu-id="52a80-120">Gibt den Typ des Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="52a80-120">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-121">-Name</span><span class="sxs-lookup"><span data-stu-id="52a80-121">-Name</span></span>
<span data-ttu-id="52a80-122">Gibt den Namen des Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="52a80-122">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-123">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="52a80-123">-OrganizationDetails</span></span>
<span data-ttu-id="52a80-124">Die für den Aussteller zu verwendenden Organisationsdetails.</span><span class="sxs-lookup"><span data-stu-id="52a80-124">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52a80-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="52a80-125">-PassThru</span></span>
<span data-ttu-id="52a80-126">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="52a80-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="52a80-127">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="52a80-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="52a80-128">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="52a80-128">-VaultName</span></span>
<span data-ttu-id="52a80-129">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="52a80-129">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="52a80-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="52a80-130">-Confirm</span></span>
<span data-ttu-id="52a80-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="52a80-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52a80-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52a80-132">-WhatIf</span></span>
<span data-ttu-id="52a80-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="52a80-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52a80-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="52a80-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52a80-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a80-135">-DefaultProfile</span></span>
<span data-ttu-id="52a80-136">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52a80-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a80-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a80-137">CommonParameters</span></span>
<span data-ttu-id="52a80-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a80-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a80-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a80-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a80-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52a80-140">INPUTS</span></span>

## <span data-ttu-id="52a80-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52a80-141">OUTPUTS</span></span>

### <span data-ttu-id="52a80-142">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="52a80-142">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="52a80-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="52a80-143">NOTES</span></span>

## <span data-ttu-id="52a80-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52a80-144">RELATED LINKS</span></span>

[<span data-ttu-id="52a80-145">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52a80-145">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="52a80-146">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="52a80-146">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

