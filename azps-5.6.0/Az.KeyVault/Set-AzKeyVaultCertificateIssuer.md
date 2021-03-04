---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 33c274154e122c0bb0925b8381d2dd51cad18264
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922979"
---
# <span data-ttu-id="6b08a-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b08a-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="6b08a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b08a-102">SYNOPSIS</span></span>
<span data-ttu-id="6b08a-103">Legt einen Zertifikataussteller in einem Schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="6b08a-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="6b08a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6b08a-104">SYNTAX</span></span>

### <span data-ttu-id="6b08a-105">Erweitert (Standard)</span><span class="sxs-lookup"><span data-stu-id="6b08a-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b08a-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="6b08a-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b08a-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6b08a-107">DESCRIPTION</span></span>
<span data-ttu-id="6b08a-108">Das Set-AzKeyVaultCertificateIssuer-Cmdlet legt einen Zertifikataussteller in einem Schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="6b08a-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="6b08a-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6b08a-109">EXAMPLES</span></span>

### <span data-ttu-id="6b08a-110">Beispiel 1: Festlegen eines Zertifikatausstellers</span><span class="sxs-lookup"><span data-stu-id="6b08a-110">Example 1: Set a certificate issuer</span></span>
```powershell
PS C:\> $AdminDetails = New-AzKeyVaultCertificateAdministratorDetail -FirstName user -LastName name -EmailAddress username@microsoft.com
PS C:\> $OrgDetails = New-AzKeyVaultCertificateOrganizationDetail -AdministrationDetails $AdminDetails
PS C:\> $Password = ConvertTo-SecureString -String P@ssw0rd -AsPlainText -Force
PS C:\> Set-AzKeyVaultCertificateIssuer -VaultName "Contosokv01" -Name "TestIssuer01" -IssuerProvider "Test" -AccountId "555" -ApiKey $Password -OrganizationDetails $OrgDetails -PassThru

AccountId           : 555
ApiKey              :
OrganizationDetails : Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails
Name                : TestIssuer01
IssuerProvider      : Test
VaultName           : Contosokv01
```

<span data-ttu-id="6b08a-111">Mit diesem Befehl werden die Eigenschaften für einen Zertifikataussteller festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6b08a-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="6b08a-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6b08a-112">PARAMETERS</span></span>

### <span data-ttu-id="6b08a-113">-AccountId</span><span class="sxs-lookup"><span data-stu-id="6b08a-113">-AccountId</span></span>
<span data-ttu-id="6b08a-114">Gibt die Konto-ID für den Zertifikataussteller an.</span><span class="sxs-lookup"><span data-stu-id="6b08a-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="6b08a-115">-ApiKey</span><span class="sxs-lookup"><span data-stu-id="6b08a-115">-ApiKey</span></span>
<span data-ttu-id="6b08a-116">Gibt den API-Schlüssel für den Zertifikataussteller an.</span><span class="sxs-lookup"><span data-stu-id="6b08a-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="6b08a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b08a-117">-DefaultProfile</span></span>
<span data-ttu-id="6b08a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6b08a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6b08a-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6b08a-119">-InputObject</span></span>
<span data-ttu-id="6b08a-120">Gibt den Zertifikataussteller an, der festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6b08a-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="6b08a-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="6b08a-121">-IssuerProvider</span></span>
<span data-ttu-id="6b08a-122">Gibt den Typ des Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="6b08a-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="6b08a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="6b08a-123">-Name</span></span>
<span data-ttu-id="6b08a-124">Gibt den Namen des Ausstellers an.</span><span class="sxs-lookup"><span data-stu-id="6b08a-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="6b08a-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6b08a-125">-OrganizationDetails</span></span>
<span data-ttu-id="6b08a-126">Organisationsdetails, die mit dem Aussteller verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6b08a-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="6b08a-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6b08a-127">-PassThru</span></span>
<span data-ttu-id="6b08a-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="6b08a-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="6b08a-129">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="6b08a-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="6b08a-130">-VaultName</span><span class="sxs-lookup"><span data-stu-id="6b08a-130">-VaultName</span></span>
<span data-ttu-id="6b08a-131">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="6b08a-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="6b08a-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6b08a-132">-Confirm</span></span>
<span data-ttu-id="6b08a-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6b08a-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b08a-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b08a-134">-WhatIf</span></span>
<span data-ttu-id="6b08a-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6b08a-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b08a-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6b08a-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b08a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b08a-137">CommonParameters</span></span>
<span data-ttu-id="6b08a-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b08a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b08a-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b08a-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b08a-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6b08a-140">INPUTS</span></span>

### <span data-ttu-id="6b08a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="6b08a-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="6b08a-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="6b08a-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="6b08a-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6b08a-143">OUTPUTS</span></span>

### <span data-ttu-id="6b08a-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="6b08a-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="6b08a-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="6b08a-145">NOTES</span></span>

## <span data-ttu-id="6b08a-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="6b08a-146">RELATED LINKS</span></span>

[<span data-ttu-id="6b08a-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b08a-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="6b08a-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="6b08a-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

