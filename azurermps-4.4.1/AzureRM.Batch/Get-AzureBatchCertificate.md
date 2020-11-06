---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchCertificate.md
ms.openlocfilehash: 84b70c119cc91bbcfd468c84818f0b1d7856cae3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505257"
---
# <span data-ttu-id="b0d06-101">Get-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d06-101">Get-AzureBatchCertificate</span></span>

## <span data-ttu-id="b0d06-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b0d06-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d06-103">Ruft die Zertifikate in einem Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b0d06-103">Gets the certificates in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0d06-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0d06-104">SYNTAX</span></span>

### <span data-ttu-id="b0d06-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="b0d06-105">ODataFilter (Default)</span></span>
```
Get-AzureBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0d06-106">Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b0d06-106">Thumbprint</span></span>
```
Get-AzureBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0d06-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0d06-107">DESCRIPTION</span></span>
<span data-ttu-id="b0d06-108">Das Cmdlet " **Get-AzureBatchCertificate** " Ruft die Zertifikate im Azure-Batch Konto ab, das vom *batchcontext* -Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b0d06-108">The **Get-AzureBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="b0d06-109">Um ein bestimmtes Zertifikat zu erhalten, geben Sie die Parameter *ThumbprintAlgorithm* und *Fingerabdruck* an.</span><span class="sxs-lookup"><span data-stu-id="b0d06-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="b0d06-110">Geben Sie den *Filter* -Parameter an, um die Zertifikate abzurufen, die einem OData-Filter (Open Data Protocol) entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b0d06-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="b0d06-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b0d06-111">EXAMPLES</span></span>

### <span data-ttu-id="b0d06-112">Beispiel 1: Abrufen eines Zertifikats nach dem Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b0d06-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzureBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=C1E494A415149C5F211C4778B52F2E834A07247
C) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="b0d06-113">Dieser Befehl ruft ein einzelnes Zertifikat ab, das den angegebenen Fingerabdruck aufweist.</span><span class="sxs-lookup"><span data-stu-id="b0d06-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="b0d06-114">Der Zertifikat Fingerabdruck-Algorithmus ist SHA1.</span><span class="sxs-lookup"><span data-stu-id="b0d06-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="b0d06-115">Beispiel 2: Abrufen gefilterter Zertifikate</span><span class="sxs-lookup"><span data-stu-id="b0d06-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzureBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
Thumbprint                  : 025b351b087a084c5067f5e71eff8591970323f9
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=025b351b087a084c5067f5e71eff8591970323f9) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:17 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAyMB4XDTE1MTAwMjE2MjkxNFoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDIwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAJxagvVrlnKfv6hfzSiFJUkdGkPjC3tFiKebK6IaeHzesFdFfupXUE
wT0xOWh9xwa3OVkPECEc/u1sw3iVX/J4AODiwzmOWutoVRpWjxGFpgw9+dPvXMjs/Ue7JL7ag3siHs5EcarW91qKbgtko6i/r4emaRyk60U93TrbWQAWJ9AgMBAAGjS
zBJMEcGA1UdAQRAMD6AEAdqsOpyeXF/uDe7ZGKeez+hGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMoIQy9W5y8iwhppGhtAG06dHKTAJBgUrDgMCHQUAA4GBAC0MaAem
6ByyURFvGnFZyjEepjXC5wcaGq+gguDFe8rG88ceig1ZqewdcmC1y4p05uBhbmETbYVWzJarNsHYq2LTihi4t2J4jt2YVYz/IRdUB82iaFFbJRSPrN+6xD3KM2lve5N
4OjtlZAdiXiSUYFf3I6ypberUsAdba3QQajCN
DeleteCertificateError      : 

