---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ac2ac931929acee527c900071de3062c4ef5398d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500478"
---
# <span data-ttu-id="c8f41-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8f41-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="c8f41-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c8f41-102">SYNOPSIS</span></span>
<span data-ttu-id="c8f41-103">Abrufen von Endpunkten und Metadaten für eine Instanz von Azure Services.</span><span class="sxs-lookup"><span data-stu-id="c8f41-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c8f41-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8f41-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c8f41-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c8f41-105">DESCRIPTION</span></span>
<span data-ttu-id="c8f41-106">Das Get-AzureRmEnvironment-Cmdlet ruft Endpunkte und Metadaten für eine Instanz von Azure Services ab.</span><span class="sxs-lookup"><span data-stu-id="c8f41-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="c8f41-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c8f41-107">EXAMPLES</span></span>

### <span data-ttu-id="c8f41-108">Beispiel 1: Abrufen der AzureCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c8f41-108">Example 1: Getting the AzureCloud environment</span></span>
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

<span data-ttu-id="c8f41-109">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureCloud (Standardumgebung) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8f41-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="c8f41-110">Beispiel 2: Abrufen der AzureChinaCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c8f41-110">Example 2: Getting the AzureChinaCloud environment</span></span>
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

<span data-ttu-id="c8f41-111">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureChinaCloud-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8f41-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="c8f41-112">Beispiel 3: Abrufen der AzureUSGovernment-Umgebung</span><span class="sxs-lookup"><span data-stu-id="c8f41-112">Example 3: Getting the AzureUSGovernment environment</span></span>
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
ActiveDirectoryAuthority                          : https://login.microsoftonline.us/
GraphUrl                                          : https://graph.windows.net/
GraphEndpointResourceId                           : https://graph.windows.net/
TrafficManagerDnsSuffix                           : usgovtrafficmanager.net
AzureKeyVaultDnsSuffix                            : vault.usgovcloudapi.net
AzureDataLakeStoreFileSystemEndpointSuffix        :
AzureDataLakeAnalyticsCatalogAndJobEndpointSuffix :
AzureKeyVaultServiceEndpointResourceId            : https://vault.usgovcloudapi.net
```

<span data-ttu-id="c8f41-113">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureUSGovernment-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c8f41-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="c8f41-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="c8f41-114">PARAMETERS</span></span>

### <span data-ttu-id="c8f41-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c8f41-115">-DefaultProfile</span></span>
<span data-ttu-id="c8f41-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c8f41-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c8f41-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c8f41-117">-Name</span></span>
<span data-ttu-id="c8f41-118">Gibt den Namen der Azure-Instanz an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c8f41-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="c8f41-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c8f41-119">CommonParameters</span></span>
<span data-ttu-id="c8f41-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c8f41-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c8f41-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c8f41-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c8f41-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c8f41-122">INPUTS</span></span>

### <span data-ttu-id="c8f41-123">Keine</span><span class="sxs-lookup"><span data-stu-id="c8f41-123">None</span></span>
<span data-ttu-id="c8f41-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c8f41-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c8f41-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c8f41-125">OUTPUTS</span></span>

### <span data-ttu-id="c8f41-126">PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8f41-126">PSAzureEnvironment</span></span>

## <span data-ttu-id="c8f41-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="c8f41-127">NOTES</span></span>

## <span data-ttu-id="c8f41-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c8f41-128">RELATED LINKS</span></span>

[<span data-ttu-id="c8f41-129">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8f41-129">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="c8f41-130">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8f41-130">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="c8f41-131">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="c8f41-131">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

