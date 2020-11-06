---
external help file: Microsoft.Azure.Commands.IotHub.dll-Help.xml
Module Name: AzureRM.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.iothub/get-azurermiothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/IotHub/Commands.IotHub/help/Get-AzureRmIotHubCertificate.md
ms.openlocfilehash: 745fcb6fdfb9ee47faf28cde84985dcfd7199ecc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503673"
---
# <span data-ttu-id="409a2-101">Get-AzureRmIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="409a2-101">Get-AzureRmIotHubCertificate</span></span>

## <span data-ttu-id="409a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="409a2-102">SYNOPSIS</span></span>
<span data-ttu-id="409a2-103">Listet alle Zertifikate oder ein bestimmtes Zertifikat auf, das in einem Azure-viel-Hub enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="409a2-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="409a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="409a2-104">SYNTAX</span></span>

### <span data-ttu-id="409a2-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="409a2-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409a2-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="409a2-106">InputObjectSet</span></span>
```
Get-AzureRmIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="409a2-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="409a2-107">ResourceIdSet</span></span>
```
Get-AzureRmIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="409a2-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="409a2-108">DESCRIPTION</span></span>
<span data-ttu-id="409a2-109">Eine ausführliche Erläuterung der CA-Zertifikate in Azure viel Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="409a2-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="409a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="409a2-110">EXAMPLES</span></span>

### <span data-ttu-id="409a2-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="409a2-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="409a2-112">Auflisten aller Zertifikate in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="409a2-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="409a2-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="409a2-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/IotHubs/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiothub
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="409a2-114">Anzeigen von Details zu myCertificate</span><span class="sxs-lookup"><span data-stu-id="409a2-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="409a2-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="409a2-115">PARAMETERS</span></span>

### <span data-ttu-id="409a2-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="409a2-116">-CertificateName</span></span>
<span data-ttu-id="409a2-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="409a2-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="409a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409a2-118">-DefaultProfile</span></span>
<span data-ttu-id="409a2-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="409a2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="409a2-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="409a2-120">-InputObject</span></span>
<span data-ttu-id="409a2-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="409a2-121">IotHub Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="409a2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="409a2-122">-Name</span></span>
<span data-ttu-id="409a2-123">Name des viel-Hubs</span><span class="sxs-lookup"><span data-stu-id="409a2-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409a2-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="409a2-124">-ResourceGroupName</span></span>
<span data-ttu-id="409a2-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="409a2-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="409a2-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="409a2-126">-ResourceId</span></span>
<span data-ttu-id="409a2-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="409a2-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="409a2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409a2-128">CommonParameters</span></span>
<span data-ttu-id="409a2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="409a2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409a2-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="409a2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409a2-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="409a2-131">INPUTS</span></span>

### <span data-ttu-id="409a2-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="409a2-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>
<span data-ttu-id="409a2-133">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="409a2-133">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="409a2-134">System. String</span><span class="sxs-lookup"><span data-stu-id="409a2-134">System.String</span></span>

## <span data-ttu-id="409a2-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="409a2-135">OUTPUTS</span></span>

### <span data-ttu-id="409a2-136">Microsoft. Azure. Commands. Management. IotHub. Models. PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="409a2-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="409a2-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="409a2-137">NOTES</span></span>

## <span data-ttu-id="409a2-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="409a2-138">RELATED LINKS</span></span>
