---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: 240da78c14b681b334d0793bfc15b2af4d97b5f3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "94007466"
---
# <span data-ttu-id="7fad6-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7fad6-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="7fad6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7fad6-102">SYNOPSIS</span></span>
<span data-ttu-id="7fad6-103">Fügt dem angegebenen Batch Konto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="7fad6-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="7fad6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7fad6-104">SYNTAX</span></span>

### <span data-ttu-id="7fad6-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="7fad6-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7fad6-106">RawData</span><span class="sxs-lookup"><span data-stu-id="7fad6-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fad6-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7fad6-107">DESCRIPTION</span></span>
<span data-ttu-id="7fad6-108">Mit dem Cmdlet **New-AzBatchCertificate** wird dem angegebenen Azure-Batch Konto ein Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fad6-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="7fad6-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7fad6-109">EXAMPLES</span></span>

### <span data-ttu-id="7fad6-110">Beispiel 1: Hinzufügen eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="7fad6-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="7fad6-111">Dieser Befehl fügt dem angegebenen Batch Konto ein Zertifikat mithilfe der Datei E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="7fad6-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="7fad6-112">Beispiel 2: Hinzufügen eines Zertifikats aus unformatierten Daten</span><span class="sxs-lookup"><span data-stu-id="7fad6-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="7fad6-113">Der erste Befehl liest die Daten aus der Datei mit dem Namen mycert. pfx in die $rawData Variable ein.</span><span class="sxs-lookup"><span data-stu-id="7fad6-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="7fad6-114">Mit dem zweiten Befehl wird dem angegebenen Stapelverarbeitungs Konto ein Zertifikat mithilfe der in $rawData gespeicherten Rohdaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fad6-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="7fad6-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fad6-115">PARAMETERS</span></span>

### <span data-ttu-id="7fad6-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="7fad6-116">-BatchContext</span></span>
<span data-ttu-id="7fad6-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fad6-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7fad6-118">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fad6-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7fad6-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKey-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7fad6-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7fad6-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="7fad6-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7fad6-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="7fad6-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7fad6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fad6-122">-DefaultProfile</span></span>
<span data-ttu-id="7fad6-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7fad6-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fad6-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="7fad6-124">-FilePath</span></span>
<span data-ttu-id="7fad6-125">Gibt den Pfad der Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="7fad6-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="7fad6-126">Die Zertifikatdatei muss entweder im CER-oder im PFX-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="7fad6-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="7fad6-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="7fad6-127">-Password</span></span>
<span data-ttu-id="7fad6-128">Gibt das Kennwort für den Zugriff auf den privaten Zertifikatschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="7fad6-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="7fad6-129">Sie müssen diesen Parameter angeben, wenn Sie im PFX-Format ein Zertifikat angeben.</span><span class="sxs-lookup"><span data-stu-id="7fad6-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="7fad6-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="7fad6-130">-RawData</span></span>
<span data-ttu-id="7fad6-131">Gibt die unformatierten Zertifikatdaten im CER-oder PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="7fad6-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="7fad6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fad6-132">CommonParameters</span></span>
<span data-ttu-id="7fad6-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fad6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fad6-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fad6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fad6-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7fad6-135">INPUTS</span></span>

### <span data-ttu-id="7fad6-136">System. Byte []</span><span class="sxs-lookup"><span data-stu-id="7fad6-136">System.Byte[]</span></span>

### <span data-ttu-id="7fad6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7fad6-137">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="7fad6-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7fad6-138">OUTPUTS</span></span>

### <span data-ttu-id="7fad6-139">System. void</span><span class="sxs-lookup"><span data-stu-id="7fad6-139">System.Void</span></span>

## <span data-ttu-id="7fad6-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="7fad6-140">NOTES</span></span>

## <span data-ttu-id="7fad6-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7fad6-141">RELATED LINKS</span></span>

[<span data-ttu-id="7fad6-142">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7fad6-142">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="7fad6-143">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="7fad6-143">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="7fad6-144">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="7fad6-144">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="7fad6-145">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="7fad6-145">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


