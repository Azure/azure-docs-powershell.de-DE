---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackendservicefabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackendServiceFabric.md
ms.openlocfilehash: 352e40aa64adf5eea98950ac9271f0237e634ab6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010096"
---
# <span data-ttu-id="23c00-101">New-AzApiManagementBackendServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c00-101">New-AzApiManagementBackendServiceFabric</span></span>

## <span data-ttu-id="23c00-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23c00-102">SYNOPSIS</span></span>
<span data-ttu-id="23c00-103">Erstellt ein Objekt von `PsApiManagementServiceFabric`</span><span class="sxs-lookup"><span data-stu-id="23c00-103">Creates an object of `PsApiManagementServiceFabric`</span></span>

## <span data-ttu-id="23c00-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23c00-104">SYNTAX</span></span>

```
New-AzApiManagementBackendServiceFabric -ManagementEndpoint <String[]> -ClientCertificateThumbprint <String>
 [-MaxPartitionResolutionRetry <Int32>] [-ServerX509Name <Hashtable>] [-ServerCertificateThumbprint <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23c00-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23c00-105">DESCRIPTION</span></span>

<span data-ttu-id="23c00-106">Das Cmdlet **New-AzApiManagementBackendServiceFabric** erstellt ein Objekt `PsApiManagementServiceFabric` , das in Cmdlet **New-AzApiManagementBackend** und **setAzApiManagementBackend** verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="23c00-106">The **New-AzApiManagementBackendServiceFabric** cmdlet creates an object of `PsApiManagementServiceFabric` to be used in cmdlet **New-AzApiManagementBackend** and **Set-AzApiManagementBackend**.</span></span>

## <span data-ttu-id="23c00-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23c00-107">EXAMPLES</span></span>

### <span data-ttu-id="23c00-108">Beispiel 1: Erstellen eines Back-End-Dienst Fabric-In-Memory-Objekts</span><span class="sxs-lookup"><span data-stu-id="23c00-108">Example 1: Create a Backend Service Fabric In-Memory Object</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$ManagementEndpoints = 'https://sfbackend-01.net:443', 'https://sfbackend-02.net:443'
PS C:\>$ServerCertificateThumbprints = '33CC47C6FCA848DC9B14A6F071C1EF7C'
PS C:\>$serviceFabric = New-AzApiManagementBackendServiceFabric -ManagementEndpoint  $ManagementEndpoints -ClientCertificateThumbprint "33CC47C6FCA848DC9B14A6F071C1EF7C" -ServerX509Name @{"CN=foobar.net" = @('33CC47C6FCA848DC9B14A6F071C1EF7C'); } -ServerCertificateThumbprint $ServerCertificateThumbprints

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -ServiceFabricCluster $serviceFabric -Description "service fabric backend" -PassThru
```

<span data-ttu-id="23c00-109">Erstellen eines Back-End-Dienst Fabric-Vertrags</span><span class="sxs-lookup"><span data-stu-id="23c00-109">Creates a Backend Service Fabric Contract</span></span>

## <span data-ttu-id="23c00-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="23c00-110">PARAMETERS</span></span>

### <span data-ttu-id="23c00-111">-ClientCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="23c00-111">-ClientCertificateThumbprint</span></span>
<span data-ttu-id="23c00-112">Fingerabdruck des Client Zertifikats für den Verwaltungsendpunkt</span><span class="sxs-lookup"><span data-stu-id="23c00-112">Client Certificate Thumbprint for the management endpoint.</span></span>
<span data-ttu-id="23c00-113">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23c00-113">This parameter is required.</span></span>

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

### <span data-ttu-id="23c00-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23c00-114">-DefaultProfile</span></span>
<span data-ttu-id="23c00-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23c00-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23c00-116">-ManagementEndpoint</span><span class="sxs-lookup"><span data-stu-id="23c00-116">-ManagementEndpoint</span></span>
<span data-ttu-id="23c00-117">Endpunkte der Service Fabric-Cluster Verwaltung</span><span class="sxs-lookup"><span data-stu-id="23c00-117">Service Fabric Cluster management Endpoints.</span></span>
<span data-ttu-id="23c00-118">Dieser Parameter ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="23c00-118">This parameter is required.</span></span>

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

### <span data-ttu-id="23c00-119">-MaxPartitionResolutionRetry</span><span class="sxs-lookup"><span data-stu-id="23c00-119">-MaxPartitionResolutionRetry</span></span>
<span data-ttu-id="23c00-120">Die maximale Anzahl von Wiederholungen beim Auflösen einer Service Fabric-Partition.</span><span class="sxs-lookup"><span data-stu-id="23c00-120">Maximum number of retries when resolving a Service Fabric partition.</span></span>
<span data-ttu-id="23c00-121">Dieser Parameter ist optional und der Standardwert 5.</span><span class="sxs-lookup"><span data-stu-id="23c00-121">This parameter is optional and default value is 5.</span></span>

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

### <span data-ttu-id="23c00-122">-ServerCertificateThumbprint</span><span class="sxs-lookup"><span data-stu-id="23c00-122">-ServerCertificateThumbprint</span></span>
<span data-ttu-id="23c00-123">Fingerabdruck des Zertifikat-Cluster Verwaltungsdiensts wird für die TLS-Kommunikation verwendet. Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="23c00-123">Thumbprint of certificates cluster management service uses for tls communication.This parameter is optional.</span></span>

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

### <span data-ttu-id="23c00-124">-ServerX509Name</span><span class="sxs-lookup"><span data-stu-id="23c00-124">-ServerX509Name</span></span>
<span data-ttu-id="23c00-125">Server-X509-Zertifikatsnamen-Sammlung.</span><span class="sxs-lookup"><span data-stu-id="23c00-125">Server X509 Certificate Names Collection.</span></span>
<span data-ttu-id="23c00-126">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="23c00-126">This parameter is optional.</span></span>

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

### <span data-ttu-id="23c00-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23c00-127">CommonParameters</span></span>
<span data-ttu-id="23c00-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23c00-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23c00-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23c00-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23c00-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23c00-130">INPUTS</span></span>

### <span data-ttu-id="23c00-131">System. String</span><span class="sxs-lookup"><span data-stu-id="23c00-131">System.String</span></span>

## <span data-ttu-id="23c00-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23c00-132">OUTPUTS</span></span>

### <span data-ttu-id="23c00-133">Microsoft. Azure. Commands. ApiManagement. Servicemanagement. Models. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="23c00-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="23c00-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="23c00-134">NOTES</span></span>

## <span data-ttu-id="23c00-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23c00-135">RELATED LINKS</span></span>

[<span data-ttu-id="23c00-136">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23c00-136">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="23c00-137">Neu – AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23c00-137">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="23c00-138">Neu – AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="23c00-138">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="23c00-139">Satz-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23c00-139">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="23c00-140">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="23c00-140">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
