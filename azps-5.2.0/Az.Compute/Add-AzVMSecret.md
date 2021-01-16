---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: 059aedf6ca3b5c229092f9ce536d23a8fc602830
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98305851"
---
# <span data-ttu-id="c41a2-101">Add-AzVMSecret</span><span class="sxs-lookup"><span data-stu-id="c41a2-101">Add-AzVMSecret</span></span>

## <span data-ttu-id="c41a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c41a2-102">SYNOPSIS</span></span>
<span data-ttu-id="c41a2-103">Fügt einem virtuellen Computer ein Geheimnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-103">Adds a secret to a virtual machine.</span></span>

## <span data-ttu-id="c41a2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c41a2-104">SYNTAX</span></span>

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c41a2-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c41a2-105">DESCRIPTION</span></span>
<span data-ttu-id="c41a2-106">Das **Cmdlet "Add-AzVMSecret"** fügt einem virtuellen Computer ein Geheimnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-106">The **Add-AzVMSecret** cmdlet adds a secret to a virtual machine.</span></span>
<span data-ttu-id="c41a2-107">Mit diesem Wert können Sie dem virtuellen Computer ein Zertifikat hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c41a2-107">This value lets you add a certificate to the virtual machine.</span></span>
<span data-ttu-id="c41a2-108">Das Geheimnis muss in einem Schlüsseltresor gespeichert sein.</span><span class="sxs-lookup"><span data-stu-id="c41a2-108">The secret must be stored in a Key Vault.</span></span>
<span data-ttu-id="c41a2-109">Weitere Informationen zum Schlüsseltresor finden Sie unter ["Was ist der Azure Key Vault?".](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)</span><span class="sxs-lookup"><span data-stu-id="c41a2-109">For more information about Key Vault, see [What is Azure Key Vault?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/).</span></span>
<span data-ttu-id="c41a2-110">Weitere Informationen zu den Cmdlets finden Sie unter [Azure Key Vault-Cmdlets](/powershell/module/az.keyvault) oder im [Set-AzKeyVaultSecret-Cmdlet.](/powershell/module/az.keyvault/set-azkeyvaultsecret)</span><span class="sxs-lookup"><span data-stu-id="c41a2-110">For more information about the cmdlets, see [Azure Key Vault Cmdlets](/powershell/module/az.keyvault) or the [Set-AzKeyVaultSecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet.</span></span>

## <span data-ttu-id="c41a2-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c41a2-111">EXAMPLES</span></span>

### <span data-ttu-id="c41a2-112">Beispiel 1: Hinzufügen eines Geheimen zu einem virtuellen Computer</span><span class="sxs-lookup"><span data-stu-id="c41a2-112">Example 1: Add a secret to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

<span data-ttu-id="c41a2-113">Der erste Befehl erstellt ein Objekt des virtuellen Computers und speichert es dann in der $VirtualMachine Variable.</span><span class="sxs-lookup"><span data-stu-id="c41a2-113">The first command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c41a2-114">Der Befehl weist dem virtuellen Computer einen Namen und eine Größe zu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-114">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="c41a2-115">Der zweite Befehl erstellt mithilfe des Cmdlets Get-Credential Anmeldeinformationen und speichert das Ergebnis dann in der $Credential Variable.</span><span class="sxs-lookup"><span data-stu-id="c41a2-115">The second command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="c41a2-116">Der Befehl fordert Sie zur Eingabe eines Benutzernamens und Kennworts auf.</span><span class="sxs-lookup"><span data-stu-id="c41a2-116">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="c41a2-117">Weitere Informationen erhalten Sie, wenn Sie " `Get-Help Get-Credential` eingeben" aus.</span><span class="sxs-lookup"><span data-stu-id="c41a2-117">For more information, type `Get-Help Get-Credential`.</span></span>
<span data-ttu-id="c41a2-118">Der dritte Befehl verwendet das **Cmdlet "Set-AzVMOperatingSystem",** um den virtuellen Computer zu konfigurieren, der in $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c41a2-118">The third command uses the **Set-AzVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c41a2-119">Der vierte Befehl weist der $SourceVaultId A0 eine Quelltresor-ID zur späteren Verwendung zu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-119">The fourth command assigns a source vault ID to the $SourceVaultId variable for later use.</span></span>
<span data-ttu-id="c41a2-120">Bei dem Befehl wird davon ausgegangen, $SubscriptionId die Variable über einen geeigneten Wert verfügt.</span><span class="sxs-lookup"><span data-stu-id="c41a2-120">The command assumes that the $SubscriptionId variable has an appropriate value.</span></span>
<span data-ttu-id="c41a2-121">Der fünfte Befehl weist der Variablen $CertificateStore 01 einen Wert zur späteren Verwendung zu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-121">The fifth command assigns a value to the $CertificateStore01 variable for later use.</span></span>
<span data-ttu-id="c41a2-122">Der sechste Befehl weist eine URL für einen Zertifikatspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-122">The sixth command assigns a URL for a certificate store.</span></span>
<span data-ttu-id="c41a2-123">Der siebte Befehl fügt dem virtuellen Computer, der in der Datei gespeichert ist, $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="c41a2-123">The seventh command adds a secret to the virtual machine stored in $VirtualMachine.</span></span>
<span data-ttu-id="c41a2-124">Der Parameter "SourceVaultId" gibt den Schlüsseltresor an.</span><span class="sxs-lookup"><span data-stu-id="c41a2-124">The SourceVaultId parameter specifies the Key Vault.</span></span>
<span data-ttu-id="c41a2-125">Der Befehl gibt den Namen des Zertifikatspeichers und die URL des Zertifikats an.</span><span class="sxs-lookup"><span data-stu-id="c41a2-125">The command specifies the name of the certificate store and the URL of the certificate.</span></span>
<span data-ttu-id="c41a2-126">Sie können **Add-AzVMSecret** wiederholt ausführen, um geheime Daten für andere Zertifikate hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="c41a2-126">You can run the **Add-AzVMSecret** repeatedly to add secrets for other certificates.</span></span>

## <span data-ttu-id="c41a2-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c41a2-127">PARAMETERS</span></span>

### <span data-ttu-id="c41a2-128">-CertificateStore</span><span class="sxs-lookup"><span data-stu-id="c41a2-128">-CertificateStore</span></span>
<span data-ttu-id="c41a2-129">Gibt den Namen eines Zertifikatspeichers auf dem virtuellen Computer an, auf dem das Betriebssystem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c41a2-129">Specifies the name of a certificate store on the virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="c41a2-130">Dieses Cmdlet fügt dem speicher, den dieser Parameter angibt, das Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="c41a2-130">This cmdlet adds the certificate to the store that this parameter specifies.</span></span>
<span data-ttu-id="c41a2-131">Sie können diesen Parameter nur für virtuelle Computer angeben, auf der das Betriebssystem Windows ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c41a2-131">You can only specify this parameter for virtual machines that run the Windows operating system.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a2-132">-CertificateUrl</span><span class="sxs-lookup"><span data-stu-id="c41a2-132">-CertificateUrl</span></span>
<span data-ttu-id="c41a2-133">Gibt die URL an, die auf einen geheimen Schlüsseltresor verweist, der ein Zertifikat enthält.</span><span class="sxs-lookup"><span data-stu-id="c41a2-133">Specifies the URL that points to a Key Vault secret which contains a certificate.</span></span>
<span data-ttu-id="c41a2-134">Das Zertifikat ist die Base64-Codierung des folgenden JavaScript Object Notation (JSON)-Objekts, das in UTF-8 codiert ist: { "data": " \<Base64-encoded-file\> ", "dataType": " \<file-format\> ", "password": " " } Derzeit akzeptiert dataType nur \<pfx-file-password\> PFX-Dateien.</span><span class="sxs-lookup"><span data-stu-id="c41a2-134">The certificate is the Base64 encoding of the following JavaScript Object Notation (JSON) object, which is encoded in UTF-8: { "data": "\<Base64-encoded-file\>", "dataType": "\<file-format\>", "password": "\<pfx-file-password\>" } Currently, dataType accepts only .pfx files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a2-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c41a2-135">-DefaultProfile</span></span>
<span data-ttu-id="c41a2-136">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c41a2-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c41a2-137">-SourceVaultId</span><span class="sxs-lookup"><span data-stu-id="c41a2-137">-SourceVaultId</span></span>
<span data-ttu-id="c41a2-138">Gibt die Ressourcen-ID des Schlüsseltresor an, der die Zertifikate enthält, die Sie dem virtuellen Computer hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="c41a2-138">Specifies the resource ID of the Key Vault that contains the certificates that you can add to the virtual machine.</span></span>
<span data-ttu-id="c41a2-139">Dieser Wert fungiert auch als Schlüssel zum Hinzufügen mehrerer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="c41a2-139">This value also acts as the key for adding multiple certificates.</span></span>
<span data-ttu-id="c41a2-140">Dies bedeutet, dass Sie denselben Wert für *"SourceVaultId"* verwenden können, wenn Sie mehrere Zertifikate aus demselben Schlüsseltresor hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c41a2-140">This means that you can use the same value for *SourceVaultId* when you add multiple certificates from the same Key Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a2-141">-VM</span><span class="sxs-lookup"><span data-stu-id="c41a2-141">-VM</span></span>
<span data-ttu-id="c41a2-142">Gibt das Objekt des virtuellen Computers an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="c41a2-142">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="c41a2-143">Verwenden Sie das [Get-AzVM-Cmdlet,](./Get-AzVM.md) um ein Objekt des virtuellen Computers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="c41a2-143">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="c41a2-144">Sie können das [Cmdlet "New-AzVMConfig"](./New-AzVMConfig.md) verwenden, um ein Objekt für einen virtuellen Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c41a2-144">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c41a2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c41a2-145">CommonParameters</span></span>
<span data-ttu-id="c41a2-146">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c41a2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c41a2-147">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c41a2-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c41a2-148">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c41a2-148">INPUTS</span></span>

### <span data-ttu-id="c41a2-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c41a2-149">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c41a2-150">System.String</span><span class="sxs-lookup"><span data-stu-id="c41a2-150">System.String</span></span>

## <span data-ttu-id="c41a2-151">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c41a2-151">OUTPUTS</span></span>

### <span data-ttu-id="c41a2-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="c41a2-152">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c41a2-153">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c41a2-153">NOTES</span></span>

## <span data-ttu-id="c41a2-154">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c41a2-154">RELATED LINKS</span></span>

[<span data-ttu-id="c41a2-155">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c41a2-155">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c41a2-156">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c41a2-156">New-AzVMConfig</span></span>](./New-AzVMConfig.md)

[<span data-ttu-id="c41a2-157">Set-AzVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="c41a2-157">Set-AzVMOperatingSystem</span></span>](./Set-AzVMOperatingSystem.md)
