---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 35FAA57F-B2BD-4E43-8238-12F7A8269E4D
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificatecontact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateContact.md
ms.openlocfilehash: 12fe8cdc0e8e7210a2db7c7c6ccab1a0fcceeba3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010187"
---
# <span data-ttu-id="ac0be-101">Remove-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ac0be-101">Remove-AzKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ac0be-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac0be-102">SYNOPSIS</span></span>
<span data-ttu-id="ac0be-103">Löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ac0be-103">Deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="ac0be-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac0be-104">SYNTAX</span></span>

### <span data-ttu-id="ac0be-105">ByName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac0be-105">ByName (Default)</span></span>
```
Remove-AzKeyVaultCertificateContact [-VaultName] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0be-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="ac0be-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificateContact [-InputObject] <PSKeyVault> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac0be-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac0be-107">ByResourceId</span></span>
```
Remove-AzKeyVaultCertificateContact [-ResourceId] <String> [-EmailAddress] <String[]> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac0be-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac0be-108">DESCRIPTION</span></span>
<span data-ttu-id="ac0be-109">Das Cmdlet **Remove-AzKeyVaultCertificateContact** löscht einen Kontakt, der für Zertifikat Benachrichtigungen aus einem schlüsseltresor registriert ist.</span><span class="sxs-lookup"><span data-stu-id="ac0be-109">The **Remove-AzKeyVaultCertificateContact** cmdlet deletes a contact that is registered for certificate notifications from a key vault.</span></span>

## <span data-ttu-id="ac0be-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac0be-110">EXAMPLES</span></span>

### <span data-ttu-id="ac0be-111">Beispiel 1: Entfernen eines Zertifikat Kontakts</span><span class="sxs-lookup"><span data-stu-id="ac0be-111">Example 1: Remove a certificate contact</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateContact -VaultName "Contoso01" -EmailAddress "patti.fuller@contoso.com" -PassThru

Email               VaultName
-----               ---------
user1@microsoft.com mvault2
user2@microsoft.com mvault2
user3@microsoft.com mvault2
user4@microsoft.com mvault2
```

<span data-ttu-id="ac0be-112">Mit diesem Befehl wird Patti Fuller als Zertifikat Kontakt für den contoso01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="ac0be-112">This command removes Patti Fuller as a certificate contact for the Contoso01 key vault.</span></span>  <span data-ttu-id="ac0be-113">Wenn passthru angegeben wird, gibt das Cmdlet die Liste der verbleibenden Zertifikat Kontakte zurück.</span><span class="sxs-lookup"><span data-stu-id="ac0be-113">If PassThru is specified, the cmdlet returns the list of remaining certificate contacts.</span></span>

## <span data-ttu-id="ac0be-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac0be-114">PARAMETERS</span></span>

### <span data-ttu-id="ac0be-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac0be-115">-DefaultProfile</span></span>
<span data-ttu-id="ac0be-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ac0be-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac0be-117">-Email-Email</span><span class="sxs-lookup"><span data-stu-id="ac0be-117">-EmailAddress</span></span>
<span data-ttu-id="ac0be-118">Gibt die e-Mail-Adresse des zu entfernenden Kontakts an.</span><span class="sxs-lookup"><span data-stu-id="ac0be-118">Specifies the email address of the contact to remove.</span></span>

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

### <span data-ttu-id="ac0be-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ac0be-119">-InputObject</span></span>
<span data-ttu-id="ac0be-120">Keyvault-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ac0be-120">KeyVault object.</span></span>

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

### <span data-ttu-id="ac0be-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ac0be-121">-PassThru</span></span>
<span data-ttu-id="ac0be-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="ac0be-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="ac0be-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="ac0be-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ac0be-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ac0be-124">-ResourceId</span></span>
<span data-ttu-id="ac0be-125">Keyvault-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ac0be-125">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="ac0be-126">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="ac0be-126">-VaultName</span></span>
<span data-ttu-id="ac0be-127">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="ac0be-127">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="ac0be-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac0be-128">-Confirm</span></span>
<span data-ttu-id="ac0be-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac0be-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac0be-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac0be-130">-WhatIf</span></span>
<span data-ttu-id="ac0be-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac0be-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac0be-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac0be-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac0be-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac0be-133">CommonParameters</span></span>
<span data-ttu-id="ac0be-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac0be-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac0be-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac0be-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac0be-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac0be-136">INPUTS</span></span>

### <span data-ttu-id="ac0be-137">Microsoft. Azure. Commands. keyvault. Models. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="ac0be-137">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="ac0be-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ac0be-138">System.String</span></span>

## <span data-ttu-id="ac0be-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac0be-139">OUTPUTS</span></span>

### <span data-ttu-id="ac0be-140">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ac0be-140">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateContact</span></span>

## <span data-ttu-id="ac0be-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac0be-141">NOTES</span></span>

## <span data-ttu-id="ac0be-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac0be-142">RELATED LINKS</span></span>

[<span data-ttu-id="ac0be-143">Add-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ac0be-143">Add-AzKeyVaultCertificateContact</span></span>](./Add-AzKeyVaultCertificateContact.md)

[<span data-ttu-id="ac0be-144">Get-AzKeyVaultCertificateContact</span><span class="sxs-lookup"><span data-stu-id="ac0be-144">Get-AzKeyVaultCertificateContact</span></span>](./Get-AzKeyVaultCertificateContact.md)

