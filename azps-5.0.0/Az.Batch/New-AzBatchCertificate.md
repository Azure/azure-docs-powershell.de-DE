---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176627"
---
# <span data-ttu-id="32efa-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32efa-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="32efa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32efa-102">SYNOPSIS</span></span>
<span data-ttu-id="32efa-103">Fügt dem angegebenen Batch Konto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="32efa-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="32efa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32efa-104">SYNTAX</span></span>

### <span data-ttu-id="32efa-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="32efa-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="32efa-106">RawData</span><span class="sxs-lookup"><span data-stu-id="32efa-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32efa-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32efa-107">DESCRIPTION</span></span>
<span data-ttu-id="32efa-108">Mit dem Cmdlet **New-AzBatchCertificate** wird dem angegebenen Azure-Batch Konto ein Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="32efa-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="32efa-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32efa-109">EXAMPLES</span></span>

### <span data-ttu-id="32efa-110">Beispiel 1: Hinzufügen eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="32efa-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="32efa-111">Dieser Befehl fügt dem angegebenen Batch Konto ein Zertifikat mithilfe der Datei E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="32efa-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="32efa-112">Beispiel 2: Hinzufügen eines Zertifikats aus unformatierten Daten</span><span class="sxs-lookup"><span data-stu-id="32efa-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="32efa-113">Der erste Befehl liest die Daten aus der Datei mit dem Namen mycert. pfx in die $rawData Variable ein.</span><span class="sxs-lookup"><span data-stu-id="32efa-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="32efa-114">Mit dem zweiten Befehl wird dem angegebenen Stapelverarbeitungs Konto ein Zertifikat mithilfe der in $rawData gespeicherten Rohdaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="32efa-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="32efa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="32efa-115">PARAMETERS</span></span>

### <span data-ttu-id="32efa-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="32efa-116">-BatchContext</span></span>
<span data-ttu-id="32efa-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="32efa-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="32efa-118">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="32efa-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="32efa-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="32efa-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="32efa-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="32efa-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="32efa-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="32efa-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32efa-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32efa-122">-DefaultProfile</span></span>
<span data-ttu-id="32efa-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32efa-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32efa-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="32efa-124">-FilePath</span></span>
<span data-ttu-id="32efa-125">Gibt den Pfad der Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="32efa-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="32efa-126">Die Zertifikatdatei muss entweder im CER-oder im PFX-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="32efa-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32efa-127">-Art</span><span class="sxs-lookup"><span data-stu-id="32efa-127">-Kind</span></span>
<span data-ttu-id="32efa-128">Die Art des zu erstellendes Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="32efa-128">The kind of certificate to create.</span></span> <span data-ttu-id="32efa-129">Wenn dies nicht angegeben ist, wird davon ausgegangen, dass alle Zertifikate ohne Kennwort CER sind und alle Zertifikate mit Kennwort PFX sind.</span><span class="sxs-lookup"><span data-stu-id="32efa-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateKind
Parameter Sets: (All)
Aliases:
Accepted values: Cer, Pfx

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32efa-130">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="32efa-130">-Password</span></span>
<span data-ttu-id="32efa-131">Gibt das Kennwort für den Zugriff auf den privaten Zertifikatschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="32efa-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="32efa-132">Sie müssen diesen Parameter angeben, wenn Sie im PFX-Format ein Zertifikat angeben.</span><span class="sxs-lookup"><span data-stu-id="32efa-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32efa-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="32efa-133">-RawData</span></span>
<span data-ttu-id="32efa-134">Gibt die unformatierten Zertifikatdaten im CER-oder PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="32efa-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: System.Byte[]
Parameter Sets: RawData
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32efa-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32efa-135">CommonParameters</span></span>
<span data-ttu-id="32efa-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32efa-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32efa-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32efa-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32efa-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32efa-138">INPUTS</span></span>

### <span data-ttu-id="32efa-139">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="32efa-139">System.Byte[]</span></span>

### <span data-ttu-id="32efa-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="32efa-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="32efa-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32efa-141">OUTPUTS</span></span>

### <span data-ttu-id="32efa-142">System. void</span><span class="sxs-lookup"><span data-stu-id="32efa-142">System.Void</span></span>

## <span data-ttu-id="32efa-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="32efa-143">NOTES</span></span>

## <span data-ttu-id="32efa-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32efa-144">RELATED LINKS</span></span>

[<span data-ttu-id="32efa-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32efa-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="32efa-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="32efa-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="32efa-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="32efa-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="32efa-148">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="32efa-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
