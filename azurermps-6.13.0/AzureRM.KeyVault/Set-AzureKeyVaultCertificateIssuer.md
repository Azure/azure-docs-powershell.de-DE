---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/set-azurekeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Set-AzureKeyVaultCertificateIssuer.md
ms.openlocfilehash: 69619b9f5ddd54e0d307a096cc967c307d1f36d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479573"
---
# <span data-ttu-id="28cd5-101">Set-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="28cd5-101">Set-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="28cd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="28cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="28cd5-103">Legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="28cd5-103">Sets a certificate issuer in a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="28cd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="28cd5-104">SYNTAX</span></span>

### <span data-ttu-id="28cd5-105">Erweitert (Standard)</span><span class="sxs-lookup"><span data-stu-id="28cd5-105">Expanded (Default)</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="28cd5-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="28cd5-106">ByValue</span></span>
```
Set-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="28cd5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="28cd5-107">DESCRIPTION</span></span>
<span data-ttu-id="28cd5-108">Das Set-AzureKeyVaultCertificateIssuer-Cmdlet legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="28cd5-108">The Set-AzureKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="28cd5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="28cd5-109">EXAMPLES</span></span>

### <span data-ttu-id="28cd5-110">Beispiel 1: Einrichten eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="28cd5-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzureKeyVaultCertificateAdministratorDetails -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzureKeyVaultCertificateOrganizationDetails -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzureKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="28cd5-111">Mit diesem Befehl werden die Eigenschaften für einen Aussteller des Zertifikats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="28cd5-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="28cd5-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="28cd5-112">PARAMETERS</span></span>

### <span data-ttu-id="28cd5-113">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="28cd5-113">-AccountId</span></span>
<span data-ttu-id="28cd5-114">Gibt die Konto-ID für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="28cd5-114">Specifies the account ID for the certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-115">-Apischluessel</span><span class="sxs-lookup"><span data-stu-id="28cd5-115">-ApiKey</span></span>
<span data-ttu-id="28cd5-116">Gibt den API-Schlüssel für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="28cd5-116">Specifies the API key for the certificate issuer.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cd5-117">-DefaultProfile</span></span>
<span data-ttu-id="28cd5-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="28cd5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28cd5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="28cd5-119">-InputObject</span></span>
<span data-ttu-id="28cd5-120">Gibt den Zertifikataussteller an, der festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="28cd5-120">Specifies the certificate issuer to set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: ByValue
Aliases: Issuer

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="28cd5-121">-IssuerProvider</span></span>
<span data-ttu-id="28cd5-122">Gibt den Typ des Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="28cd5-122">Specifies the type of certificate issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: Expanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="28cd5-123">-Name</span></span>
<span data-ttu-id="28cd5-124">Gibt den Namen des Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="28cd5-124">Specifies the name of the Issuer.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="28cd5-125">-OrganizationDetails</span></span>
<span data-ttu-id="28cd5-126">Die für den Aussteller zu verwendenden Organisationsdetails.</span><span class="sxs-lookup"><span data-stu-id="28cd5-126">Organization details to be used with the issuer.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Parameter Sets: Expanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28cd5-127">-PassThru</span></span>
<span data-ttu-id="28cd5-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="28cd5-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28cd5-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="28cd5-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28cd5-130">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="28cd5-130">-VaultName</span></span>
<span data-ttu-id="28cd5-131">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="28cd5-131">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28cd5-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="28cd5-132">-Confirm</span></span>
<span data-ttu-id="28cd5-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="28cd5-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cd5-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cd5-134">-WhatIf</span></span>
<span data-ttu-id="28cd5-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="28cd5-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cd5-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="28cd5-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cd5-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cd5-137">CommonParameters</span></span>
<span data-ttu-id="28cd5-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28cd5-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cd5-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cd5-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cd5-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="28cd5-140">INPUTS</span></span>

### <span data-ttu-id="28cd5-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="28cd5-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>
<span data-ttu-id="28cd5-142">Parameter: OrganizationDetails (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28cd5-142">Parameters: OrganizationDetails (ByValue)</span></span>

### <span data-ttu-id="28cd5-143">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="28cd5-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>
<span data-ttu-id="28cd5-144">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="28cd5-144">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="28cd5-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="28cd5-145">OUTPUTS</span></span>

### <span data-ttu-id="28cd5-146">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="28cd5-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="28cd5-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="28cd5-147">NOTES</span></span>

## <span data-ttu-id="28cd5-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="28cd5-148">RELATED LINKS</span></span>

[<span data-ttu-id="28cd5-149">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="28cd5-149">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="28cd5-150">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="28cd5-150">Remove-AzureKeyVaultCertificateIssuer</span></span>](./Remove-AzureKeyVaultCertificateIssuer.md)

