---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 061b16758386cf2e279250a1ab72cdcf4180a1f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179258"
---
# <span data-ttu-id="9eef3-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9eef3-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9eef3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9eef3-102">SYNOPSIS</span></span>
<span data-ttu-id="9eef3-103">Löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="9eef3-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="9eef3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9eef3-104">SYNTAX</span></span>

### <span data-ttu-id="9eef3-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="9eef3-105">Default (Default)</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eef3-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="9eef3-106">InputObject</span></span>
```
Remove-AzKeyVaultCertificateIssuer [-InputObject] <PSKeyVaultCertificateIssuerIdentityItem> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9eef3-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9eef3-107">DESCRIPTION</span></span>
<span data-ttu-id="9eef3-108">Das Cmdlet **Remove-AzKeyVaultCertificateIssuer** löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="9eef3-108">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="9eef3-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9eef3-109">EXAMPLES</span></span>

### <span data-ttu-id="9eef3-110">Beispiel 1: Entfernen eines Zertifikatsausstellers</span><span class="sxs-lookup"><span data-stu-id="9eef3-110">Example 1: Remove a certificate issuer</span></span>
```powershell
PS C:\> Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force

AccountId           :
ApiKey              :
OrganizationDetails :
Name                : TestIssuer01
IssuerProvider      : test
VaultName           : ContosoKV01
```

<span data-ttu-id="9eef3-111">Mit diesem Befehl wird der Zertifikataussteller namens TestIssuer01 aus dem ContosoKV01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="9eef3-111">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="9eef3-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9eef3-112">PARAMETERS</span></span>

### <span data-ttu-id="9eef3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eef3-113">-DefaultProfile</span></span>
<span data-ttu-id="9eef3-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9eef3-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eef3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="9eef3-115">-Force</span></span>
<span data-ttu-id="9eef3-116">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="9eef3-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9eef3-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9eef3-117">-InputObject</span></span>
<span data-ttu-id="9eef3-118">Zertifikataussteller Objekt</span><span class="sxs-lookup"><span data-stu-id="9eef3-118">Certificate Issuer Object</span></span>

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

### <span data-ttu-id="9eef3-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9eef3-119">-Name</span></span>
<span data-ttu-id="9eef3-120">Gibt den Namen des zu entfernenden Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="9eef3-120">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="9eef3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eef3-121">-PassThru</span></span>
<span data-ttu-id="9eef3-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9eef3-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eef3-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9eef3-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eef3-124">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="9eef3-124">-VaultName</span></span>
<span data-ttu-id="9eef3-125">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="9eef3-125">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="9eef3-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9eef3-126">-Confirm</span></span>
<span data-ttu-id="9eef3-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9eef3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eef3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eef3-128">-WhatIf</span></span>
<span data-ttu-id="9eef3-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9eef3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eef3-130">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9eef3-130">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9eef3-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9eef3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eef3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eef3-132">CommonParameters</span></span>
<span data-ttu-id="9eef3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9eef3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eef3-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9eef3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eef3-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9eef3-135">INPUTS</span></span>

### <span data-ttu-id="9eef3-136">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuerIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9eef3-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuerIdentityItem</span></span>

## <span data-ttu-id="9eef3-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9eef3-137">OUTPUTS</span></span>

### <span data-ttu-id="9eef3-138">Microsoft. Azure. Commands. keyvault. Models. PSKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9eef3-138">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="9eef3-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="9eef3-139">NOTES</span></span>

## <span data-ttu-id="9eef3-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9eef3-140">RELATED LINKS</span></span>

[<span data-ttu-id="9eef3-141">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9eef3-141">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="9eef3-142">Satz-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="9eef3-142">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


