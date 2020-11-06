---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: 2D3021B3-12C5-4797-8BF2-800E3CEAC56C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/add-azurekeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Add-AzureKeyVaultCertificateContact.md
ms.openlocfilehash: c56dad380d1e5a43b3f4dafdc0e0e964e6264ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504413"
---
# <span data-ttu-id="05050-101">Add-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05050-101">Add-AzureKeyVaultCertificateContact</span></span>

## <span data-ttu-id="05050-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="05050-102">SYNOPSIS</span></span>
<span data-ttu-id="05050-103">Fügt einen Kontakt für Zertifikat Benachrichtigungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="05050-103">Adds a contact for certificate notifications.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05050-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="05050-104">SYNTAX</span></span>

### <span data-ttu-id="05050-105">Interaktiv (Standard)</span><span class="sxs-lookup"><span data-stu-id="05050-105">Interactive (Default)</span></span>
```
Add-AzureKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05050-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="05050-106">ByObject</span></span>
```
Add-AzureKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05050-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="05050-107">ByResourceId</span></span>
```
Add-AzureKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05050-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="05050-108">DESCRIPTION</span></span>
<span data-ttu-id="05050-109">Das Cmdlet **Add-AzureKeyVaultCertificateContact** fügt einen Kontakt für einen schlüsseltresor für Zertifikat Benachrichtigungen im Azure Key Vault hinzu.</span><span class="sxs-lookup"><span data-stu-id="05050-109">The **Add-AzureKeyVaultCertificateContact** cmdlet adds a contact for a key vault for certificate notifications in Azure Key Vault.</span></span>
<span data-ttu-id="05050-110">Der Kontakt erhält Updates zu Ereignissen wie Zertifikat in der Nähe von Ablauf, Zertifikat erneuert usw.</span><span class="sxs-lookup"><span data-stu-id="05050-110">The contact receives updates about events such as certificate close to expiry, certificate renewed, and so on.</span></span>
<span data-ttu-id="05050-111">Diese Ereignisse werden durch die Zertifikatrichtlinie bestimmt.</span><span class="sxs-lookup"><span data-stu-id="05050-111">These events are determined by the certificate policy.</span></span>

## <span data-ttu-id="05050-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="05050-112">EXAMPLES</span></span>

### <span data-ttu-id="05050-113">Beispiel 1: Hinzufügen eines Key Vault-Zertifikats Kontakts</span><span class="sxs-lookup"><span data-stu-id="05050-113">Example 1: Add a key vault certificate contact</span></span>
```powershell
PS C:\> Add-AzureKeyVaultCertificateContact -VaultName "ContosoKV01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email                    VaultName
-----                    ---------
patti.fuller@contoso.com ContosoKV01
```

<span data-ttu-id="05050-114">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den ContosoKV01-schlüsseltresor hinzugefügt und die Liste der Kontakte für den Vault "ContosoKV01" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="05050-114">This command adds Patti Fuller as a certificate contact for the ContosoKV01 key vault and returns the list of contacts for the "ContosoKV01" vault.</span></span>

## <span data-ttu-id="05050-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="05050-115">PARAMETERS</span></span>

### <span data-ttu-id="05050-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05050-116">-DefaultProfile</span></span>
<span data-ttu-id="05050-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="05050-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="05050-118">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="05050-118">-EmailAddress</span></span>
<span data-ttu-id="05050-119">Gibt die e-Mail-Adresse des Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="05050-119">Specifies the email address of the contact.</span></span>

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

### <span data-ttu-id="05050-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="05050-120">-InputObject</span></span>
<span data-ttu-id="05050-121">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="05050-121">KeyVault object.</span></span>

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

### <span data-ttu-id="05050-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="05050-122">-PassThru</span></span>
<span data-ttu-id="05050-123">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="05050-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="05050-124">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="05050-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="05050-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="05050-125">-ResourceId</span></span>
<span data-ttu-id="05050-126">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="05050-126">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="05050-127">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="05050-127">-VaultName</span></span>
<span data-ttu-id="05050-128">Gibt den Namen des Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="05050-128">Specifies the name of the key vault.</span></span>

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

### <span data-ttu-id="05050-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="05050-129">-Confirm</span></span>
<span data-ttu-id="05050-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="05050-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05050-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05050-131">-WhatIf</span></span>
<span data-ttu-id="05050-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="05050-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05050-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="05050-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05050-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05050-134">CommonParameters</span></span>
<span data-ttu-id="05050-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05050-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05050-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05050-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05050-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="05050-137">INPUTS</span></span>

### <span data-ttu-id="05050-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="05050-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>
<span data-ttu-id="05050-139">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="05050-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="05050-140">System. String</span><span class="sxs-lookup"><span data-stu-id="05050-140">System.String</span></span>

## <span data-ttu-id="05050-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="05050-141">OUTPUTS</span></span>

### <span data-ttu-id="05050-142">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05050-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="05050-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="05050-143">NOTES</span></span>

## <span data-ttu-id="05050-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="05050-144">RELATED LINKS</span></span>

[<span data-ttu-id="05050-145">Get-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05050-145">Get-AzureKeyVaultCertificateContact</span></span>](./Get-AzureKeyVaultCertificateContact.md)

[<span data-ttu-id="05050-146">Remove-AzureKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="05050-146">Remove-AzureKeyVaultCertificateContact</span></span>](./Remove-AzureKeyVaultCertificateContact.md)

