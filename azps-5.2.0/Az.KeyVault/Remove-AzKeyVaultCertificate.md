---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 34985F06-4D8D-463B-B113-972666D18485
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificate.md
ms.openlocfilehash: c6d99fb2b6b568b090cb0ed86277b06fcde28115
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290105"
---
# <span data-ttu-id="c821f-101">Remove-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c821f-101">Remove-AzKeyVaultCertificate</span></span>

## <span data-ttu-id="c821f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c821f-102">SYNOPSIS</span></span>
<span data-ttu-id="c821f-103">Entfernt ein Zertifikat aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c821f-103">Removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c821f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c821f-104">SYNTAX</span></span>

### <span data-ttu-id="c821f-105">ByVaultNameAndName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c821f-105">ByVaultNameAndName (Default)</span></span>
```
Remove-AzKeyVaultCertificate [-VaultName] <String> [-Name] <String> [-InRemovedState] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c821f-106">ByObject</span><span class="sxs-lookup"><span data-stu-id="c821f-106">ByObject</span></span>
```
Remove-AzKeyVaultCertificate [-InputObject] <PSKeyVaultCertificateIdentityItem> [-InRemovedState] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c821f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c821f-107">DESCRIPTION</span></span>
<span data-ttu-id="c821f-108">Das **Cmdlet "Remove-AzKeyVaultCertificate"** entfernt ein Zertifikat aus einem Schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="c821f-108">The **Remove-AzKeyVaultCertificate** cmdlet removes a certificate from a key vault.</span></span>

## <span data-ttu-id="c821f-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c821f-109">EXAMPLES</span></span>

### <span data-ttu-id="c821f-110">Beispiel 1: Entfernen eines Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c821f-110">Example 1: Remove a certificate</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName "ContosoKV01" -Name "SelfSigned01" -PassThru -Force

Certificate        : [Subject]
                       CN=contoso.com

                     [Issuer]
                       CN=contoso.com

                     [Serial Number]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

                     [Not Before]
                       4/11/2018 4:28:39 PM

                     [Not After]
                       10/11/2018 4:38:39 PM

                     [Thumbprint]
                       XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX

KeyId              : https://contosokv01.vault.azure.net:443/keys/selfsigned01/968c3920884a435abf8faea11f565456
SecretId           : https://contosokv01.vault.azure.net:443/secrets/selfsigned01/968c3920884a435abf8faea11f565456
Thumbprint         : XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
RecoveryLevel      : Purgeable
ScheduledPurgeDate :
DeletedDate        :
Enabled            : True
Expires            : 10/11/2018 11:38:39 PM
NotBefore          : 4/11/2018 11:28:39 PM
Created            : 4/11/2018 11:38:39 PM
Updated            : 4/11/2018 11:38:39 PM
Tags               :
VaultName          : ContosoKV01
Name               : SelfSigned01
Version            : 968c3920884a435abf8faea11f565456
Id                 : https://contosokv01.vault.azure.net:443/certificates/selfsigned01/968c3920884a435abf8faea11f565456
```

<span data-ttu-id="c821f-111">Mit diesem Befehl wird das Zertifikat mit dem Namen "SelfSigned01" aus dem Schlüsseltresor "ContosoKV01" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c821f-111">This command removes the certificate named SelfSigned01 from the key vault named ContosoKV01.</span></span>
<span data-ttu-id="c821f-112">Dieser Befehl gibt den Parameter *"Force"* an.</span><span class="sxs-lookup"><span data-stu-id="c821f-112">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="c821f-113">Daher werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="c821f-113">Therefore, the cmdlet does not prompt you for confirmation.</span></span>

### <span data-ttu-id="c821f-114">Beispiel 2: Endgültiges Löschen des gelöschten Zertifikats aus dem Schlüsseltresor</span><span class="sxs-lookup"><span data-stu-id="c821f-114">Example 2: Purge the deleted certificate from the key vault permanently</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificate -VaultName 'Contoso' -Name 'MyCert' -InRemovedState
```

<span data-ttu-id="c821f-115">Mit diesem Befehl wird das Zertifikat mit dem Namen "MyCert" dauerhaft aus dem Schlüsseltresor namens "Contoso" entfernt.</span><span class="sxs-lookup"><span data-stu-id="c821f-115">This command permanently removes the certificate named 'MyCert' from the key vault named 'Contoso'.</span></span>
<span data-ttu-id="c821f-116">Zum Ausführen dieses Cmdlets ist die Berechtigung zum Löschen erforderlich, die dem Benutzer in diesem Schlüsseltresor zuvor explizit erteilt worden sein muss.</span><span class="sxs-lookup"><span data-stu-id="c821f-116">Executing this cmdlet requires the 'purge' permission, which must have been previously and explicitly granted to the user on this key vault.</span></span>

