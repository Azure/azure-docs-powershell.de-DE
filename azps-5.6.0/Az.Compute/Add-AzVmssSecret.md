---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsssecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssSecret.md
ms.openlocfilehash: ec07964f62a22385d98c8cd9b8c98ea0b088ec8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927379"
---
# <span data-ttu-id="3f3e0-101">Add-AzVmssSecret</span><span class="sxs-lookup"><span data-stu-id="3f3e0-101">Add-AzVmssSecret</span></span>

## <span data-ttu-id="3f3e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f3e0-102">SYNOPSIS</span></span>
<span data-ttu-id="3f3e0-103">Fügt einem VMSS einen Geheimtipp hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-103">Adds a secret to a VMSS.</span></span>

## <span data-ttu-id="3f3e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f3e0-104">SYNTAX</span></span>

```
Add-AzVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3f3e0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f3e0-105">DESCRIPTION</span></span>
<span data-ttu-id="3f3e0-106">Das **Add-AzVmssSecret-Cmdlet** fügt dem VmSS (Virtual Machine Scale Set) einen Geheimtipp hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-106">The **Add-AzVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="3f3e0-107">Der Geheimschlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="3f3e0-108">Weitere Informationen zum Schlüsseltresor finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="3f3e0-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="3f3e0-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="3f3e0-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="3f3e0-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) oder das [Set-AzKeyVaultSecret-Cmdlet.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="3f3e0-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="3f3e0-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f3e0-111">EXAMPLES</span></span>

### <span data-ttu-id="3f3e0-112">Beispiel 1: Hinzufügen eines Geheimtipps zum VMSS</span><span class="sxs-lookup"><span data-stu-id="3f3e0-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzVmssConfig
PS C:\> Add-AzVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="3f3e0-113">In diesem Beispiel wird dem VMSS ein Geheimtipp hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="3f3e0-114">Der erste Befehl verwendet das Get-AzKeyVault-Cmdlet, um einen Tresorgeheimnis aus dem Tresor namens ContosoVault zu erhalten, und speichert das Ergebnis in der Variablen namens $Vault.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-114">The first command uses the Get-AzKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="3f3e0-115">Der zweite Befehl verwendet das **Cmdlet New-AzVmssVaultCertificateConfig,** um eine Key Vault-Zertifikatkonfiguration mit der angegebenen Zertifikat-URL aus dem Zertifikatspeicher namens Zertifikate zu erstellen und die Ergebnisse in der Variablen namens $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-115">The second command uses the **New-AzVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="3f3e0-116">Der dritte Befehl verwendet das **Cmdlet New-AzVmssConfig** zum Erstellen eines VMSS-Konfigurationsobjekts und speichert das Ergebnis in der Variablen namens $VMSS.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-116">The third command uses the **New-AzVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="3f3e0-117">Der vierte Befehl fügt dem VMSS mithilfe des Tresorschlüssels mithilfe der Schlüsselressourcen-ID und des in den Variablen $Vault und $CertConfig gespeicherten Tresorzertifikats einen Geheimschlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="3f3e0-118">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="3f3e0-118">PARAMETERS</span></span>

### <span data-ttu-id="3f3e0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f3e0-119">-DefaultProfile</span></span>
<span data-ttu-id="3f3e0-120">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3f3e0-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="3f3e0-121">-SourceVaultId</span></span>
<span data-ttu-id="3f3e0-122">Gibt die Ressourcen-ID des Schlüsseltresor an, der die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="3f3e0-123">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="3f3e0-124">Dies bedeutet, dass Sie denselben Wert für den *Parameter SourceVaultId verwenden* können, wenn Sie mehrere Zertifikate aus demselben Schlüsseltresor hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="3f3e0-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="3f3e0-125">-VaultCertificate</span></span>
<span data-ttu-id="3f3e0-126">Gibt das Vault **Certificate-Objekt** an, das die Zertifikat-URL und den Zertifikatnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="3f3e0-127">Sie können das [Cmdlet New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-127">You can use the [New-AzVmssVaultCertificateConfig](./New-AzVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="3f3e0-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f3e0-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="3f3e0-129">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="3f3e0-130">Sie können das [Cmdlet New-AzVmssConfig](./New-AzVmssConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-130">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="3f3e0-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3f3e0-131">-Confirm</span></span>
<span data-ttu-id="3f3e0-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f3e0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f3e0-133">-WhatIf</span></span>
<span data-ttu-id="3f3e0-134">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3f3e0-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f3e0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f3e0-136">CommonParameters</span></span>
<span data-ttu-id="3f3e0-137">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f3e0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f3e0-138">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3f3e0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f3e0-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f3e0-139">INPUTS</span></span>

### <span data-ttu-id="3f3e0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f3e0-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="3f3e0-141">System.String</span><span class="sxs-lookup"><span data-stu-id="3f3e0-141">System.String</span></span>

### <span data-ttu-id="3f3e0-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span><span class="sxs-lookup"><span data-stu-id="3f3e0-142">Microsoft.Azure.Management.Compute.Models.VaultCertificate[]</span></span>

## <span data-ttu-id="3f3e0-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f3e0-143">OUTPUTS</span></span>

### <span data-ttu-id="3f3e0-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="3f3e0-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="3f3e0-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="3f3e0-145">NOTES</span></span>

## <span data-ttu-id="3f3e0-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="3f3e0-146">RELATED LINKS</span></span>

[<span data-ttu-id="3f3e0-147">New-AzVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="3f3e0-147">New-AzVmssVaultCertificateConfig</span></span>](./New-AzVmssVaultCertificateConfig.md)

[<span data-ttu-id="3f3e0-148">New-AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="3f3e0-148">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