Thumbprint                  : c1e494a415149c5f211c4778b52f2e834a07247c
ThumbprintAlgorithm         : sha1
Url                         : https://pstests.eastus.batch.azure.com/certificates(thumbprintAlgorithm=sha1,thumbprint=c1e494a415149c5f211c4778b52f2e834a07247c) 
State                       : Active
StateTransitionTime         : 10/6/2015 6:21:16 PM
PreviousState               : 
PreviousStateTransitionTime : 
Data                        : 
CertificateFormat           : 
Password                    : 
PublicData                  : MIIB9DCCAWGgAwIBAgIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAMBYxFDASBgNVBAMTC0JhdGNoVGVzdDAxMB4XDTE1MTAwMjE2MjkwNVoXDTM5MTIzMTIzNTk
1OVowFjEUMBIGA1UEAxMLQmF0Y2hUZXN0MDEwgZ8wDQYJKoZIhvcNAQEBBQADgY0AMIGJAoGBAM06unpRipn3BmHBM75d0s8w/Wwifci16PoJo4c2V68GwsCCFsNOn5
ypo7BBXo1fpBjrnso5w+koaE5LjxkBSVm+TkogwbKlW6WURTM0O5viRVbPnEEU/Y01Pj5cJElFuLEk9Uoe/r/lP8b5A607t1cPjSXkwhEZEYc3LkHDSo0ZAgMBAAGjS
zBJMEcGA1UdAQRAMD6AEFRsTAsrvF+FmPuICooZXaKhGDAWMRQwEgYDVQQDEwtCYXRjaFRlc3QwMYIQpUXhwCuAPJRDhl7kY/0PdTAJBgUrDgMCHQUAA4GBALt0F8Ep
+8XVE/M2aNtxzlku72gxiOiAo1HmpUaixXx3gl8kdP3xgoKMaq4JskqdLmbJJUnCQ3wmzsdPwjswsW2ycT12zuBddaiS+id98k8U/KYc6FxMgS+H70FYOxARLn7P4FS
SBf/QCyign+BherzezdZ5NBdfzbmWxIMP5iFJ
DeleteCertificateError      :
```

<span data-ttu-id="b0d06-116">Dieser Befehl ruft alle Zertifikate im aktiven Zustand vom Batch Konto ab.</span><span class="sxs-lookup"><span data-stu-id="b0d06-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="b0d06-117">Der Parameter *Filter* gibt den Zustand an.</span><span class="sxs-lookup"><span data-stu-id="b0d06-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="b0d06-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0d06-118">PARAMETERS</span></span>

### <span data-ttu-id="b0d06-119">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="b0d06-119">-BatchContext</span></span>
<span data-ttu-id="b0d06-120">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b0d06-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="b0d06-121">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d06-121">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="b0d06-122">-Filter</span><span class="sxs-lookup"><span data-stu-id="b0d06-122">-Filter</span></span>
<span data-ttu-id="b0d06-123">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="b0d06-123">Specifies an OData filter clause.</span></span>
<span data-ttu-id="b0d06-124">Wenn Sie diesen Parameter angeben, ruft dieses Cmdlet die Zertifikate ab, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="b0d06-124">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d06-125">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b0d06-125">-MaxCount</span></span>
<span data-ttu-id="b0d06-126">Gibt die maximale Anzahl von Zertifikaten an, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b0d06-126">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="b0d06-127">Wenn Sie den Wert 0 (null) oder weniger angeben, verwendet das Cmdlet keine Obergrenze.</span><span class="sxs-lookup"><span data-stu-id="b0d06-127">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="b0d06-128">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="b0d06-128">The default value is 1000.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ODataFilter
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d06-129">-Wählen Sie</span><span class="sxs-lookup"><span data-stu-id="b0d06-129">-Select</span></span>
<span data-ttu-id="b0d06-130">Gibt eine OData-Auswahl Klausel an.</span><span class="sxs-lookup"><span data-stu-id="b0d06-130">Specifies an OData select clause.</span></span>
<span data-ttu-id="b0d06-131">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften abzurufen.</span><span class="sxs-lookup"><span data-stu-id="b0d06-131">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="b0d06-132">-Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="b0d06-132">-Thumbprint</span></span>
<span data-ttu-id="b0d06-133">Gibt den Fingerabdruck des Zertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="b0d06-133">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d06-134">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="b0d06-134">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="b0d06-135">Gibt den Algorithmus an, der zum Ableiten des Parameters *Fingerabdruck* verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b0d06-135">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="b0d06-136">Derzeit ist der einzige gültige Wert SHA1.</span><span class="sxs-lookup"><span data-stu-id="b0d06-136">Currently, the only valid value is sha1.</span></span>

```yaml
Type: System.String
Parameter Sets: Thumbprint
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0d06-137">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d06-137">-DefaultProfile</span></span>
<span data-ttu-id="b0d06-138">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b0d06-138">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0d06-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d06-139">CommonParameters</span></span>
<span data-ttu-id="b0d06-140">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d06-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d06-141">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d06-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d06-142">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b0d06-142">INPUTS</span></span>

### <span data-ttu-id="b0d06-143">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="b0d06-143">BatchAccountContext</span></span>
<span data-ttu-id="b0d06-144">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="b0d06-144">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="b0d06-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b0d06-145">OUTPUTS</span></span>

### <span data-ttu-id="b0d06-146">Microsoft.Azure.Commands.Batch. Models. PSCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d06-146">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="b0d06-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="b0d06-147">NOTES</span></span>

## <span data-ttu-id="b0d06-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b0d06-148">RELATED LINKS</span></span>

[<span data-ttu-id="b0d06-149">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="b0d06-149">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="b0d06-150">Neu – AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d06-150">New-AzureBatchCertificate</span></span>](./New-AzureBatchCertificate.md)

[<span data-ttu-id="b0d06-151">Remove-AzureBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="b0d06-151">Remove-AzureBatchCertificate</span></span>](./Remove-AzureBatchCertificate.md)

[<span data-ttu-id="b0d06-152">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="b0d06-152">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


