---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-AzKeyvaultcertificateissuer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultCertificateIssuer.md
ms.openlocfilehash: 204ee5a7a4d0e5247ae3de239dce650deb4cff0c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842115"
---
# <span data-ttu-id="45071-101">Remove-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45071-101">Remove-AzKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="45071-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45071-102">SYNOPSIS</span></span>
<span data-ttu-id="45071-103">Löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="45071-103">Deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="45071-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45071-104">SYNTAX</span></span>

```
Remove-AzKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="45071-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45071-105">DESCRIPTION</span></span>
<span data-ttu-id="45071-106">Das Cmdlet **Remove-AzKeyVaultCertificateIssuer** löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="45071-106">The **Remove-AzKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="45071-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45071-107">EXAMPLES</span></span>

### <span data-ttu-id="45071-108">Beispiel 1: Entfernen eines Zertifikatsausstellers</span><span class="sxs-lookup"><span data-stu-id="45071-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="45071-109">Mit diesem Befehl wird der Zertifikataussteller namens TestIssuer01 aus dem ContosoKV01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="45071-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="45071-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45071-110">PARAMETERS</span></span>

### <span data-ttu-id="45071-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45071-111">-DefaultProfile</span></span>
<span data-ttu-id="45071-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="45071-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45071-113">-Force</span><span class="sxs-lookup"><span data-stu-id="45071-113">-Force</span></span>
<span data-ttu-id="45071-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="45071-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45071-115">-Name</span><span class="sxs-lookup"><span data-stu-id="45071-115">-Name</span></span>
<span data-ttu-id="45071-116">Gibt den Namen des zu entfernenden Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="45071-116">Specifies the name of the issuer to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IssuerName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45071-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45071-117">-PassThru</span></span>
<span data-ttu-id="45071-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="45071-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="45071-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="45071-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45071-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="45071-120">-VaultName</span></span>
<span data-ttu-id="45071-121">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="45071-121">Specifies the name of a key vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45071-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="45071-122">-Confirm</span></span>
<span data-ttu-id="45071-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="45071-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45071-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45071-124">-WhatIf</span></span>
<span data-ttu-id="45071-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45071-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45071-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="45071-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45071-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="45071-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45071-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45071-128">CommonParameters</span></span>
<span data-ttu-id="45071-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45071-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45071-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45071-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45071-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45071-131">INPUTS</span></span>

### <span data-ttu-id="45071-132">Keine</span><span class="sxs-lookup"><span data-stu-id="45071-132">None</span></span>
<span data-ttu-id="45071-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="45071-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="45071-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45071-134">OUTPUTS</span></span>

### <span data-ttu-id="45071-135">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45071-135">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="45071-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="45071-136">NOTES</span></span>

## <span data-ttu-id="45071-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45071-137">RELATED LINKS</span></span>

[<span data-ttu-id="45071-138">Get-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45071-138">Get-AzKeyVaultCertificateIssuer</span></span>](./Get-AzKeyVaultCertificateIssuer.md)

[<span data-ttu-id="45071-139">Satz-AzKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="45071-139">Set-AzKeyVaultCertificateIssuer</span></span>](./Set-AzKeyVaultCertificateIssuer.md)


