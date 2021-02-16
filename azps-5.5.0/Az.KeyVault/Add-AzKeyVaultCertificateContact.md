---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/add-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Add-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 5b6661bada9b63485f937a0401064de2c33e3336
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170483"
---
# <span data-ttu-id="3fbfa-101">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3fbfa-101">Add-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3fbfa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3fbfa-102">SYNOPSIS</span></span>
<span data-ttu-id="3fbfa-103">Fügt einen Kontakt für Zertifikatbenachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-103">Adds a contact for certificate notifications.</span></span>

## <span data-ttu-id="3fbfa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3fbfa-104">SYNTAX</span></span>

### <span data-ttu-id="3fbfa-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="3fbfa-105">Interactive (Default)</span></span>
```
Add-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbfa-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="3fbfa-106">ByObject</span></span>
```
Add-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3fbfa-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="3fbfa-107">ByResourceId</span></span>
```
Add-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fbfa-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3fbfa-108">DESCRIPTION</span></span>
<span data-ttu-id="3fbfa-109">Das **Cmdlet "Add-AzKeyVaultCertificateContact"** fügt einen Kontakt für einen Schlüsseltresor für Zertifikatbenachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-109">The **Add-AzKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="3fbfa-110">Der Kontakt empfängt Aktualisierungen zu Ereignissen wie Zertifikaten, die kurz vor Ablauf, erneuern des Zertifikats und so weiter.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="3fbfa-111">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="3fbfa-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3fbfa-112">EXAMPLES</span></span>

### <span data-ttu-id="3fbfa-113">Beispiel 1: Hinzufügen eines Schlüsseltresorzertifikatkontakts</span><span class="sxs-lookup"><span data-stu-id="3fbfa-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="3fbfa-114">Mit diesem Befehl wird Auchi Fuller als Zertifikatkontakt für den Schlüsseltresor ContosoKV01 hinzugefügt und die Liste der Kontakte für den Tresor "ContosoKV01" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="3fbfa-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3fbfa-115">PARAMETERS</span></span>

### <span data-ttu-id="3fbfa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fbfa-116">-DefaultProfile</span></span>
<span data-ttu-id="3fbfa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="3fbfa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fbfa-118">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="3fbfa-118">-EmailAddress</span></span>
<span data-ttu-id="3fbfa-119">Gibt die E-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="3fbfa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3fbfa-120">-InputObject</span></span>
<span data-ttu-id="3fbfa-121">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-121">KeyVault object.</span></span>

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

### <span data-ttu-id="3fbfa-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fbfa-122">-PassThru</span></span>
<span data-ttu-id="3fbfa-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="3fbfa-124">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="3fbfa-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3fbfa-125">-ResourceId</span></span>
<span data-ttu-id="3fbfa-126">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="3fbfa-127">-VaultName</span><span class="sxs-lookup"><span data-stu-id="3fbfa-127">-VaultName</span></span>
<span data-ttu-id="3fbfa-128">Gibt den Namen des Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="3fbfa-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3fbfa-129">-Confirm</span></span>
<span data-ttu-id="3fbfa-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fbfa-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="3fbfa-131">-WhatIf</span></span>
<span data-ttu-id="3fbfa-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fbfa-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fbfa-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fbfa-134">CommonParameters</span></span>
<span data-ttu-id="3fbfa-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fbfa-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fbfa-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3fbfa-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fbfa-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3fbfa-137">INPUTS</span></span>

### <span data-ttu-id="3fbfa-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fbfa-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="3fbfa-139">System.String</span><span class="sxs-lookup"><span data-stu-id="3fbfa-139">System.String</span></span>

## <span data-ttu-id="3fbfa-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3fbfa-140">OUTPUTS</span></span>

### <span data-ttu-id="3fbfa-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3fbfa-141">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="3fbfa-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3fbfa-142">NOTES</span></span>

## <span data-ttu-id="3fbfa-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3fbfa-143">RELATED LINKS</span></span>

[<span data-ttu-id="3fbfa-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3fbfa-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="3fbfa-145">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="3fbfa-145">Remove-AzKeyVaultCertificateContact</span></span>](./Remove-AzKeyVaultCertificateContact.md)

