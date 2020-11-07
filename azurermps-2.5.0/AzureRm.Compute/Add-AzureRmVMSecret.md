---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmsecret
schema: 2.0.0
ms.openlocfilehash: 70342620aeab42ba7236091e8aacc32ea44354ef
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850172"
---
# <span data-ttu-id="5cf62-101">Add-AzureRmVMSecret</span><span class="sxs-lookup"><span data-stu-id="5cf62-101">Add-AzureRmVMSecret</span></span>

## <span data-ttu-id="5cf62-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cf62-102">SYNOPSIS</span></span>
<span data-ttu-id="5cf62-103">Fügt einen geheimen Schlüssel zu einem virtuellen Computer hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-103">Adds a secret to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cf62-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cf62-104">SYNTAX</span></span>

```
Add-AzureRmVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5cf62-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cf62-105">DESCRIPTION</span></span>
<span data-ttu-id="5cf62-106">Das Cmdlet **Add-AzureRmVMSecret** fügt einem virtuellen Computer einen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-106">The **Add-AzureRmVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="5cf62-107">Mit diesem Wert können Sie dem virtuellen Computer ein Zertifikat hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="5cf62-108">Das Kennwort muss in einem schlüsseltresor gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="5cf62-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="5cf62-109">Weitere Informationen zu Key Vault finden Sie unter [Was ist Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span><span class="sxs-lookup"><span data-stu-id="5cf62-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="5cf62-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in der Microsoft Developer Network Library oder im Cmdlet " [AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) ".</span><span class="sxs-lookup"><span data-stu-id="5cf62-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](https://msdn.microsoft.com/library/azure/dn868052.aspx) in the Microsoft Developer Network library or the [Set-AzureKeyVaultSecret](/powershell/module/azurerm.keyvault/set-azurekeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="5cf62-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cf62-111">EXAMPLES</span></span>

### <span data-ttu-id="5cf62-112">Beispiel 1: Hinzufügen eines Geheimnisses zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="5cf62-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzureRmVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="5cf62-113">Der erste Befehl erstellt ein Objekt eines virtuellen Computers und speichert es dann in der $VirtualMachine-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="5cf62-114">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-114">The command assigns a name and size to the virtual machine.</span></span>

<span data-ttu-id="5cf62-115">Der zweite Befehl erstellt ein Anmeldeinformationsobjekt mithilfe des Get-Credential-Cmdlets und speichert dann das Ergebnis in der $Credential-Variablen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="5cf62-116">Der Befehl fordert Sie auf, einen Benutzernamen und ein Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="5cf62-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="5cf62-117">Wenn Sie weitere Informationen wünschen, geben Sie `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="5cf62-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="5cf62-118">Der dritte Befehl verwendet das Cmdlet " **Satz-AzureRmVMOperatingSystem** ", um den in $VirtualMachine gespeicherten virtuellen Computer zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5cf62-118">The third command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="5cf62-119">Der vierte Befehl weist der $SourceVaultId Variablen eine Quell Tresor-ID zur späteren Verwendung zu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="5cf62-120">Der Befehl geht davon aus, dass die $SubscriptionId Variable über einen geeigneten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="5cf62-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>

<span data-ttu-id="5cf62-121">Der fünfte Befehl weist der $CertificateStore 01-Variablen einen Wert für die spätere Verwendung zu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>

<span data-ttu-id="5cf62-122">Der sechste Befehl weist eine URL für einen Zertifikatspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-122">The sixth command assigns a URL for a certificate store.</span></span>

<span data-ttu-id="5cf62-123">Der siebte Befehl fügt dem virtuellen Computer, der in $VirtualMachine gespeichert ist, einen Schlüssel hinzu.</span><span class="sxs-lookup"><span data-stu-id="5cf62-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="5cf62-124">Der SourceVaultId-Parameter gibt den schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="5cf62-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="5cf62-125">Der Befehl gibt den Namen des Zertifikatspeichers und die URL des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="5cf62-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="5cf62-126">Sie können das **Add-AzureRmVMSecret** wiederholt ausführen, um Geheimnisse für andere Zertifikate hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-126">You can run the **Add-AzureRmVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="5cf62-127">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cf62-127">PARAMETERS</span></span>

