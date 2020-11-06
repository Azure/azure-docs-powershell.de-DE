---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificateVerificationCode.md
ms.openlocfilehash: 55cd14216e9a592128c8d600238b49862cb1f20a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496537"
---
# <span data-ttu-id="c2513-101">Get-AzureRmIotHubCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="c2513-101">Get-AzureRmIotHubCertificateVerificationCode</span></span>

## <span data-ttu-id="c2513-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c2513-102">SYNOPSIS</span></span>
<span data-ttu-id="c2513-103">Generiert einen Bestätigungscode für ein Azure-viel-Hub-Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="c2513-103">Generates a verification code for an Azure IoT Hub certificate.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2513-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c2513-104">SYNTAX</span></span>

### <span data-ttu-id="c2513-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2513-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2513-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c2513-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-InputObject] <PSCertificateDescription>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2513-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2513-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2513-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c2513-108">DESCRIPTION</span></span>
<span data-ttu-id="c2513-109">Dieser Verifizierungscode wird verwendet, um den Beweis des Besitzes für ein Zertifikat abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="c2513-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="c2513-110">Verwenden Sie diesen Verifizierungscode als CN eines neuen Zertifikats, das mit dem privaten Stammzertifikat-Schlüssel signiert wurde.</span><span class="sxs-lookup"><span data-stu-id="c2513-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="c2513-111">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="c2513-111">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="c2513-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c2513-112">EXAMPLES</span></span>

### <span data-ttu-id="c2513-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2513-113">Example 1</span></span>
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

<span data-ttu-id="c2513-114">Generiert einen Bestätigungscode für myCertificate</span><span class="sxs-lookup"><span data-stu-id="c2513-114">Generates a verification code for MyCertificate</span></span> 

## <span data-ttu-id="c2513-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2513-115">PARAMETERS</span></span>

### <span data-ttu-id="c2513-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="c2513-116">-CertificateName</span></span>
<span data-ttu-id="c2513-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c2513-117">Name of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2513-118">-DefaultProfile</span></span>
<span data-ttu-id="c2513-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c2513-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2513-120">-ETag</span><span class="sxs-lookup"><span data-stu-id="c2513-120">-Etag</span></span>
<span data-ttu-id="c2513-121">ETag des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="c2513-121">Etag of the Certificate</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c2513-122">-InputObject</span></span>
<span data-ttu-id="c2513-123">Certificate-Objekt</span><span class="sxs-lookup"><span data-stu-id="c2513-123">Certificate Object</span></span>

```yaml
Type: PSCertificateDescription
Parameter Sets: InputObjectSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-124">-Name</span><span class="sxs-lookup"><span data-stu-id="c2513-124">-Name</span></span>
<span data-ttu-id="c2513-125">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="c2513-125">Name of the Iot Hub</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2513-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2513-127">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="c2513-127">Name of the Resource Group</span></span>

```yaml
Type: String
Parameter Sets: ResourceSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="c2513-128">-ResourceId</span></span>
<span data-ttu-id="c2513-129">Zertifikatressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="c2513-129">Certificate Resource Id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2513-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2513-130">CommonParameters</span></span>
<span data-ttu-id="c2513-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2513-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2513-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2513-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2513-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c2513-133">INPUTS</span></span>

### <span data-ttu-id="c2513-134">System. String</span><span class="sxs-lookup"><span data-stu-id="c2513-134">System.String</span></span>

## <span data-ttu-id="c2513-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c2513-135">OUTPUTS</span></span>

### <span data-ttu-id="c2513-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateWithNonceDescription</span><span class="sxs-lookup"><span data-stu-id="c2513-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateWithNonceDescription</span></span>

## <span data-ttu-id="c2513-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="c2513-137">NOTES</span></span>

## <span data-ttu-id="c2513-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c2513-138">RELATED LINKS</span></span>

