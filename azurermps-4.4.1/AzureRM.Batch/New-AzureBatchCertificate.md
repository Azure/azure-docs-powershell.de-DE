---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: B423C1A1-1988-4721-81E7-3B7EC163B03A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchCertificate.md
ms.openlocfilehash: d567c176580cba0659d6c88c919ffa34cad393ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665272"
---
# <span data-ttu-id="a941a-101">New-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a941a-101">New-AzureBatchCertificate</span></span>

## <span data-ttu-id="a941a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a941a-102">SYNOPSIS</span></span>
<span data-ttu-id="a941a-103">Fügt dem angegebenen Batch Konto ein Zertifikat hinzu.</span><span class="sxs-lookup"><span data-stu-id="a941a-103">Adds a certificate to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a941a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a941a-104">SYNTAX</span></span>

### <span data-ttu-id="a941a-105">Datei (Standard)</span><span class="sxs-lookup"><span data-stu-id="a941a-105">File (Default)</span></span>
```
New-AzureBatchCertificate [-FilePath] <String> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a941a-106">RawData</span><span class="sxs-lookup"><span data-stu-id="a941a-106">RawData</span></span>
```
New-AzureBatchCertificate [-RawData] <Byte[]> [-Password <String>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a941a-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a941a-107">DESCRIPTION</span></span>
<span data-ttu-id="a941a-108">Mit dem Cmdlet **New-AzureBatchCertificate** wird dem angegebenen Azure-Batch Konto ein Zertifikat hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a941a-108">The **New-AzureBatchCertificate** cmdlet adds a certificate to the specified Azure Batch account.</span></span>

## <span data-ttu-id="a941a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a941a-109">EXAMPLES</span></span>

### <span data-ttu-id="a941a-110">Beispiel 1: Hinzufügen eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="a941a-110">Example 1: Add a certificate from a file</span></span>
```
PS C:\>New-AzureBatchCertificate -FilePath "E:\Certificates\MyCert.cer" -BatchContext $Context
```

<span data-ttu-id="a941a-111">Dieser Befehl fügt dem angegebenen Batch Konto ein Zertifikat mithilfe der Datei E:\Certificates\MyCert.cer.</span><span class="sxs-lookup"><span data-stu-id="a941a-111">This command adds a certificate to the specified Batch account by using the file E:\Certificates\MyCert.cer.</span></span>

### <span data-ttu-id="a941a-112">Beispiel 2: Hinzufügen eines Zertifikats aus unformatierten Daten</span><span class="sxs-lookup"><span data-stu-id="a941a-112">Example 2: Add a certificate from raw data</span></span>
```
PS C:\>$RawData = [System.IO.File]::ReadAllBytes("E:\Certificates\MyCert.pfx")
PS C:\> New-AzureBatchCertificate -RawData $RawData -Password "Password1234" -BatchContext $Context
```

<span data-ttu-id="a941a-113">Der erste Befehl liest die Daten aus der Datei mit dem Namen mycert. pfx in die $rawData Variable ein.</span><span class="sxs-lookup"><span data-stu-id="a941a-113">The first command reads the data from the file named MyCert.pfx into the $RawData variable.</span></span>

<span data-ttu-id="a941a-114">Mit dem zweiten Befehl wird dem angegebenen Stapelverarbeitungs Konto ein Zertifikat mithilfe der in $rawData gespeicherten Rohdaten hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="a941a-114">The second command adds a certificate to the specified Batch account using the raw data stored in $RawData.</span></span>

## <span data-ttu-id="a941a-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="a941a-115">PARAMETERS</span></span>

### <span data-ttu-id="a941a-116">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="a941a-116">-BatchContext</span></span>
<span data-ttu-id="a941a-117">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="a941a-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a941a-118">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a941a-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="a941a-119">-FilePath</span><span class="sxs-lookup"><span data-stu-id="a941a-119">-FilePath</span></span>
<span data-ttu-id="a941a-120">Gibt den Pfad der Zertifikatsdatei an.</span><span class="sxs-lookup"><span data-stu-id="a941a-120">Specifies the path of the certificate file.</span></span>
<span data-ttu-id="a941a-121">Die Zertifikatdatei muss entweder im CER-oder im PFX-Format vorliegen.</span><span class="sxs-lookup"><span data-stu-id="a941a-121">The certificate file must be in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="a941a-122">-Kennwort</span><span class="sxs-lookup"><span data-stu-id="a941a-122">-Password</span></span>
<span data-ttu-id="a941a-123">Gibt das Kennwort für den Zugriff auf den privaten Zertifikatschlüssel an.</span><span class="sxs-lookup"><span data-stu-id="a941a-123">Specifies the password to access the certificate private key.</span></span>
<span data-ttu-id="a941a-124">Sie müssen diesen Parameter angeben, wenn Sie im PFX-Format ein Zertifikat angeben.</span><span class="sxs-lookup"><span data-stu-id="a941a-124">You must specify this parameter if you specify a certificate in .pfx format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a941a-125">-RawData</span><span class="sxs-lookup"><span data-stu-id="a941a-125">-RawData</span></span>
<span data-ttu-id="a941a-126">Gibt die unformatierten Zertifikatdaten im CER-oder PFX-Format an.</span><span class="sxs-lookup"><span data-stu-id="a941a-126">Specifies the raw certificate data in either .cer or .pfx format.</span></span>

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

### <span data-ttu-id="a941a-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a941a-127">-DefaultProfile</span></span>
<span data-ttu-id="a941a-128">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a941a-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a941a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a941a-129">CommonParameters</span></span>
<span data-ttu-id="a941a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a941a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a941a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a941a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a941a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a941a-132">INPUTS</span></span>

### <span data-ttu-id="a941a-133">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a941a-133">BatchAccountContext</span></span>
<span data-ttu-id="a941a-134">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a941a-134">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="a941a-135">Byte []</span><span class="sxs-lookup"><span data-stu-id="a941a-135">Byte[]</span></span>
<span data-ttu-id="a941a-136">Der Parameter "rawData" akzeptiert den Wert vom Typ "Byte []" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="a941a-136">Parameter 'RawData' accepts value of type 'Byte[]' from the pipeline</span></span>

## <span data-ttu-id="a941a-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a941a-137">OUTPUTS</span></span>

## <span data-ttu-id="a941a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="a941a-138">NOTES</span></span>

## <span data-ttu-id="a941a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a941a-139">RELATED LINKS</span></span>

[<span data-ttu-id="a941a-140">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a941a-140">Get-AzureBatchCertificate</span></span>](./Get-AzureBatchCertificate.md)

[<span data-ttu-id="a941a-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a941a-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="a941a-142">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="a941a-142">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="a941a-143">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="a941a-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


