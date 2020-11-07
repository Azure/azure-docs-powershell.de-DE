---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 656BE930-E778-40B0-8A75-BFE52DE386CE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsssecret
schema: 2.0.0
ms.openlocfilehash: 9c31442e1242114572540c23049f26715fc3099e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848936"
---
# <span data-ttu-id="84193-101">Add-AzureRmVmssSecret</span><span class="sxs-lookup"><span data-stu-id="84193-101">Add-AzureRmVmssSecret</span></span>

## <span data-ttu-id="84193-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="84193-102">SYNOPSIS</span></span>
<span data-ttu-id="84193-103">Fügt einen Schlüssel zu einem VMSS hinzu.</span><span class="sxs-lookup"><span data-stu-id="84193-103">Adds a secret to a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="84193-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="84193-104">SYNTAX</span></span>

```
Add-AzureRmVmssSecret [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-SourceVaultId] <String>]
 [[-VaultCertificate] <VaultCertificate[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84193-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="84193-105">DESCRIPTION</span></span>
<span data-ttu-id="84193-106">Das **Add-AzureRmVmssSecret-** Cmdlet fügt dem virtuellen Computer-Skalierungs Satz (VMSS) einen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="84193-106">The **Add-AzureRmVmssSecret** cmdlet adds a secret to the Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="84193-107">Der Schlüssel muss in einem Azure Key Vault gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="84193-107">The secret must be stored in an Azure Key Vault.</span></span>
<span data-ttu-id="84193-108">Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="84193-108">For more information relating to Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span></span> <span data-ttu-id="84193-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="84193-109">(https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="84193-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) ( https://msdn.microsoft.com/library/azure/dn868052.aspx) in der Microsoft Developer-Netzwerkbibliothek oder im Cmdlet " [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) ".</span><span class="sxs-lookup"><span data-stu-id="84193-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) (https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="84193-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="84193-111">EXAMPLES</span></span>

### <span data-ttu-id="84193-112">Beispiel 1: Hinzufügen eines Geheimnisses zum VMSS</span><span class="sxs-lookup"><span data-stu-id="84193-112">Example 1: Add a secret to the VMSS</span></span>
```
PS C:\> $Vault = Get-AzureRmKeyVault -VaultName "ContosoVault"
PS C:\> $CertConfig = New-AzureRmVmssVaultCertificateConfig -CertificateUrl "http://keyVaultName.vault.contoso.net/secrets/secretName/secretVersion" -CertificateStore "Certificates"
PS C:\> $VMSS = New-AzureRmVmssConfig
PS C:\> Add-AzureRmVmssSecret -VirtualMachineScaleSet $VMSS -SourceVaultId $Vault.ResourceId -VaultCertificate $CertConfig
```

<span data-ttu-id="84193-113">In diesem Beispiel wird der VMSS ein Schlüssel hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="84193-113">This example adds a secret to the VMSS.</span></span>
<span data-ttu-id="84193-114">Der erste Befehl verwendet das Get-AzureRmKeyVault-Cmdlet, um einen Vault Secret aus dem Vault mit dem Namen ContosoVault abzurufen, und speichert das Ergebnis in der Variablen mit dem Namen $Vault.</span><span class="sxs-lookup"><span data-stu-id="84193-114">The first command uses the Get-AzureRmKeyVault cmdlet to get a vault secret from the vault named ContosoVault and stores the result in the variable named $Vault.</span></span>
<span data-ttu-id="84193-115">Der zweite Befehl verwendet das Cmdlet **New-AzureRmVmssVaultCertificateConfig** zum Erstellen einer Schlüsseldepot-Zertifikatkonfiguration unter Verwendung der angegebenen Zertifikat-URL aus dem Zertifikatspeicher mit dem Namen Zertifikate und speichert die Ergebnisse in der Variablen mit dem Namen $CertConfig.</span><span class="sxs-lookup"><span data-stu-id="84193-115">The second command uses the **New-AzureRmVmssVaultCertificateConfig** cmdlet to create a Key Vault certificate configuration using the specified certificate URL from the certificate store named Certificates and stores the results in the variable named $CertConfig.</span></span>
<span data-ttu-id="84193-116">Der dritte Befehl verwendet das Cmdlet **New-AzureRmVmssConfig** , um ein VMSS-Konfigurationsobjekt zu erstellen und das Ergebnis in der Variablen mit dem Namen $VMSS zu speichern.</span><span class="sxs-lookup"><span data-stu-id="84193-116">The third command uses the **New-AzureRmVmssConfig** cmdlet to create a VMSS configuration object and stores the result in the variable named $VMSS.</span></span>
<span data-ttu-id="84193-117">Der vierte Befehl fügt dem VMSS mithilfe der Schlüsselressourcen-ID und des Vault-Zertifikats, das in den $Vault-und $CertConfig Variablen gespeichert ist, einen geheimen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="84193-117">The fourth command adds a secret to the VMSS using the vault secret using the key resource ID and the vault certificate stored in the $Vault and $CertConfig variables.</span></span>

## <span data-ttu-id="84193-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="84193-118">PARAMETERS</span></span>

### <span data-ttu-id="84193-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84193-119">-DefaultProfile</span></span>
<span data-ttu-id="84193-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="84193-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="84193-121">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="84193-121">-SourceVaultId</span></span>
<span data-ttu-id="84193-122">Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="84193-122">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="84193-123">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="84193-123">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="84193-124">Das bedeutet, dass Sie für den *SourceVaultId* -Parameter denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsselspeicher hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84193-124">This means that you can use the same value for the *SourceVaultId* parameter when you add multiple certificates from the same Key Vault.</span></span>

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

### <span data-ttu-id="84193-125">-VaultCertificate</span><span class="sxs-lookup"><span data-stu-id="84193-125">-VaultCertificate</span></span>
<span data-ttu-id="84193-126">Gibt das Vault **Certificate** -Objekt an, das die Zertifikat-URL und den Zertifikatsnamen enthält.</span><span class="sxs-lookup"><span data-stu-id="84193-126">Specifies the Vault **Certificate** object that contains the certificate URL and certificate name.</span></span>
<span data-ttu-id="84193-127">Sie können das Cmdlet [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84193-127">You can use the [New-AzureRmVmssVaultCertificateConfig](./New-AzureRmVmssVaultCertificateConfig.md) cmdlet to create this object.</span></span>

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

### <span data-ttu-id="84193-128">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="84193-128">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="84193-129">Gibt das VMSS-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="84193-129">Specifies the VMSS object.</span></span>
<span data-ttu-id="84193-130">Sie können das Cmdlet [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) verwenden, um dieses Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="84193-130">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create this object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84193-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="84193-131">-Confirm</span></span>
<span data-ttu-id="84193-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="84193-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="84193-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84193-133">-WhatIf</span></span>
<span data-ttu-id="84193-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="84193-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84193-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="84193-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="84193-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84193-136">CommonParameters</span></span>
<span data-ttu-id="84193-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84193-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84193-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84193-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84193-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="84193-139">INPUTS</span></span>

### <span data-ttu-id="84193-140">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="84193-140">VirtualMachineScaleSet</span></span>
<span data-ttu-id="84193-141">Der Parameter "VirtualMachineScaleSet" akzeptiert den Wert vom Typ "VirtualMachineScaleSet" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="84193-141">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="84193-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="84193-142">OUTPUTS</span></span>

### <span data-ttu-id="84193-143">Keine</span><span class="sxs-lookup"><span data-stu-id="84193-143">None</span></span>
<span data-ttu-id="84193-144">Dieses Cmdlet generiert keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="84193-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="84193-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="84193-145">NOTES</span></span>

## <span data-ttu-id="84193-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="84193-146">RELATED LINKS</span></span>

[<span data-ttu-id="84193-147">Neu – AzureRmVmssVaultCertificateConfig</span><span class="sxs-lookup"><span data-stu-id="84193-147">New-AzureRmVmssVaultCertificateConfig</span></span>](./New-AzureRmVmssVaultCertificateConfig.md)

[<span data-ttu-id="84193-148">Neu – AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="84193-148">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
