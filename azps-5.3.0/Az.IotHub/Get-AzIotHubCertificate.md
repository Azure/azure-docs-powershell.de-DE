---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubCertificate.md
ms.openlocfilehash: 8bc586ea9543c7545e7d24e3bc6d7bc36bb77d49
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472497"
---
# <span data-ttu-id="160e1-101">Get-AzIotHubCertificate</span><span class="sxs-lookup"><span data-stu-id="160e1-101">Get-AzIotHubCertificate</span></span>

## <span data-ttu-id="160e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="160e1-102">SYNOPSIS</span></span>
<span data-ttu-id="160e1-103">Listet alle Zertifikate oder ein bestimmtes Zertifikat auf, die in einem Azure IoT Hub enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="160e1-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="160e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="160e1-104">SYNTAX</span></span>

### <span data-ttu-id="160e1-105">ResourceSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="160e1-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubCertificate [-ResourceGroupName] <String> [-Name] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="160e1-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="160e1-106">InputObjectSet</span></span>
```
Get-AzIotHubCertificate [-InputObject] <PSIotHub> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="160e1-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="160e1-107">ResourceIdSet</span></span>
```
Get-AzIotHubCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="160e1-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="160e1-108">DESCRIPTION</span></span>
<span data-ttu-id="160e1-109">Eine ausführliche Erläuterung der Zertifizierungsstellenzertifikate in Azure IoT Hub finden Sie unter https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span><span class="sxs-lookup"><span data-stu-id="160e1-109">For a detailed explanation of CA certificates in Azure IoT Hub, see https://docs.microsoft.com/en-us/azure/iot-hub/iot-hub-x509ca-overview</span></span>

## <span data-ttu-id="160e1-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="160e1-110">EXAMPLES</span></span>

### <span data-ttu-id="160e1-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="160e1-111">Example 1</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub"

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiothub3   mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiothub    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="160e1-112">Auflisten aller Zertifikate in MyIotHub</span><span class="sxs-lookup"><span data-stu-id="160e1-112">List all certificates in MyIotHub</span></span>

### <span data-ttu-id="160e1-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="160e1-113">Example 2</span></span>
```
PS C:\> Get-AzIotHubCertificate -ResourceGroupName "myresourcegroup" -Name "myiothub" -CertificateName "mycertificate"

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

<span data-ttu-id="160e1-114">Details zu MyCertificate anzeigen</span><span class="sxs-lookup"><span data-stu-id="160e1-114">Show details about MyCertificate</span></span>

## <span data-ttu-id="160e1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="160e1-115">PARAMETERS</span></span>

### <span data-ttu-id="160e1-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="160e1-116">-CertificateName</span></span>
<span data-ttu-id="160e1-117">Name des Zertifikats</span><span class="sxs-lookup"><span data-stu-id="160e1-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="160e1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160e1-118">-DefaultProfile</span></span>
<span data-ttu-id="160e1-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="160e1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="160e1-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="160e1-120">-InputObject</span></span>
<span data-ttu-id="160e1-121">IotHub-Objekt</span><span class="sxs-lookup"><span data-stu-id="160e1-121">IotHub Object</span></span>

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

### <span data-ttu-id="160e1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="160e1-122">-Name</span></span>
<span data-ttu-id="160e1-123">Name des Iot Hub</span><span class="sxs-lookup"><span data-stu-id="160e1-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="160e1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160e1-124">-ResourceGroupName</span></span>
<span data-ttu-id="160e1-125">Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="160e1-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="160e1-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="160e1-126">-ResourceId</span></span>
<span data-ttu-id="160e1-127">IotHub-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="160e1-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="160e1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160e1-128">CommonParameters</span></span>
<span data-ttu-id="160e1-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="160e1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160e1-130">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="160e1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160e1-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="160e1-131">INPUTS</span></span>

### <span data-ttu-id="160e1-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="160e1-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="160e1-133">System.String</span><span class="sxs-lookup"><span data-stu-id="160e1-133">System.String</span></span>

## <span data-ttu-id="160e1-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="160e1-134">OUTPUTS</span></span>

### <span data-ttu-id="160e1-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span><span class="sxs-lookup"><span data-stu-id="160e1-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSCertificateDescription</span></span>

## <span data-ttu-id="160e1-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="160e1-136">NOTES</span></span>

## <span data-ttu-id="160e1-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="160e1-137">RELATED LINKS</span></span>
