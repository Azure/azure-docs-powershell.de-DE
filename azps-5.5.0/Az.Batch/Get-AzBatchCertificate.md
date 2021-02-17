---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A9C98F8F-90F2-4BF4-A234-31966FBB975B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchCertificate.md
ms.openlocfilehash: 26bd35f59ae5e640093c1695e7caf991e1e1e956
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100171563"
---
# <span data-ttu-id="1562f-101">Get-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1562f-101">Get-AzBatchCertificate</span></span>

## <span data-ttu-id="1562f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1562f-102">SYNOPSIS</span></span>
<span data-ttu-id="1562f-103">Ruft die Zertifikate in einem Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="1562f-103">Gets the certificates in a Batch account.</span></span>

## <span data-ttu-id="1562f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1562f-104">SYNTAX</span></span>

### <span data-ttu-id="1562f-105">ODataFilter (Standard)</span><span class="sxs-lookup"><span data-stu-id="1562f-105">ODataFilter (Default)</span></span>
```
Get-AzBatchCertificate [-Filter <String>] [-MaxCount <Int32>] [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1562f-106">Thumbprint</span><span class="sxs-lookup"><span data-stu-id="1562f-106">Thumbprint</span></span>
```
Get-AzBatchCertificate [-ThumbprintAlgorithm] <String> [-Thumbprint] <String> [-Select <String>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1562f-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1562f-107">DESCRIPTION</span></span>
<span data-ttu-id="1562f-108">Das **Cmdlet "Get-AzBatchCertificate"** ruft die Zertifikate im Azure -Batchkonto ab, die vom *Parameter "BatchContext"* angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1562f-108">The **Get-AzBatchCertificate** cmdlet gets the certificates in the Azure Batch account that the *BatchContext* parameter specifies.</span></span>
<span data-ttu-id="1562f-109">Um ein bestimmtes Zertifikat zu erhalten, geben Sie die Parameter *ThumbprintAlgorithm* und *Thumbprint* an.</span><span class="sxs-lookup"><span data-stu-id="1562f-109">To obtain a particular certificate, specify the *ThumbprintAlgorithm* and *Thumbprint* parameters.</span></span>
<span data-ttu-id="1562f-110">Geben Sie den *Filterparameter* an, um die Zertifikate zu erhalten, die einem Open Data Protocol (OData)-Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1562f-110">Specify the *Filter* parameter to get the certificates that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="1562f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1562f-111">EXAMPLES</span></span>

### <span data-ttu-id="1562f-112">Beispiel 1: Erhalten eines Zertifikats per Fingerabdruck</span><span class="sxs-lookup"><span data-stu-id="1562f-112">Example 1: Get a certificate by thumbprint</span></span>
```
PS C:\>Get-AzBatchCertificate -ThumbprintAlgorithm "sha1" - Thumbprint "C1E494A415149C5F211C4778B52F2E834A07247C" -BatchContext $Context
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

<span data-ttu-id="1562f-113">Dieser Befehl ruft ein einzelnes Zertifikat mit dem angegebenen Fingerabdruck ab.</span><span class="sxs-lookup"><span data-stu-id="1562f-113">This command gets a single certificate that has the specified thumbprint.</span></span>
<span data-ttu-id="1562f-114">Der Algorithmus zum Drucken des Zertifikats ist "sha1".</span><span class="sxs-lookup"><span data-stu-id="1562f-114">The certificate thumbprint algorithm is sha1.</span></span>

### <span data-ttu-id="1562f-115">Beispiel 2: Erhalten gefilterter Zertifikate</span><span class="sxs-lookup"><span data-stu-id="1562f-115">Example 2: Get filtered certificates</span></span>
```
PS C:\>Get-AzBatchCertificate -Filter "state eq 'active'" -BatchContext $Context
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

<span data-ttu-id="1562f-116">Dieser Befehl ruft alle Zertifikate im aktiven Zustand aus dem Batchkonto ab.</span><span class="sxs-lookup"><span data-stu-id="1562f-116">This command gets all certificates in the active state from the Batch account.</span></span>
<span data-ttu-id="1562f-117">Der *Parameter "Filter"* gibt den Zustand an.</span><span class="sxs-lookup"><span data-stu-id="1562f-117">The *Filter* parameter specifies the state.</span></span>

## <span data-ttu-id="1562f-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1562f-118">PARAMETERS</span></span>

### <span data-ttu-id="1562f-119">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="1562f-119">-BatchContext</span></span>
<span data-ttu-id="1562f-120">Gibt die **BatchAccountContext-Instanz** an, die von diesem Cmdlet für die Interaktion mit dem Batchdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1562f-120">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="1562f-121">Wenn Sie das cmdlet Get-AzBatchAccount BatchAccountContext verwenden, wird die Azure Active Directory-Authentifizierung bei der Interaktion mit dem Batchdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="1562f-121">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="1562f-122">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das cmdlet Get-AzBatchAccountKey, um ein BatchAccountContext-Objekt mit aufgefüllten Zugriffstasten zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1562f-122">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="1562f-123">Bei der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig der primäre Zugriffsschlüssel verwendet.</span><span class="sxs-lookup"><span data-stu-id="1562f-123">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="1562f-124">Wenn Sie den zu verwendende Schlüssel ändern möchten, legen Sie die Eigenschaft "BatchAccountContext.KeyInUse" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="1562f-124">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="1562f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1562f-125">-DefaultProfile</span></span>
<span data-ttu-id="1562f-126">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1562f-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1562f-127">-Filter</span><span class="sxs-lookup"><span data-stu-id="1562f-127">-Filter</span></span>
<span data-ttu-id="1562f-128">Gibt eine OData-Filterklausel an.</span><span class="sxs-lookup"><span data-stu-id="1562f-128">Specifies an OData filter clause.</span></span>
<span data-ttu-id="1562f-129">Wenn Sie diesen Parameter angeben, ruft dieses Cmdlet die Zertifikate ab, die dem Filter entsprechen.</span><span class="sxs-lookup"><span data-stu-id="1562f-129">If you specify this parameter, this cmdlet gets the certificates that match the filter.</span></span>

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

### <span data-ttu-id="1562f-130">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="1562f-130">-MaxCount</span></span>
<span data-ttu-id="1562f-131">Gibt die maximale Anzahl von zurückzukehrenden Zertifikaten an.</span><span class="sxs-lookup"><span data-stu-id="1562f-131">Specifies the maximum number of certificates to return.</span></span>
<span data-ttu-id="1562f-132">Wenn Sie einen Wert von Null (0) oder kleiner angeben, wird für das Cmdlet keine Obergrenze verwendet.</span><span class="sxs-lookup"><span data-stu-id="1562f-132">If you specify a value of zero (0) or less, the cmdlet does not use an upper limit.</span></span>
<span data-ttu-id="1562f-133">Der Standardwert ist 1000.</span><span class="sxs-lookup"><span data-stu-id="1562f-133">The default value is 1000.</span></span>

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

### <span data-ttu-id="1562f-134">-Select</span><span class="sxs-lookup"><span data-stu-id="1562f-134">-Select</span></span>
<span data-ttu-id="1562f-135">Gibt eine OData-Auswahlklausel an.</span><span class="sxs-lookup"><span data-stu-id="1562f-135">Specifies an OData select clause.</span></span>
<span data-ttu-id="1562f-136">Geben Sie einen Wert für diesen Parameter an, um bestimmte Eigenschaften und nicht alle Objekteigenschaften zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="1562f-136">Specify a value for this parameter to get specific properties rather than all object properties.</span></span>

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

### <span data-ttu-id="1562f-137">-Thumbprint</span><span class="sxs-lookup"><span data-stu-id="1562f-137">-Thumbprint</span></span>
<span data-ttu-id="1562f-138">Gibt den Fingerabdruck des Zertifikats an, das dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="1562f-138">Specifies the thumbprint of the certificate that this cmdlet gets.</span></span>

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

### <span data-ttu-id="1562f-139">-ThumbprintAlgorithm</span><span class="sxs-lookup"><span data-stu-id="1562f-139">-ThumbprintAlgorithm</span></span>
<span data-ttu-id="1562f-140">Gibt den Algorithmus an, der zum Ableitung des Parameters *"Thumbprint" verwendet* wird.</span><span class="sxs-lookup"><span data-stu-id="1562f-140">Specifies the algorithm used to derive the *Thumbprint* parameter.</span></span>
<span data-ttu-id="1562f-141">Derzeit ist der einzige gültige Wert "sha1".</span><span class="sxs-lookup"><span data-stu-id="1562f-141">Currently, the only valid value is sha1.</span></span>

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

### <span data-ttu-id="1562f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1562f-142">CommonParameters</span></span>
<span data-ttu-id="1562f-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1562f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1562f-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1562f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1562f-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1562f-145">INPUTS</span></span>

### <span data-ttu-id="1562f-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1562f-146">System.String</span></span>

### <span data-ttu-id="1562f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="1562f-147">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="1562f-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1562f-148">OUTPUTS</span></span>

### <span data-ttu-id="1562f-149">Microsoft.Azure.Commands.Batch. Models.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="1562f-149">Microsoft.Azure.Commands.Batch.Models.PSCertificate</span></span>

## <span data-ttu-id="1562f-150">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1562f-150">NOTES</span></span>

## <span data-ttu-id="1562f-151">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1562f-151">RELATED LINKS</span></span>

[<span data-ttu-id="1562f-152">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="1562f-152">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="1562f-153">New-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1562f-153">New-AzBatchCertificate</span></span>](./New-AzBatchCertificate.md)

[<span data-ttu-id="1562f-154">Remove-AzBatchCertificate</span><span class="sxs-lookup"><span data-stu-id="1562f-154">Remove-AzBatchCertificate</span></span>](./Remove-AzBatchCertificate.md)

[<span data-ttu-id="1562f-155">Azure-Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="1562f-155">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
