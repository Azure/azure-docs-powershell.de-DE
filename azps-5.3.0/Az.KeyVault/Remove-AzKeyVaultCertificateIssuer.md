---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458323"
---
# <span data-ttu-id="cc80f-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cc80f-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="cc80f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cc80f-102">SYNOPSIS</span></span>
<span data-ttu-id="cc80f-103">Löscht einen Zertifikataussteller aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="cc80f-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="cc80f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="cc80f-104">SYNTAX</span></span>

### <span data-ttu-id="cc80f-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="cc80f-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cc80f-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cc80f-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cc80f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cc80f-107">DESCRIPTION</span></span>
<span data-ttu-id="cc80f-108">Das **Cmdlet "Remove-AzKeyVaultCertificateIssuer"** löscht einen Zertifikataussteller aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="cc80f-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="cc80f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="cc80f-109">EXAMPLES</span></span>

### <span data-ttu-id="cc80f-110">Beispiel 1: Entfernen eines Zertifikatausstellers</span><span class="sxs-lookup"><span data-stu-id="cc80f-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="cc80f-111">Mit diesem Befehl wird der Zertifikataussteller "TestIssuer01" aus dem Schlüsseltresor ContosoKV01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="cc80f-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="cc80f-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cc80f-112">PARAMETERS</span></span>

### <span data-ttu-id="cc80f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cc80f-113">-DefaultProfile</span></span>
<span data-ttu-id="cc80f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="cc80f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cc80f-115">-Force</span><span class="sxs-lookup"><span data-stu-id="cc80f-115">-Force</span></span>
<span data-ttu-id="cc80f-116">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="cc80f-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cc80f-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cc80f-117">-InputObject</span></span>
<span data-ttu-id="cc80f-118">Zertifikatausstellerobjekt</span><span class="sxs-lookup"><span data-stu-id="cc80f-118">Certificate Issuer Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cc80f-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cc80f-119">-Name</span></span>
<span data-ttu-id="cc80f-120">Gibt den Namen des Ausstellers an, der entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="cc80f-120">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc80f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cc80f-121">-PassThru</span></span>
<span data-ttu-id="cc80f-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="cc80f-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cc80f-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="cc80f-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cc80f-124">-VaultName</span><span class="sxs-lookup"><span data-stu-id="cc80f-124">-VaultName</span></span>
<span data-ttu-id="cc80f-125">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="cc80f-125">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cc80f-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cc80f-126">-Confirm</span></span>
<span data-ttu-id="cc80f-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="cc80f-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cc80f-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="cc80f-128">-WhatIf</span></span>
<span data-ttu-id="cc80f-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc80f-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc80f-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="cc80f-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cc80f-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc80f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cc80f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cc80f-132">CommonParameters</span></span>
<span data-ttu-id="cc80f-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cc80f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cc80f-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cc80f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cc80f-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="cc80f-135">INPUTS</span></span>

### <span data-ttu-id="cc80f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="cc80f-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="cc80f-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="cc80f-137">OUTPUTS</span></span>

### <span data-ttu-id="cc80f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cc80f-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="cc80f-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="cc80f-139">NOTES</span></span>

## <span data-ttu-id="cc80f-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="cc80f-140">RELATED LINKS</span></span>

[<span data-ttu-id="cc80f-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cc80f-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="cc80f-142">Set-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="cc80f-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


