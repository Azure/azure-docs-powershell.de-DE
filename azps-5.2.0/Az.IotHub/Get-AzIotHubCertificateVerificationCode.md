---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificateVerificationCode.md
ms.openlocfilehash: 4bf362402ba3db0ba50d9144d6bb9fa79977a998
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292763"
---
# <span data-ttu-id="4ee6b-101">Get-AzIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="4ee6b-101">Get-AzIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="4ee6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4ee6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ee6b-103">Generiert einen Überprüfungscode für ein Azure IoT Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

## <span data-ttu-id="4ee6b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ee6b-104">SYNTAX</span></span>

### <span data-ttu-id="4ee6b-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4ee6b-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ee6b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ee6b-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ee6b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ee6b-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ee6b-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4ee6b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ee6b-109">Dieser Überprüfungscode wird verwendet, um den Schritt zum Nachweis des Besitzes für ein Zertifikat zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="4ee6b-110">Verwenden Sie diesen Überprüfungscode als CN eines neuen Zertifikats, das mit dem privaten Schlüssel für Stammzertifikate signiert ist.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="4ee6b-111">Eine ausführliche Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="4ee6b-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="4ee6b-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4ee6b-112">EXAMPLES</span></span>

### <span data-ttu-id="4ee6b-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4ee6b-113">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
VerificationCode    : 47292AB6260DB02CCD2D07C601B7303DD49858B6
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="4ee6b-114">Generiert einen Prüfcode für MyCertificate.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="4ee6b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4ee6b-115">PARAMETERS</span></span>

### <span data-ttu-id="4ee6b-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="4ee6b-116">-CertificateName</span></span>
<span data-ttu-id="4ee6b-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="4ee6b-117">Name of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ee6b-118">-DefaultProfile</span></span>
<span data-ttu-id="4ee6b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4ee6b-120">-Etag</span><span class="sxs-lookup"><span data-stu-id="4ee6b-120">-Etag</span></span>
<span data-ttu-id="4ee6b-121">Etag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="4ee6b-121">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ee6b-122">-InputObject</span></span>
<span data-ttu-id="4ee6b-123">Zertifikatobjekt</span><span class="sxs-lookup"><span data-stu-id="4ee6b-123">Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-124">-Name</span><span class="sxs-lookup"><span data-stu-id="4ee6b-124">-Name</span></span>
<span data-ttu-id="4ee6b-125">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="4ee6b-125">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ee6b-126">-ResourceGroupName</span></span>
<span data-ttu-id="4ee6b-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="4ee6b-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ee6b-128">-ResourceId</span></span>
<span data-ttu-id="4ee6b-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="4ee6b-129">Certificate Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4ee6b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ee6b-130">CommonParameters</span></span>
<span data-ttu-id="4ee6b-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ee6b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ee6b-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ee6b-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ee6b-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee6b-133">INPUTS</span></span>

### <span data-ttu-id="4ee6b-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="4ee6b-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

### <span data-ttu-id="4ee6b-135">System.String</span><span class="sxs-lookup"><span data-stu-id="4ee6b-135">System.String</span></span>

## <span data-ttu-id="4ee6b-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4ee6b-136">OUTPUTS</span></span>

### <span data-ttu-id="4ee6b-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="4ee6b-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="4ee6b-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4ee6b-138">NOTES</span></span>

## <span data-ttu-id="4ee6b-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4ee6b-139">RELATED LINKS</span></span>
