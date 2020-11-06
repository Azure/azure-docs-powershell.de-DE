---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: 304d64e2eaff4ae1488bdde12991d22834022e93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505542"
---
# <span data-ttu-id="4e65d-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4e65d-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="4e65d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4e65d-102">SYNOPSIS</span></span>
<span data-ttu-id="4e65d-103">Fügt dem angegebenen Batch Konto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="4e65d-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e65d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e65d-104">SYNTAX</span></span>

### <span data-ttu-id="4e65d-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="4e65d-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4e65d-106">RawData</span><span class="sxs-lookup"><span data-stu-id="4e65d-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <SecureString>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e65d-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4e65d-107">DESCRIPTION</span></span>
<span data-ttu-id="4e65d-108">Mit dem Cmdlet **New-AzureBatchCertificate** wird dem angegebenen Azure-Batch Konto ein Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e65d-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="4e65d-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4e65d-109">EXAMPLES</span></span>

### <span data-ttu-id="4e65d-110">Beispiel 1: Hinzufügen eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="4e65d-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="4e65d-111">Dieser Befehl fügt dem angegebenen Batch Konto ein Zertifikat mithilfe der Datei E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="4e65d-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="4e65d-112">Beispiel 2: Hinzufügen eines Zertifikats aus unformatierten Daten</span><span class="sxs-lookup"><span data-stu-id="4e65d-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="4e65d-113">Der erste Befehl liest die Daten aus der Datei mit dem Namen mycert. pfx in die $rawData Variable ein.</span><span class="sxs-lookup"><span data-stu-id="4e65d-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="4e65d-114">Mit dem zweiten Befehl wird dem angegebenen Stapelverarbeitungs Konto ein Zertifikat mithilfe der in $rawData gespeicherten Rohdaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="4e65d-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="4e65d-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="4e65d-115">PARAMETERS</span></span>

### <span data-ttu-id="4e65d-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="4e65d-116">-BatchContext</span></span>
<span data-ttu-id="4e65d-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e65d-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4e65d-118">Wenn Sie das Get-AzureRmBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e65d-118">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="4e65d-119">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4e65d-119">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="4e65d-120">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="4e65d-120">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="4e65d-121">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="4e65d-121">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e65d-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e65d-122">-DefaultProfile</span></span>
<span data-ttu-id="4e65d-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4e65d-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e65d-124">-FilePath</span><span class="sxs-lookup"><span data-stu-id="4e65d-124">-FilePath</span></span>
<span data-ttu-id="4e65d-125">Gibt den Pfad der Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="4e65d-125">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="4e65d-126">Die Zertifikatdatei muss entweder im CER-oder im PFX-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="4e65d-126">The certificate file must be in either .cer or .pfx format.</span></span>

```yaml
Type: String
Parameter Sets: File
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e65d-127">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="4e65d-127">-Password</span></span>
<span data-ttu-id="4e65d-128">Gibt das Kennwort für den Zugriff auf den privaten Zertifikatschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="4e65d-128">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="4e65d-129">Sie müssen diesen Parameter angeben, wenn Sie im PFX-Format ein Zertifikat angeben.</span><span class="sxs-lookup"><span data-stu-id="4e65d-129">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e65d-130">-RawData</span><span class="sxs-lookup"><span data-stu-id="4e65d-130">-RawData</span></span>
<span data-ttu-id="4e65d-131">Gibt die unformatierten Zertifikatdaten im CER-oder PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="4e65d-131">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

```yaml
Type: Byte[]
Parameter Sets: RawData
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4e65d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e65d-132">CommonParameters</span></span>
<span data-ttu-id="4e65d-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e65d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e65d-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e65d-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e65d-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4e65d-135">INPUTS</span></span>

### <span data-ttu-id="4e65d-136">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e65d-136">BatchAccountContext</span></span>
<span data-ttu-id="4e65d-137">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4e65d-137">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="4e65d-138">Byte []</span><span class="sxs-lookup"><span data-stu-id="4e65d-138">Byte[]</span></span>
<span data-ttu-id="4e65d-139">Der Parameter "rawData" akzeptiert den Wert vom Typ "Byte []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="4e65d-139">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="4e65d-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4e65d-140">OUTPUTS</span></span>

## <span data-ttu-id="4e65d-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="4e65d-141">NOTES</span></span>

## <span data-ttu-id="4e65d-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4e65d-142">RELATED LINKS</span></span>

[<span data-ttu-id="4e65d-143">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4e65d-143">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="4e65d-144">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="4e65d-144">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="4e65d-145">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="4e65d-145">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="4e65d-146">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4e65d-146">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


