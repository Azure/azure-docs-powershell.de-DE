---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: FC14F6BF-BD8F-45E0-9CAA-A937E5E56288
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurekeyvaultcertificateissuer
schema: 2.0.0
ms.openlocfilehash: 4c732cdfc175c47e9bd8125234cb1d33f1b19097
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848224"
---
# <span data-ttu-id="360fb-101">Remove-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="360fb-101">Remove-AzureKeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="360fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="360fb-102">SYNOPSIS</span></span>
<span data-ttu-id="360fb-103">Löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="360fb-103">Deletes a certificate issuer from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="360fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="360fb-104">SYNTAX</span></span>

```
Remove-AzureKeyVaultCertificateIssuer [-VaultName] <String> [-Name] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="360fb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="360fb-105">DESCRIPTION</span></span>
<span data-ttu-id="360fb-106">Das Cmdlet **Remove-AzureKeyVaultCertificateIssuer** löscht einen Zertifikataussteller aus einem schlüsseltresor.</span><span class="sxs-lookup"><span data-stu-id="360fb-106">The **Remove-AzureKeyVaultCertificateIssuer** cmdlet deletes a certificate issuer from a key vault.</span></span>

## <span data-ttu-id="360fb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="360fb-107">EXAMPLES</span></span>

### <span data-ttu-id="360fb-108">Beispiel 1: Entfernen eines Zertifikatsausstellers</span><span class="sxs-lookup"><span data-stu-id="360fb-108">Example 1: Remove a certificate issuer</span></span>
```
PS C:\>Remove-AzureKeyVaultCertificateIssuer -VaultName "ContosoKV01" -Name "TestIssuer01" -Force
```

<span data-ttu-id="360fb-109">Mit diesem Befehl wird der Zertifikataussteller namens TestIssuer01 aus dem ContosoKV01-schlüsseltresor entfernt.</span><span class="sxs-lookup"><span data-stu-id="360fb-109">This command removes the certificate issuer named TestIssuer01 from the ContosoKV01 key vault.</span></span>

## <span data-ttu-id="360fb-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="360fb-110">PARAMETERS</span></span>

### <span data-ttu-id="360fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="360fb-111">-DefaultProfile</span></span>
<span data-ttu-id="360fb-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="360fb-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="360fb-113">-Force</span><span class="sxs-lookup"><span data-stu-id="360fb-113">-Force</span></span>
<span data-ttu-id="360fb-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="360fb-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="360fb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="360fb-115">-Name</span></span>
<span data-ttu-id="360fb-116">Gibt den Namen des zu entfernenden Emittenten an.</span><span class="sxs-lookup"><span data-stu-id="360fb-116">Specifies the name of the issuer to remove.</span></span>

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

### <span data-ttu-id="360fb-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="360fb-117">-PassThru</span></span>
<span data-ttu-id="360fb-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="360fb-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="360fb-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="360fb-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="360fb-120">-Vaultname</span><span class="sxs-lookup"><span data-stu-id="360fb-120">-VaultName</span></span>
<span data-ttu-id="360fb-121">Gibt den Namen eines Schlüsseldepots an.</span><span class="sxs-lookup"><span data-stu-id="360fb-121">Specifies the name of a key vault.</span></span>

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

### <span data-ttu-id="360fb-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="360fb-122">-Confirm</span></span>
<span data-ttu-id="360fb-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="360fb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="360fb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="360fb-124">-WhatIf</span></span>
<span data-ttu-id="360fb-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="360fb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360fb-126">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="360fb-126">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="360fb-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="360fb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="360fb-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="360fb-128">CommonParameters</span></span>
<span data-ttu-id="360fb-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="360fb-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="360fb-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="360fb-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="360fb-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="360fb-131">INPUTS</span></span>

## <span data-ttu-id="360fb-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="360fb-132">OUTPUTS</span></span>

### <span data-ttu-id="360fb-133">Microsoft. Azure. Commands. keyvault. Models. KeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="360fb-133">Microsoft.Azure.Commands.KeyVault.Models.KeyVaultCertificateIssuer</span></span>

## <span data-ttu-id="360fb-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="360fb-134">NOTES</span></span>

## <span data-ttu-id="360fb-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="360fb-135">RELATED LINKS</span></span>

[<span data-ttu-id="360fb-136">Get-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="360fb-136">Get-AzureKeyVaultCertificateIssuer</span></span>](./Get-AzureKeyVaultCertificateIssuer.md)

[<span data-ttu-id="360fb-137">Satz-AzureKeyVaultCertificateIssuer</span><span class="sxs-lookup"><span data-stu-id="360fb-137">Set-AzureKeyVaultCertificateIssuer</span></span>](./Set-AzureKeyVaultCertificateIssuer.md)


