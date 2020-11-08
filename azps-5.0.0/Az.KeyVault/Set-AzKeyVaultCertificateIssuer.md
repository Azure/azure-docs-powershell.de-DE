---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 4C2C77F7-ECE4-4106-8AF1-256A496A977B
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 4d3be232e97f71a030548fd0b3754a7472b80b22
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179251"
---
# <span data-ttu-id="b797f-101">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b797f-101">Set-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="b797f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b797f-102">SYNOPSIS</span></span>
<span data-ttu-id="b797f-103">Legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="b797f-103">Sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="b797f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b797f-104">SYNTAX</span></span>

### <span data-ttu-id="b797f-105">Erweitert (Standard)</span><span class="sxs-lookup"><span data-stu-id="b797f-105">Expanded (Default)</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> -IssuerProvider <String>
 [-AccountId <String>] [-ApiKey <SecureString>]
 [-OrganizationDetails <PSKeyVaultCertificateOrganizationDetails>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b797f-106">ByValue</span><span class="sxs-lookup"><span data-stu-id="b797f-106">ByValue</span></span>
```
Set-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String>
 -InputObject <PSKeyVaultCertificateIssuerIdentityItem> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b797f-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b797f-107">DESCRIPTION</span></span>
<span data-ttu-id="b797f-108">Das Set-AzKeyVaultCertificateIssuer-Cmdlet legt einen Zertifikataussteller in einem schlüsseltresor fest.</span><span class="sxs-lookup"><span data-stu-id="b797f-108">The Set-AzKeyVaultCertificateIssuer cmdlet sets a certificate issuer in a key vault.</span></span>

## <span data-ttu-id="b797f-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b797f-109">EXAMPLES</span></span>

### <span data-ttu-id="b797f-110">Beispiel 1: Einrichten eines Zertifikats Emittenten</span><span class="sxs-lookup"><span data-stu-id="b797f-110">Example 1: Set a certificate issuer</span></span>
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

<span data-ttu-id="b797f-111">Mit diesem Befehl werden die Eigenschaften für einen Aussteller des Zertifikats festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b797f-111">This command sets the properties for a certificate issuer.</span></span>

## <span data-ttu-id="b797f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b797f-112">PARAMETERS</span></span>

### <span data-ttu-id="b797f-113">-Konto-Nr</span><span class="sxs-lookup"><span data-stu-id="b797f-113">-AccountId</span></span>
<span data-ttu-id="b797f-114">Gibt die Konto-ID für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="b797f-114">Specifies the account ID for the certificate issuer.</span></span>

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

### <span data-ttu-id="b797f-115">-Apischluessel</span><span class="sxs-lookup"><span data-stu-id="b797f-115">-ApiKey</span></span>
<span data-ttu-id="b797f-116">Gibt den API-Schlüssel für den Aussteller des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="b797f-116">Specifies the API key for the certificate issuer.</span></span>

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

### <span data-ttu-id="b797f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b797f-117">-DefaultProfile</span></span>
<span data-ttu-id="b797f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="b797f-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b797f-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b797f-119">-InputObject</span></span>
<span data-ttu-id="b797f-120">Gibt den Zertifikataussteller an, der festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b797f-120">Specifies the certificate issuer to set.</span></span>

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

### <span data-ttu-id="b797f-121">-IssuerProvider</span><span class="sxs-lookup"><span data-stu-id="b797f-121">-IssuerProvider</span></span>
<span data-ttu-id="b797f-122">Gibt den Typ des Zertifikatausstellers an.</span><span class="sxs-lookup"><span data-stu-id="b797f-122">Specifies the type of certificate issuer.</span></span>

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

### <span data-ttu-id="b797f-123">-Name</span><span class="sxs-lookup"><span data-stu-id="b797f-123">-Name</span></span>
<span data-ttu-id="b797f-124">Gibt den Namen des Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="b797f-124">Specifies the name of the Issuer.</span></span>

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

### <span data-ttu-id="b797f-125">-OrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b797f-125">-OrganizationDetails</span></span>
<span data-ttu-id="b797f-126">Die für den Aussteller zu verwendenden Organisationsdetails.</span><span class="sxs-lookup"><span data-stu-id="b797f-126">Organization details to be used with the issuer.</span></span>

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

### <span data-ttu-id="b797f-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b797f-127">-PassThru</span></span>
<span data-ttu-id="b797f-128">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b797f-128">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b797f-129">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="b797f-129">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b797f-130">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="b797f-130">-VaultName</span></span>
<span data-ttu-id="b797f-131">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="b797f-131">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="b797f-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b797f-132">-Confirm</span></span>
<span data-ttu-id="b797f-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b797f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b797f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b797f-134">-WhatIf</span></span>
<span data-ttu-id="b797f-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b797f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b797f-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b797f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b797f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b797f-137">CommonParameters</span></span>
<span data-ttu-id="b797f-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b797f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b797f-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b797f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b797f-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b797f-140">INPUTS</span></span>

### <span data-ttu-id="b797f-141">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateOrganizationDetails</span><span class="sxs-lookup"><span data-stu-id="b797f-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateOrganizationDetails</span></span>

### <span data-ttu-id="b797f-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="b797f-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="b797f-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b797f-143">OUTPUTS</span></span>

### <span data-ttu-id="b797f-144">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificatePolicy</span><span class="sxs-lookup"><span data-stu-id="b797f-144">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificatePolicy</span></span>

## <span data-ttu-id="b797f-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="b797f-145">NOTES</span></span>

## <span data-ttu-id="b797f-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b797f-146">RELATED LINKS</span></span>

[<span data-ttu-id="b797f-147">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b797f-147">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="b797f-148">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="b797f-148">Remove-AzKeyVaultCertificateIssuer</span></span>](./Remove-AzKeyVaultCertificateIssuer.md)

