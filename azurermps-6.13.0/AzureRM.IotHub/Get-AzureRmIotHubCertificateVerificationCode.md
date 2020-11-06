---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: a2c4c72f93597f3275e9edb1fecb6139eafbeb50
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503669"
---
# <span data-ttu-id="c37fa-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="c37fa-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="c37fa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c37fa-102">SYNOPSIS</span></span>
<span data-ttu-id="c37fa-103">Generiert einen Bestätigungscode für ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c37fa-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c37fa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c37fa-104">SYNTAX</span></span>

### <span data-ttu-id="c37fa-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c37fa-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c37fa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c37fa-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c37fa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c37fa-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c37fa-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c37fa-108">DESCRIPTION</span></span>
<span data-ttu-id="c37fa-109">Dieser Verifizierungscode wird verwendet, um den Beweis des Besitzes für ein Zertifikat abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c37fa-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="c37fa-110">Verwenden Sie diesen Verifizierungscode als CN eines neuen Zertifikats, das mit dem privaten Stammzertifikat-Schlüssel signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c37fa-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="c37fa-111">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c37fa-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c37fa-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c37fa-112">EXAMPLES</span></span>

### <span data-ttu-id="c37fa-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c37fa-113">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="c37fa-114">Generiert einen Bestätigungscode für myCertificate</span><span class="sxs-lookup"><span data-stu-id="c37fa-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="c37fa-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c37fa-115">PARAMETERS</span></span>

### <span data-ttu-id="c37fa-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c37fa-116">-CertificateName</span></span>
<span data-ttu-id="c37fa-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c37fa-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="c37fa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c37fa-118">-DefaultProfile</span></span>
<span data-ttu-id="c37fa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c37fa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c37fa-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="c37fa-120">-Etag</span></span>
<span data-ttu-id="c37fa-121">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c37fa-121">Etag of the Certificate</span></span>

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

### <span data-ttu-id="c37fa-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c37fa-122">-InputObject</span></span>
<span data-ttu-id="c37fa-123">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="c37fa-123">Certificate Object</span></span>

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

### <span data-ttu-id="c37fa-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c37fa-124">-Name</span></span>
<span data-ttu-id="c37fa-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="c37fa-125">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c37fa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c37fa-126">-ResourceGroupName</span></span>
<span data-ttu-id="c37fa-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c37fa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c37fa-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c37fa-128">-ResourceId</span></span>
<span data-ttu-id="c37fa-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c37fa-129">Certificate Resource Id</span></span>

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

### <span data-ttu-id="c37fa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c37fa-130">CommonParameters</span></span>
<span data-ttu-id="c37fa-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c37fa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c37fa-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c37fa-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c37fa-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c37fa-133">INPUTS</span></span>

### <span data-ttu-id="c37fa-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="c37fa-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>
<span data-ttu-id="c37fa-135">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c37fa-135">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="c37fa-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c37fa-136">System.String</span></span>

## <span data-ttu-id="c37fa-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c37fa-137">OUTPUTS</span></span>

### <span data-ttu-id="c37fa-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="c37fa-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="c37fa-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="c37fa-139">NOTES</span></span>

## <span data-ttu-id="c37fa-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c37fa-140">RELATED LINKS</span></span>