## <span data-ttu-id="c821f-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c821f-117">PARAMETERS</span></span>

### <span data-ttu-id="c821f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c821f-118">-DefaultProfile</span></span>
<span data-ttu-id="c821f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c821f-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c821f-120">-Force</span><span class="sxs-lookup"><span data-stu-id="c821f-120">-Force</span></span>
<span data-ttu-id="c821f-121">Erzwingt die Ausführung des Befehls ohne Benutzerbestätigung.</span><span class="sxs-lookup"><span data-stu-id="c821f-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c821f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c821f-122">-InputObject</span></span>
<span data-ttu-id="c821f-123">Zertifikatobjekt.</span><span class="sxs-lookup"><span data-stu-id="c821f-123">Certificate Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem
Parameter Sets: ByObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c821f-124">-InRemovedState</span><span class="sxs-lookup"><span data-stu-id="c821f-124">-InRemovedState</span></span>
<span data-ttu-id="c821f-125">Wenn vorhanden, entfernt das zuvor gelöschte Zertifikat dauerhaft</span><span class="sxs-lookup"><span data-stu-id="c821f-125">If present, removes the previously deleted certificate permanently</span></span>

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

### <span data-ttu-id="c821f-126">-Name</span><span class="sxs-lookup"><span data-stu-id="c821f-126">-Name</span></span>
<span data-ttu-id="c821f-127">Gibt den Namen des Zertifikats an, das dieses Cmdlet aus einem Schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="c821f-127">Specifies the name of the certificate that this cmdlet removes from a key vault.</span></span>
<span data-ttu-id="c821f-128">Dieses Cmdlet erstellt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) eines Zertifikats basierend auf dem Namen, den dieser Parameter angibt, dem Namen des Schlüsseltresor und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c821f-128">This cmdlet constructs the fully qualified domain name (FQDN) of a certificate based on the name that this parameter specifies, the name of the key vault, and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c821f-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c821f-129">-PassThru</span></span>
<span data-ttu-id="c821f-130">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="c821f-130">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="c821f-131">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="c821f-131">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c821f-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="c821f-132">-VaultName</span></span>
<span data-ttu-id="c821f-133">Gibt den Namen des Schlüsseltresor an, aus dem dieses Cmdlet ein Zertifikat entfernt.</span><span class="sxs-lookup"><span data-stu-id="c821f-133">Specifies the name of the key vault from which this cmdlet removes a certificate.</span></span>
<span data-ttu-id="c821f-134">Dieses Cmdlet erstellt den FQDN eines Schlüsseltresor basierend auf dem Namen, den dieser Parameter angibt, und Ihrer aktuellen Umgebung.</span><span class="sxs-lookup"><span data-stu-id="c821f-134">This cmdlet constructs the FQDN of a key vault based on the name that this parameter specifies and your current environment.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVaultNameAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c821f-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c821f-135">-Confirm</span></span>
<span data-ttu-id="c821f-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c821f-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c821f-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c821f-137">-WhatIf</span></span>
<span data-ttu-id="c821f-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c821f-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c821f-139">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c821f-139">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c821f-140">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c821f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c821f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c821f-141">CommonParameters</span></span>
<span data-ttu-id="c821f-142">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c821f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c821f-143">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c821f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c821f-144">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c821f-144">INPUTS</span></span>

### <span data-ttu-id="c821f-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span><span class="sxs-lookup"><span data-stu-id="c821f-145">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIdentityItem</span></span>

## <span data-ttu-id="c821f-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c821f-146">OUTPUTS</span></span>

### <span data-ttu-id="c821f-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c821f-147">Microsoft.Azure.Commands.KeyVault.Models.PSDeletedKeyVaultCertificate</span></span>

## <span data-ttu-id="c821f-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c821f-148">NOTES</span></span>

## <span data-ttu-id="c821f-149">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c821f-149">RELATED LINKS</span></span>

[<span data-ttu-id="c821f-150">Add-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c821f-150">Add-AzKeyVaultCertificate</span></span>](./Add-AzKeyVaultCertificate.md)

[<span data-ttu-id="c821f-151">Get-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c821f-151">Get-AzKeyVaultCertificate</span></span>](./Get-AzKeyVaultCertificate.md)

[<span data-ttu-id="c821f-152">Import-AzKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="c821f-152">Import-AzKeyVaultCertificate</span></span>](./Import-AzKeyVaultCertificate.md)

[<span data-ttu-id="c821f-153">Undo-AzKeyVaultCertificateRemoval</span><span class="sxs-lookup"><span data-stu-id="c821f-153">Undo-AzKeyVaultCertificateRemoval</span></span>](./Undo-AzKeyVaultCertificateRemoval.md)
