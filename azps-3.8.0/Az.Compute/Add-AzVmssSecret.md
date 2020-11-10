---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: 6f9f1f29f23906442d7c9c8187b9bab3bf41403b
ms.sourcegitcommit: 7aaa37edc9681b643946505bcbc3cc6435f1d7ca
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/10/2020
ms.locfileid: "94395474"
---
# <span data-ttu-id="60662-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="60662-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="60662-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="60662-102">SYNOPSIS</span></span>
<span data-ttu-id="60662-103">Fügt einen Schlüssel zu einem VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="60662-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="60662-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="60662-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="60662-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="60662-105">DESCRIPTION</span></span>
<span data-ttu-id="60662-106">Das **Add-AzVmssSecret-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) einen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="60662-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="60662-107">Der Schlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="60662-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="60662-108">Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="60662-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="60662-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="60662-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="60662-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](/powershell/module/az.keyvault) oder dem Cmdlet " [AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) ".</span><span class="sxs-lookup"><span data-stu-id="60662-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="60662-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="60662-111">EXAMPLES</span></span>

### <span data-ttu-id="60662-112">Beispiel 1: Hinzufügen eines Geheimnisses zum VMSS</span><span class="sxs-lookup"><span data-stu-id="60662-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="60662-113">In diesem Beispiel wird der VMSS ein Schlüssel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="60662-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="60662-114">Der erste Befehl verwendet das Get-AzKeyVault-Cmdlet, um einen Vault Secret aus dem Vault mit dem Namen ContosoVault abzurufen, und speichert das Ergebnis in der Variablen mit dem Namen $Vault.</span><span class="sxs-lookup"><span data-stu-id="60662-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="60662-115">Der zweite Befehl verwendet das Cmdlet **New-AzVmssVaultCertificateConfig** zum Erstellen einer Schlüsseldepot-Zertifikatkonfiguration unter Verwendung der angegebenen Zertifikat-URL aus dem Zertifikatspeicher mit dem Namen Zertifikate und speichert die Ergebnisse in der Variablen mit dem Namen $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="60662-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="60662-116">Der dritte Befehl verwendet das Cmdlet **New-AzVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="60662-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="60662-117">Der vierte Befehl fügt dem VMSS mithilfe der Schlüsselressourcen-ID und des Vault-Zertifikats, das in den $Vault-und $CertConfig Variablen gespeichert ist, einen geheimen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="60662-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="60662-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="60662-118">PARAMETERS</span></span>

### <span data-ttu-id="60662-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60662-119">-DefaultProfile</span></span>
<span data-ttu-id="60662-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="60662-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60662-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="60662-121">-SourceVaultId</span></span>
<span data-ttu-id="60662-122">Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="60662-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="60662-123">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="60662-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="60662-124">Das bedeutet, dass Sie für den *SourceVaultId* -Parameter denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsselspeicher hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="60662-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60662-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="60662-125">-VaultCertificate</span></span>
<span data-ttu-id="60662-126">Gibt das Vault **Certificate** -Objekt an, das die Zertifikat-URL und den Zertifikatsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="60662-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="60662-127">Sie können das Cmdlet [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60662-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VaultCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60662-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="60662-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="60662-129">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="60662-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="60662-130">Sie können das Cmdlet [New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="60662-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="60662-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="60662-131">-Confirm</span></span>
<span data-ttu-id="60662-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60662-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60662-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60662-133">-WhatIf</span></span>
<span data-ttu-id="60662-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60662-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="60662-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60662-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60662-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60662-136">CommonParameters</span></span>
<span data-ttu-id="60662-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60662-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60662-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="60662-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60662-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="60662-139">INPUTS</span></span>

### <span data-ttu-id="60662-140">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="60662-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="60662-141">System. String</span><span class="sxs-lookup"><span data-stu-id="60662-141">System.String</span></span>

### <span data-ttu-id="60662-142">Microsoft. Azure. Management. Compute. Models. VaultCertificate []</span><span class="sxs-lookup"><span data-stu-id="60662-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="60662-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="60662-143">OUTPUTS</span></span>

### <span data-ttu-id="60662-144">Microsoft. Azure. Commands. Compute. Automation. Models. PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="60662-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="60662-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="60662-145">NOTES</span></span>

## <span data-ttu-id="60662-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="60662-146">RELATED LINKS</span></span>

[<span data-ttu-id="60662-147">Neu – AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="60662-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="60662-148">Neu – AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="60662-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
