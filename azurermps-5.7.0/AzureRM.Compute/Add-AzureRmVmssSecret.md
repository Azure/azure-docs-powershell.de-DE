---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssSecret.md
ms.openlocfilehash: 7fe1fd25801c2aa02ba6c1506f4792fda99d94de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662242"
---
# <span data-ttu-id="0a272-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="0a272-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="0a272-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0a272-102">SYNOPSIS</span></span>
<span data-ttu-id="0a272-103">Fügt einen Schlüssel zu einem VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a272-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a272-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0a272-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <VirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a272-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0a272-105">DESCRIPTION</span></span>
<span data-ttu-id="0a272-106">Das **Add-AzureRmVmssSecret-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) einen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a272-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="0a272-107">Der Schlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="0a272-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="0a272-108">Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="0a272-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="0a272-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="0a272-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="0a272-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) in der Microsoft Developer-Netzwerkbibliothek oder im Cmdlet " [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) ".</span><span class="sxs-lookup"><span data-stu-id="0a272-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="0a272-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0a272-111">EXAMPLES</span></span>

### <span data-ttu-id="0a272-112">Beispiel 1: Hinzufügen eines Geheimnisses zum VMSS</span><span class="sxs-lookup"><span data-stu-id="0a272-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="0a272-113">In diesem Beispiel wird der VMSS ein Schlüssel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="0a272-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="0a272-114">Der erste Befehl verwendet das Get-AzureRmKeyVault-Cmdlet, um einen Vault Secret aus dem Vault mit dem Namen ContosoVault abzurufen, und speichert das Ergebnis in der Variablen mit dem Namen $Vault.</span><span class="sxs-lookup"><span data-stu-id="0a272-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="0a272-115">Der zweite Befehl verwendet das Cmdlet **New-AzureRmVmssVaultCertificateConfig** zum Erstellen einer Schlüsseldepot-Zertifikatkonfiguration unter Verwendung der angegebenen Zertifikat-URL aus dem Zertifikatspeicher mit dem Namen Zertifikate und speichert die Ergebnisse in der Variablen mit dem Namen $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="0a272-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="0a272-116">Der dritte Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="0a272-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="0a272-117">Der vierte Befehl fügt dem VMSS mithilfe der Schlüsselressourcen-ID und des Vault-Zertifikats, das in den $Vault-und $CertConfig Variablen gespeichert ist, einen geheimen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="0a272-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="0a272-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0a272-118">PARAMETERS</span></span>

### <span data-ttu-id="0a272-119">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="0a272-119">-SourceVaultId</span></span>
<span data-ttu-id="0a272-120">Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="0a272-120">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="0a272-121">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="0a272-121">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="0a272-122">Das bedeutet, dass Sie für den *SourceVaultId* -Parameter denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsselspeicher hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0a272-122">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a272-123">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="0a272-123">-VaultCertificate</span></span>
<span data-ttu-id="0a272-124">Gibt das Vault **Certificate** -Objekt an, das die Zertifikat-URL und den Zertifikatsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="0a272-124">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="0a272-125">Sie können das Cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a272-125">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VaultCertificate[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0a272-126">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="0a272-126">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="0a272-127">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="0a272-127">Specifies the VMSS object.</span></span>
<span data-ttu-id="0a272-128">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0a272-128">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0a272-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0a272-129">-Confirm</span></span>
<span data-ttu-id="0a272-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0a272-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a272-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a272-131">-WhatIf</span></span>
<span data-ttu-id="0a272-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0a272-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0a272-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0a272-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a272-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a272-134">CommonParameters</span></span>
<span data-ttu-id="0a272-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a272-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a272-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a272-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a272-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0a272-137">INPUTS</span></span>

### <span data-ttu-id="0a272-138">Keine</span><span class="sxs-lookup"><span data-stu-id="0a272-138">None</span></span>
<span data-ttu-id="0a272-139">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0a272-139">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0a272-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0a272-140">OUTPUTS</span></span>

###  
<span data-ttu-id="0a272-141">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="0a272-141">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="0a272-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="0a272-142">NOTES</span></span>

## <span data-ttu-id="0a272-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0a272-143">RELATED LINKS</span></span>

[<span data-ttu-id="0a272-144">Neu – AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="0a272-144">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="0a272-145">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="0a272-145">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
