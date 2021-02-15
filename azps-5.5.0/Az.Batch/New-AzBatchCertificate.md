---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchCertificate.md
ms.openlocfilehash: b7b3dae97e5af4b7d31edabb215ef25a32be6caf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164292"
---
# <span data-ttu-id="85202-101">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="85202-101">New-AzBatchCertificate</span></span>

## <span data-ttu-id="85202-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85202-102">SYNOPSIS</span></span>
<span data-ttu-id="85202-103">Fügt dem angegebenen Batchkonto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="85202-103">Adds a certificate to the specified Batch account.</span></span>

## <span data-ttu-id="85202-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="85202-104">SYNTAX</span></span>

### <span data-ttu-id="85202-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="85202-105">File (Default)</span></span>
```
New-AzBatchCertificate [-FilePath] <String> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="85202-106">RawData</span><span class="sxs-lookup"><span data-stu-id="85202-106">RawData</span></span>
```
New-AzBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] [-Kind <PSCertificateKind>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85202-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85202-107">DESCRIPTION</span></span>
<span data-ttu-id="85202-108">Das **Cmdlet "New-AzBatchCertificate"** fügt dem angegebenen Azure -Batchkonto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="85202-108">The **New-AzBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="85202-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="85202-109">EXAMPLES</span></span>

### <span data-ttu-id="85202-110">Beispiel 1: Hinzufügen eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="85202-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="85202-111">Dieser Befehl fügt dem angegebenen Batchkonto mithilfe der Datei "E:\Certificates\MyCert.cer" ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="85202-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="85202-112">Beispiel 2: Hinzufügen eines Zertifikats aus Rohdaten</span><span class="sxs-lookup"><span data-stu-id="85202-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="85202-113">Der erste Befehl liest die Daten aus der Datei "MyCert.pfx" in die $RawData Variable.</span><span class="sxs-lookup"><span data-stu-id="85202-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>
<span data-ttu-id="85202-114">Der zweite Befehl fügt dem angegebenen Batchkonto ein Zertifikat hinzu und verwendet dazu die rohen Daten, die in $RawData.</span><span class="sxs-lookup"><span data-stu-id="85202-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="85202-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85202-115">PARAMETERS</span></span>

### <span data-ttu-id="85202-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="85202-116">-BatchContext</span></span>
<span data-ttu-id="85202-117">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="85202-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="85202-118">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="85202-118">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="85202-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="85202-119">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="85202-120">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="85202-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="85202-121">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="85202-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="85202-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85202-122">-DefaultProfile</span></span>
<span data-ttu-id="85202-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85202-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="85202-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="85202-124">-FilePath</span></span>
<span data-ttu-id="85202-125">Gibt den Pfad der Zertifikatdatei an.</span><span class="sxs-lookup"><span data-stu-id="85202-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="85202-126">Die Zertifikatdatei muss im CER- oder im PFX-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="85202-126">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="85202-127">-Kind</span><span class="sxs-lookup"><span data-stu-id="85202-127">-Kind</span></span>
<span data-ttu-id="85202-128">Die Art des zu erstellende Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="85202-128">The kind of certificate to create.</span></span> <span data-ttu-id="85202-129">Ist dies nicht angegeben, wird davon ausgegangen, dass alle Zertifikate ohne Kennwort CER und alle Zertifikate mit Kennwort PFX sind.</span><span class="sxs-lookup"><span data-stu-id="85202-129">If this is not specified, it is assumed that all certificates without a password are CER and all certificates with password are PFX.</span></span>

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

### <span data-ttu-id="85202-130">-Password</span><span class="sxs-lookup"><span data-stu-id="85202-130">-Password</span></span>
<span data-ttu-id="85202-131">Gibt das Kennwort für den Zugriff auf den privaten Zertifikatschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="85202-131">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="85202-132">Sie müssen diesen Parameter angeben, wenn Sie ein Zertifikat im .pfx-Format angeben.</span><span class="sxs-lookup"><span data-stu-id="85202-132">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

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

### <span data-ttu-id="85202-133">-RawData</span><span class="sxs-lookup"><span data-stu-id="85202-133">-RawData</span></span>
<span data-ttu-id="85202-134">Gibt die Rohzertifikatdaten im CER- oder im PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="85202-134">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="85202-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85202-135">CommonParameters</span></span>
<span data-ttu-id="85202-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85202-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85202-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="85202-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85202-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="85202-138">INPUTS</span></span>

### <span data-ttu-id="85202-139">System.Byte[]</span><span class="sxs-lookup"><span data-stu-id="85202-139">System.Byte[]</span></span>

### <span data-ttu-id="85202-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="85202-140">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="85202-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="85202-141">OUTPUTS</span></span>

### <span data-ttu-id="85202-142">System.Void</span><span class="sxs-lookup"><span data-stu-id="85202-142">System.Void</span></span>

## <span data-ttu-id="85202-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="85202-143">NOTES</span></span>

## <span data-ttu-id="85202-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="85202-144">RELATED LINKS</span></span>

[<span data-ttu-id="85202-145">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="85202-145">Get-AzBatchCertificate</span></span>](./Get-AzBatchCertificate.md)

[<span data-ttu-id="85202-146">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="85202-146">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="85202-147">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="85202-147">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="85202-148">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="85202-148">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