### <span data-ttu-id="5cf62-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="5cf62-128">-CertificateStore</span></span>
<span data-ttu-id="5cf62-129">Gibt den Namen eines Zertifikatspeichers auf dem virtuellen Computer an, auf dem das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf62-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="5cf62-130">Mit diesem Cmdlet wird das Zertifikat dem Store hinzugefügt, das dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="5cf62-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="5cf62-131">Sie können diesen Parameter nur für virtuelle Computer angeben, auf denen das Windows-Betriebssystem ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cf62-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf62-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="5cf62-132">-CertificateUrl</span></span>
<span data-ttu-id="5cf62-133">Gibt die URL an, die auf ein schlüsseltresor-Kennwort verweist, das ein Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="5cf62-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>

<span data-ttu-id="5cf62-134">Bei dem Zertifikat handelt es sich um die Base64-Codierung des folgenden JSON-Objekts (JavaScript Object Notation), das in UTF-8 codiert ist:</span><span class="sxs-lookup"><span data-stu-id="5cf62-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8:</span></span>

<span data-ttu-id="5cf62-135">{"Data": " \<Base64-encoded-file\> ", "Datentyp": " \<file-format\> ", "Kennwort": "" \<pfx-file-password\> }</span><span class="sxs-lookup"><span data-stu-id="5cf62-135">{ "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" }</span></span>


<span data-ttu-id="5cf62-136">Derzeit akzeptiert DataType nur PFX-Dateien.</span><span class="sxs-lookup"><span data-stu-id="5cf62-136">Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf62-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cf62-137">-DefaultProfile</span></span>
<span data-ttu-id="5cf62-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cf62-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5cf62-139">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="5cf62-139">-SourceVaultId</span></span>
<span data-ttu-id="5cf62-140">Gibt die Ressourcen-ID des Schlüsseldepots an, das die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="5cf62-140">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="5cf62-141">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="5cf62-141">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="5cf62-142">Das bedeutet, dass Sie für *SourceVaultId* denselben Wert verwenden können, wenn Sie mehrere Zertifikate aus demselben schlüsseltresor hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-142">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf62-143">-VM</span><span class="sxs-lookup"><span data-stu-id="5cf62-143">-VM</span></span>
<span data-ttu-id="5cf62-144">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5cf62-144">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="5cf62-145">Verwenden Sie das Cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) , um ein Objekt eines virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5cf62-145">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="5cf62-146">Sie können das Cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) verwenden, um ein Objekt eines virtuellen Computers zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="5cf62-146">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cf62-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cf62-147">CommonParameters</span></span>
<span data-ttu-id="5cf62-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cf62-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cf62-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cf62-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cf62-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cf62-150">INPUTS</span></span>

### <span data-ttu-id="5cf62-151">PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5cf62-151">PSVirtualMachine</span></span>
<span data-ttu-id="5cf62-152">Der Parameter "VM" akzeptiert den Wert vom Typ "PSVirtualMachine" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="5cf62-152">Parameter 'VM' accepts value of type 'PSVirtualMachine' from the pipeline</span></span>

## <span data-ttu-id="5cf62-153">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cf62-153">OUTPUTS</span></span>

### <span data-ttu-id="5cf62-154">Microsoft. Azure. Commands. Compute. Models. PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="5cf62-154">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="5cf62-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cf62-155">NOTES</span></span>

## <span data-ttu-id="5cf62-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cf62-156">RELATED LINKS</span></span>

[<span data-ttu-id="5cf62-157">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5cf62-157">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5cf62-158">Neu – AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="5cf62-158">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)

[<span data-ttu-id="5cf62-159">Satz-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="5cf62-159">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)
