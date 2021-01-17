---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469547"
---
# <span data-ttu-id="53141-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53141-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="53141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53141-102">SYNOPSIS</span></span>
<span data-ttu-id="53141-103">Löscht einen Kontakt, der für Zertifikatbenachrichtigungen registriert ist, aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="53141-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="53141-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53141-104">SYNTAX</span></span>

### <span data-ttu-id="53141-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="53141-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53141-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="53141-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53141-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="53141-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="53141-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="53141-108">DESCRIPTION</span></span>
<span data-ttu-id="53141-109">Das **Cmdlet "Remove-AzKeyVaultCertificateContact"** löscht einen Kontakt, der für Zertifikatbenachrichtigungen aus einem Schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="53141-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="53141-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="53141-110">EXAMPLES</span></span>

### <span data-ttu-id="53141-111">Beispiel 1: Entfernen eines Zertifikatkontakts</span><span class="sxs-lookup"><span data-stu-id="53141-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="53141-112">Mit diesem Befehl wird Auchi Fuller als Zertifikatkontakt für den Schlüsseltresor von Contoso01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="53141-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="53141-113">Wird "PassThru" angegeben, gibt das Cmdlet die Liste der verbleibenden Zertifikatkontakte zurück.</span><span class="sxs-lookup"><span data-stu-id="53141-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="53141-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="53141-114">PARAMETERS</span></span>

### <span data-ttu-id="53141-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53141-115">-DefaultProfile</span></span>
<span data-ttu-id="53141-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="53141-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53141-117">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="53141-117">-EmailAddress</span></span>
<span data-ttu-id="53141-118">Gibt die E-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="53141-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="53141-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="53141-119">-InputObject</span></span>
<span data-ttu-id="53141-120">KeyVault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="53141-120">KeyVault object.</span></span>

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

### <span data-ttu-id="53141-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="53141-121">-PassThru</span></span>
<span data-ttu-id="53141-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="53141-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="53141-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="53141-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="53141-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="53141-124">-ResourceId</span></span>
<span data-ttu-id="53141-125">KeyVault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="53141-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="53141-126">-VaultName</span><span class="sxs-lookup"><span data-stu-id="53141-126">-VaultName</span></span>
<span data-ttu-id="53141-127">Gibt den Namen eines Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="53141-127">Specifies the name of a key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53141-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="53141-128">-Confirm</span></span>
<span data-ttu-id="53141-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="53141-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53141-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="53141-130">-WhatIf</span></span>
<span data-ttu-id="53141-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="53141-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="53141-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="53141-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="53141-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53141-133">CommonParameters</span></span>
<span data-ttu-id="53141-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53141-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53141-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="53141-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53141-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="53141-136">INPUTS</span></span>

### <span data-ttu-id="53141-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="53141-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="53141-138">System.String</span><span class="sxs-lookup"><span data-stu-id="53141-138">System.String</span></span>

## <span data-ttu-id="53141-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="53141-139">OUTPUTS</span></span>

### <span data-ttu-id="53141-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53141-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="53141-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="53141-141">NOTES</span></span>

## <span data-ttu-id="53141-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="53141-142">RELATED LINKS</span></span>

[<span data-ttu-id="53141-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53141-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="53141-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="53141-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

