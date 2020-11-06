---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/get-azurermenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Get-AzureRmEnvironment.md
ms.openlocfilehash: ef42490d18702682413fd2c0a19e301614ce4d94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495794"
---
# <span data-ttu-id="7f86a-101">Get-AzureRmEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f86a-101">Get-AzureRmEnvironment</span></span>

## <span data-ttu-id="7f86a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7f86a-102">SYNOPSIS</span></span>
<span data-ttu-id="7f86a-103">Abrufen von Endpunkten und Metadaten für eine Instanz von Azure Services.</span><span class="sxs-lookup"><span data-stu-id="7f86a-103">Get endpoints and metadata for an instance of Azure services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f86a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f86a-104">SYNTAX</span></span>

```
Get-AzureRmEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f86a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7f86a-105">DESCRIPTION</span></span>
<span data-ttu-id="7f86a-106">Das Get-AzureRmEnvironment-Cmdlet ruft Endpunkte und Metadaten für eine Instanz von Azure Services ab.</span><span class="sxs-lookup"><span data-stu-id="7f86a-106">The Get-AzureRmEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="7f86a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7f86a-107">EXAMPLES</span></span>

### <span data-ttu-id="7f86a-108">Beispiel 1: Abrufen der AzureCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="7f86a-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="7f86a-109">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureCloud (Standardumgebung) abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f86a-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="7f86a-110">Beispiel 2: Abrufen der AzureChinaCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="7f86a-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureChinaCloud | Format-List

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

<span data-ttu-id="7f86a-111">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureChinaCloud-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f86a-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="7f86a-112">Beispiel 3: Abrufen der AzureUSGovernment-Umgebung</span><span class="sxs-lookup"><span data-stu-id="7f86a-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzureRmEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="7f86a-113">In diesem Beispiel wird gezeigt, wie die Endpunkte und Metadaten für die AzureUSGovernment-Umgebung abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="7f86a-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="7f86a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f86a-114">PARAMETERS</span></span>

### <span data-ttu-id="7f86a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f86a-115">-DefaultProfile</span></span>
<span data-ttu-id="7f86a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7f86a-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f86a-117">-Name</span><span class="sxs-lookup"><span data-stu-id="7f86a-117">-Name</span></span>
<span data-ttu-id="7f86a-118">Gibt den Namen der Azure-Instanz an, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7f86a-118">Specifies the name of the Azure instance to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f86a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f86a-119">CommonParameters</span></span>
<span data-ttu-id="7f86a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f86a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f86a-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f86a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f86a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7f86a-122">INPUTS</span></span>

### <span data-ttu-id="7f86a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="7f86a-123">System.String</span></span>

## <span data-ttu-id="7f86a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7f86a-124">OUTPUTS</span></span>

### <span data-ttu-id="7f86a-125">Microsoft. Azure. Commands. profile. Models. PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f86a-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="7f86a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="7f86a-126">NOTES</span></span>

## <span data-ttu-id="7f86a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7f86a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7f86a-128">Add-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f86a-128">Add-AzureRMEnvironment</span></span>](./Add-AzureRMEnvironment.md)

[<span data-ttu-id="7f86a-129">Remove-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f86a-129">Remove-AzureRMEnvironment</span></span>](./Remove-AzureRMEnvironment.md)

[<span data-ttu-id="7f86a-130">Satz-AzureRMEnvironment</span><span class="sxs-lookup"><span data-stu-id="7f86a-130">Set-AzureRMEnvironment</span></span>](./Set-AzureRMEnvironment.md)

