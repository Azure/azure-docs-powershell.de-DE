---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 7cf5070b6f03c7bc19b8d05991314569616c06ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927976"
---
# <span data-ttu-id="b67e6-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b67e6-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b67e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b67e6-102">SYNOPSIS</span></span>
<span data-ttu-id="b67e6-103">Fügt einen Kontakt für Zertifikatbenachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="b67e6-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="b67e6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b67e6-104">SYNTAX</span></span>

### <span data-ttu-id="b67e6-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="b67e6-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b67e6-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="b67e6-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b67e6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b67e6-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b67e6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b67e6-108">DESCRIPTION</span></span>
<span data-ttu-id="b67e6-109">Das **Add-AzKeyVertificateContact-Cmdlet** fügt einen Kontakt für einen Schlüsseltresor für Zertifikatbenachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="b67e6-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="b67e6-110">Der Kontakt empfängt Updates zu Ereignissen wie Zertifikat, das kurz vor ablaufend ist, Zertifikat verlängert und so weiter.</span><span class="sxs-lookup"><span data-stu-id="b67e6-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="b67e6-111">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="b67e6-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="b67e6-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b67e6-112">EXAMPLES</span></span>

### <span data-ttu-id="b67e6-113">Beispiel 1: Hinzufügen eines Schlüsseltresorzertifikatkontakts</span><span class="sxs-lookup"><span data-stu-id="b67e6-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="b67e6-114">Mit diesem Befehl wird Chris Fuller als Zertifikatkontakt für den ContosoKV01-Schlüsseltresor hinzugefügt und die Kontaktliste für den Tresor "ContosoKV01" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b67e6-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="b67e6-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b67e6-115">PARAMETERS</span></span>

### <span data-ttu-id="b67e6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b67e6-116">-DefaultProfile</span></span>
<span data-ttu-id="b67e6-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="b67e6-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b67e6-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="b67e6-118">-EmailAddress</span></span>
<span data-ttu-id="b67e6-119">Gibt die E-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="b67e6-119">Specifies the email address of the contact.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67e6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b67e6-120">-InputObject</span></span>
<span data-ttu-id="b67e6-121">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b67e6-121">KeyVault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b67e6-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b67e6-122">-PassThru</span></span>
<span data-ttu-id="b67e6-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="b67e6-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="b67e6-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="b67e6-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b67e6-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b67e6-125">-ResourceId</span></span>
<span data-ttu-id="b67e6-126">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b67e6-126">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b67e6-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="b67e6-127">-VaultName</span></span>
<span data-ttu-id="b67e6-128">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="b67e6-128">Specifies the name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b67e6-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b67e6-129">-Confirm</span></span>
<span data-ttu-id="b67e6-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b67e6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b67e6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b67e6-131">-WhatIf</span></span>
<span data-ttu-id="b67e6-132">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b67e6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b67e6-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b67e6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b67e6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b67e6-134">CommonParameters</span></span>
<span data-ttu-id="b67e6-135">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b67e6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b67e6-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b67e6-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b67e6-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b67e6-137">INPUTS</span></span>

### <span data-ttu-id="b67e6-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="b67e6-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="b67e6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="b67e6-139">System.String</span></span>

## <span data-ttu-id="b67e6-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b67e6-140">OUTPUTS</span></span>

### <span data-ttu-id="b67e6-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b67e6-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="b67e6-142">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b67e6-142">NOTES</span></span>

## <span data-ttu-id="b67e6-143">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b67e6-143">RELATED LINKS</span></span>

[<span data-ttu-id="b67e6-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b67e6-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="b67e6-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="b67e6-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

