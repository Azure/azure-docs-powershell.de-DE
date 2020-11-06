---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 960a7f61ba181f267b264b27991f33a7b522c4e1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93475053"
---
# <span data-ttu-id="a673f-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="a673f-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="a673f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a673f-102">SYNOPSIS</span></span>
<span data-ttu-id="a673f-103">Abrufen von Endpunkten und Metadaten für eine Instanz von Azure Services.</span><span class="sxs-lookup"><span data-stu-id="a673f-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a673f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a673f-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a673f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a673f-105">DESCRIPTION</span></span>
<span data-ttu-id="a673f-106">Das Get-AzureRmEnvironment-Cmdlet ruft Endpunkte und Metadaten für eine Instanz von Azure Services ab.</span><span class="sxs-lookup"><span data-stu-id="a673f-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a673f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a673f-107">EXAMPLES</span></span>

### <span data-ttu-id="a673f-108">Beispiel 1: Abrufen der AzureCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a673f-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name                                              : AzureCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.windows.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.azure.com/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=254433
ServiceManagementUrl                              : https://management.core.windows.net/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301775
ResourceManagerUrl                                : https://management.azure.com/
SqlDatabaseDnsSuffix                              : .database.windows.net
StorageEndpointSuffix                             : core.windows.net
ActiveDirectoryAuthority                          : https://login.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : trafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.azure.net
AzureDataLakeStoreFileSystemEndpointSuffix        : azuredatalakestore.net
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix : azuredatalakeanalytics.net
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.net
```

<span data-ttu-id="a673f-109">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureCloud (Standardumgebung) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a673f-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="a673f-110">Beispiel 2: Abrufen der AzureChinaCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a673f-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : https://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : https://go.microsoft.com/fwlink/?LinkID=301776
ResourceManagerUrl                                : https://management.chinacloudapi.cn/
SqlDatabaseDnsSuffix                              : .database.chinacloudapi.cn
StorageEndpointSuffix                             : core.chinacloudapi.cn
ActiveDirectoryAuthority                          : https://login.chinacloudapi.cn/
GraphUrl                                          : https://graph.chinacloudapi.cn/
GraphEndpointResourceId                           : https://graph.chinacloudapi.cn/
TrafficManagerDnsSuffix                           : trafficmanager.cn
AzureKeyVaultDnsSuffix                            : vault.azure.cn
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.azure.cn
```

<span data-ttu-id="a673f-111">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureChinaCloud-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a673f-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="a673f-112">Beispiel 3: Abrufen der AzureUSGovernment-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a673f-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name                                              : AzureUSGovernment
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.usgovcloudapi.net/
AdTenant                                          :
GalleryUrl                                        : https://gallery.usgovcloudapi.net/
ManagementPortalUrl                               : https://manage.windowsazure.us
ServiceManagementUrl                              : https://management.core.usgovcloudapi.net/
PublishSettingsFileUrl                            : https://manage.windowsazure.us/publishsettings/index
ResourceManagerUrl                                : https://management.usgovcloudapi.net/
SqlDatabaseDnsSuffix                              : .database.usgovcloudapi.net
StorageEndpointSuffix                             : core.usgovcloudapi.net
ActiveDirectoryAuthority                          : https://login-us.microsoftonline.com/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="a673f-113">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureUSGovernment-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="a673f-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="a673f-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a673f-114">PARAMETERS</span></span>

### <span data-ttu-id="a673f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="a673f-115">-Name</span></span>
<span data-ttu-id="a673f-116">Gibt den Namen der Azure-Instanz an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="a673f-116">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a673f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a673f-117">CommonParameters</span></span>
<span data-ttu-id="a673f-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a673f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a673f-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a673f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a673f-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a673f-120">INPUTS</span></span>

## <span data-ttu-id="a673f-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a673f-121">OUTPUTS</span></span>

### <span data-ttu-id="a673f-122">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a673f-122">PSAzureEnvironment</span></span>

## <span data-ttu-id="a673f-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="a673f-123">NOTES</span></span>

## <span data-ttu-id="a673f-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a673f-124">RELATED LINKS</span></span>

[<span data-ttu-id="a673f-125">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a673f-125">Add-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="a673f-126">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a673f-126">Remove-AzureRMEnvironment</span></span>]()

[<span data-ttu-id="a673f-127">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="a673f-127">Set-AzureRMEnvironment</span></span>]()

