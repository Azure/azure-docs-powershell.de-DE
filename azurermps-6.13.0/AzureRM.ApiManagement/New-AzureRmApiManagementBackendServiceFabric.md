---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackendServiceFabric.md
ms.openlocfilehash: 925e4949b444c9338fad3f88cf5066430e1b5a75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480653"
---
# <span data-ttu-id="ef4a0-101">New-AzureRmApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ef4a0-101">New-AzureRmApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="ef4a0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ef4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4a0-103">Erstellt ein Objekt von `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="ef4a0-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef4a0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ef4a0-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint <String[]>
 -ClientCertificateThumbprint <String> [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>]
 [-ServerCertificateThumbprint <String[]>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef4a0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ef4a0-105">DESCRIPTION</span></span>

<span data-ttu-id="ef4a0-106">Das Cmdlet **New-AzureRmApiManagementBackendServiceFabric** erstellt ein Objekt `PsApiManagementServiceFabric` , das in Cmdlet **New-AzureRmApiManagementBackend** und **setAzureRmApiManagementBackend** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-106">The **New-AzureRmApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzureRmApiManagementBackend** and **Set-AzureRmApiManagementBackend**.</span></span>

## <span data-ttu-id="ef4a0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ef4a0-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4a0-108">Beispiel 1: Erstellen eines Back-End-Dienst Fabric-In-Memory-Objekts</span><span class="sxs-lookup"><span data-stu-id="ef4a0-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzureRmApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="ef4a0-109">Erstellen eines Back-End-Dienst Fabric-Vertrags</span><span class="sxs-lookup"><span data-stu-id="ef4a0-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="ef4a0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef4a0-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4a0-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef4a0-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="ef4a0-112">Fingerabdruck des Client Zertifikats für den Verwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="ef4a0-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="ef4a0-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-113">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4a0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4a0-114">-DefaultProfile</span></span>
<span data-ttu-id="ef4a0-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ef4a0-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="ef4a0-116">-ManagementEndpoint</span></span>
<span data-ttu-id="ef4a0-117">Endpunkte der Service Fabric-Cluster Verwaltung</span><span class="sxs-lookup"><span data-stu-id="ef4a0-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="ef4a0-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-118">This parameter is required.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4a0-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="ef4a0-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="ef4a0-120">Die maximale Anzahl von Wiederholungen beim Auflösen einer Service Fabric-Partition.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="ef4a0-121">Dieser Parameter ist optional und der Standardwert 5.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-121">This parameter is optional and default value is 5.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4a0-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="ef4a0-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="ef4a0-123">Fingerabdruck des Zertifikat-Cluster Verwaltungsdiensts wird für die TLS-Kommunikation verwendet. Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4a0-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="ef4a0-124">-ServerX509Name</span></span>
<span data-ttu-id="ef4a0-125">Server-X509-Zertifikatsnamen-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="ef4a0-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-126">This parameter is optional.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4a0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4a0-127">CommonParameters</span></span>
<span data-ttu-id="ef4a0-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4a0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4a0-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4a0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4a0-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ef4a0-130">INPUTS</span></span>

### <span data-ttu-id="ef4a0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="ef4a0-131">System.String</span></span>

## <span data-ttu-id="ef4a0-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ef4a0-132">OUTPUTS</span></span>

### <span data-ttu-id="ef4a0-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ef4a0-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="ef4a0-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="ef4a0-134">NOTES</span></span>

## <span data-ttu-id="ef4a0-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ef4a0-135">RELATED LINKS</span></span>

[<span data-ttu-id="ef4a0-136">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ef4a0-136">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="ef4a0-137">Neu – AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ef4a0-137">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ef4a0-138">Neu – AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ef4a0-138">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="ef4a0-139">Satz-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ef4a0-139">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="ef4a0-140">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ef4a0-140">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
