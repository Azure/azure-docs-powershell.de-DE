---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azenvironment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzEnvironment.md
ms.openlocfilehash: 176874b9d3fbf192597cd98659e45df800dc819c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469216"
---
# <span data-ttu-id="a28d4-101">Get-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a28d4-101">Get-AzEnvironment</span></span>

## <span data-ttu-id="a28d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a28d4-102">SYNOPSIS</span></span>
<span data-ttu-id="a28d4-103">Erhalten Sie Endpunkte und Metadaten für eine Instanz von Azure-Diensten.</span><span class="sxs-lookup"><span data-stu-id="a28d4-103">Get endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a28d4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a28d4-104">SYNTAX</span></span>

```
Get-AzEnvironment [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a28d4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a28d4-105">DESCRIPTION</span></span>
<span data-ttu-id="a28d4-106">Das Get-AzEnvironment cmdlet ruft Endpunkte und Metadaten für eine Instanz von Azure-Diensten ab.</span><span class="sxs-lookup"><span data-stu-id="a28d4-106">The Get-AzEnvironment cmdlet gets endpoints and metadata for an instance of Azure services.</span></span>

## <span data-ttu-id="a28d4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a28d4-107">EXAMPLES</span></span>

### <span data-ttu-id="a28d4-108">Beispiel 1: Abrufen der AzureCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a28d4-108">Example 1: Getting the AzureCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureCloud

Name       Resource Manager Url          ActiveDirectory Authority
----       --------------------          -------------------------
AzureCloud https://management.azure.com/ https://login.microsoftonline.com/
```

<span data-ttu-id="a28d4-109">Dieses Beispiel zeigt, wie Sie die Endpunkte und Metadaten für die AzureCloud (Standardumgebung) erhalten.</span><span class="sxs-lookup"><span data-stu-id="a28d4-109">This example shows how to get the endpoints and metadata for the AzureCloud (default) environment.</span></span>

### <span data-ttu-id="a28d4-110">Beispiel 2: Abrufen der AzureChinaCloud-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a28d4-110">Example 2: Getting the AzureChinaCloud environment</span></span>
```
PS C:\> Get-AzEnvironment AzureChinaCloud | Format-List

Name                                              : AzureChinaCloud
EnableAdfsAuthentication                          : False
ActiveDirectoryServiceEndpointResourceId          : https://management.core.chinacloudapi.cn/
AdTenant                                          :
GalleryUrl                                        : https://gallery.chinacloudapi.cn/
ManagementPortalUrl                               : http://go.microsoft.com/fwlink/?LinkId=301902
ServiceManagementUrl                              : https://management.core.chinacloudapi.cn/
PublishSettingsFileUrl                            : http://go.microsoft.com/fwlink/?LinkID=301776
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

<span data-ttu-id="a28d4-111">Dieses Beispiel zeigt, wie Sie die Endpunkte und Metadaten für die AzureChinaCloud-Umgebung erhalten.</span><span class="sxs-lookup"><span data-stu-id="a28d4-111">This example shows how to get the endpoints and metadata for the AzureChinaCloud environment.</span></span>

### <span data-ttu-id="a28d4-112">Beispiel 3: Abrufen der AzureUSGovernment-Umgebung</span><span class="sxs-lookup"><span data-stu-id="a28d4-112">Example 3: Getting the AzureUSGovernment environment</span></span>
```
PS C:\> Get-AzEnvironment AzureUSGovernment

Name              Resource Manager Url                  ActiveDirectory Authority
----              --------------------                  -------------------------
AzureUSGovernment https://management.usgovcloudapi.net/ https://login.microsoftonline.us/
```

<span data-ttu-id="a28d4-113">Dieses Beispiel zeigt, wie Sie die Endpunkte und Metadaten für die AzureUSGovernment-Umgebung erhalten.</span><span class="sxs-lookup"><span data-stu-id="a28d4-113">This example shows how to get the endpoints and metadata for the AzureUSGovernment environment.</span></span>

## <span data-ttu-id="a28d4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a28d4-114">PARAMETERS</span></span>

### <span data-ttu-id="a28d4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a28d4-115">-DefaultProfile</span></span>
<span data-ttu-id="a28d4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a28d4-116">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a28d4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="a28d4-117">-Name</span></span>
<span data-ttu-id="a28d4-118">Gibt den Namen der zu erhaltenden Azure-Instanz an.</span><span class="sxs-lookup"><span data-stu-id="a28d4-118">Specifies the name of the Azure instance to get.</span></span>

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

### <span data-ttu-id="a28d4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a28d4-119">CommonParameters</span></span>
<span data-ttu-id="a28d4-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a28d4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a28d4-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a28d4-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a28d4-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a28d4-122">INPUTS</span></span>

### <span data-ttu-id="a28d4-123">System.String</span><span class="sxs-lookup"><span data-stu-id="a28d4-123">System.String</span></span>

## <span data-ttu-id="a28d4-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a28d4-124">OUTPUTS</span></span>

### <span data-ttu-id="a28d4-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span><span class="sxs-lookup"><span data-stu-id="a28d4-125">Microsoft.Azure.Commands.Profile.Models.PSAzureEnvironment</span></span>

## <span data-ttu-id="a28d4-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a28d4-126">NOTES</span></span>

## <span data-ttu-id="a28d4-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a28d4-127">RELATED LINKS</span></span>

[<span data-ttu-id="a28d4-128">Add-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a28d4-128">Add-AzEnvironment</span></span>](./Add-AzEnvironment.md)

[<span data-ttu-id="a28d4-129">Remove-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a28d4-129">Remove-AzEnvironment</span></span>](./Remove-AzEnvironment.md)

[<span data-ttu-id="a28d4-130">Set-AzEnvironment</span><span class="sxs-lookup"><span data-stu-id="a28d4-130">Set-AzEnvironment</span></span>](./Set-AzEnvironment.md)

